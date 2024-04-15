<script lang="ts">
	import Autoplay from 'embla-carousel-autoplay';
	import * as Carousel from '$lib/components/ui/carousel/index.js';

	import servicesObj from '$lib/helpers/servicesConfig';
	import Card from './Card/Card.svelte';
</script>

<Carousel.Root
	opts={{ loop: true }}
	plugins={[
		Autoplay({
			delay: 2000,
			stopOnMouseEnter: true
		})
	]}
	class="w-full"
>
	<Carousel.Content class="-ml-1">
		{#each servicesObj as service, i (i)}
			<Carousel.Item class="pl-1 md:basis-1/2 lg:basis-1/3">
				<div class="flex h-full p-1">
					<Card title={service.title} description={service.description} />
				</div>
			</Carousel.Item>
		{/each}
	</Carousel.Content>
	<Carousel.Previous class="bg-secondary" />
	<Carousel.Next class="bg-secondary" />
</Carousel.Root>
