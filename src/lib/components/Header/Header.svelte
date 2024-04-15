<script lang="ts">
	import { fly } from 'svelte/transition';
	import Anchor from '$components/Anchor.svelte';
	import { isMenuOpen } from '$stores';
	import { MenuIcon, XCircleIcon } from 'svelte-feather-icons';
	import { browser } from '$app/environment';

	$: if ($isMenuOpen && browser) {
		document.body.style.overflow = 'hidden';
	} else if (browser) {
		document.body.style.overflow = 'auto';
	}

	const handleScrollIntoView = (id: string) => {
		$isMenuOpen = false;
		const element = document.getElementById(id);
		console.log(element);
		element && element.scrollIntoView({ behavior: 'smooth', block: 'start' });
	};
</script>

<header class="text-tertiary">
	<nav class="flex justify-between">
		<Anchor href="/" isBold={true}>Astroshiva</Anchor>
		<ul class="hidden space-x-2 sm:flex">
			<button on:pointerup={() => handleScrollIntoView('services-section')}>Services</button>
			<button on:pointerup={() => handleScrollIntoView('about-us-section')}>About-Us</button>
			<button on:pointerup={() => handleScrollIntoView('contact-section')}>Contact</button>
		</ul>
		<button
			on:pointerup={() => {
				$isMenuOpen = !$isMenuOpen;
			}}
			class="sm:hidden relative z-[100]"
			>{#if $isMenuOpen}<XCircleIcon />{:else}<MenuIcon />{/if}</button
		>

		{#if $isMenuOpen}
			<div
				transition:fly={{ duration: 300, x: 500 }}
				class="fixed top-0 right-0 z-10 w-full h-full sm:hidden bg-secondary"
			>
				<ul class="flex flex-col pt-4 pl-3 space-y-2">
					<button on:pointerup={() => handleScrollIntoView('services-section')}>Services</button>
					<button on:pointerup={() => handleScrollIntoView('about-us-section')}>About-Us</button>
					<button on:pointerup={() => handleScrollIntoView('contact-section')}>Contact</button>
				</ul>
			</div>
		{/if}
	</nav>
</header>
