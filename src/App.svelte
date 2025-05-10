<!-- DEPENDENCIES -->
<!-- npm i degit -->
<!-- npm install -->

<!-- How to create a new svelte project: -->
<!-- degit sveltejs/template [project-name]-->

<!-- alternative way -->
<!-- npx degit sveltejs/template [project-name] -->
<!---------------------------------------------->

<!-- HOW TO START SERVER: -->
<!-- npm run build -->
<!-- npm run dev -->


<!-- JAVASCRIPT -->
<script>
	import { onMount } from 'svelte';
	import ColorBox from "./Components/ColorBox.svelte";

	const _boxes = Array.from({ length: 15 }); //the total number of boxes in the application.

	//When svelte first mounts
	onMount(() => {
		const body = document.body;
		body.style.backgroundColor = 'black';
	});
</script>

<!-- HTML -->
<div class="wrapper">
	<div class="ColorBoxGrid">
		{#each _boxes as _, i}
			<ColorBox />
		{/each}
	</div>
</div>

<!-- CSS -->
<style>
	.wrapper{
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.ColorBoxGrid {
		padding: 1rem;

		display: grid;
		grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
		width: fit-content; 
		gap: 1rem;
	}
</style>