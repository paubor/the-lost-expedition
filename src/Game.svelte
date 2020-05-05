<script>
	import Expedition from './Expedition.svelte';
	import Path from './Path.svelte';
	import Camp from './Camp.svelte';
	let playerPosition = 4;
</script>

<style>
	h1 {
		color: purple;
	}

	.part {
		margin-bottom: 10px;
	}
</style>

<header>
 <h1>The Lost Solo Expedition</h1>
</header>
<div class="part">
	<Expedition {playerPosition}/>
</div>
<div class="part">
	<Path />
</div>
<div class="part">
	<Camp />
</div>
<!--<Explorers /> -->

