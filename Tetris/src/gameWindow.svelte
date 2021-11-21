<script>
	import {onMount} from 'svelte';
	onMount(() => {
			let gameContainer = document.getElementById("game-container")
			let rect = gameContainer.getBoundingClientRect()
			let width = rect.right - rect.left
			let height = rect.top - rect.bottom
			console.log(width, height)
		});
</script>

<div id="game-container">
	<div class="preview"></div>
</div>

<style>
	#game-container {
		position: relative; /* so .preview can be absolutely positioned */
		border: solid;
		height: 600px;
		width: 80%;
		margin: auto; /* center it */
		background-size: 50px 50px; /* scale for grid */
		background-image:
			linear-gradient(to right, grey 1px, transparent 1px),
			linear-gradient(to bottom, grey 1px, transparent 1px);
	}

	.preview {
		position: absolute;
		border: solid;
		width: 100px;
		height: 200px;
		right: 0px;
		top: 0px;
		margin-top: 5px;
		margin-right: 5px;
	}
</style>
