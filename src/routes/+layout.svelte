<script lang="ts">
	import '../app.css';
	import Header from '$components/Header/Header.svelte';
	import Footer from '$components/Footer/Footer.svelte';
</script>

<div class="container flex flex-col justify-between min-h-screen py-4 mx-auto sm:max-w-[85vw]">
	<Header />
	<main class="flex-grow">
		<slot></slot>
	</main>
	<Footer />
</div>
