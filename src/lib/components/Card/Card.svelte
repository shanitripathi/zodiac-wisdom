<script lang="ts">
	import Shiva from '$assets/images/shiva.jpg';
	export let title = '';
	export let description = '';
</script>

<div class="m-4 mx-auto overflow-hidden bg-white shadow-md rounded-xl md:max-w-2xl grow">
	<div class="flex-col md:flex">
		<div class="relative md:flex-shrink-0">
			<!-- svelte-ignore a11y-img-redundant-alt -->
			<img class="object-cover w-full h-full" src={Shiva} alt="An image" />
		</div>
		<div class="p-4">
			<div class="text-sm font-semibold tracking-wide text-indigo-500 uppercase">
				{title}
			</div>
			<p class="mt-2 text-gray-500">{description}</p>
		</div>
	</div>
</div>
