<script>
	import Counter from '$lib/counter.svelte';
	import Dice from '$lib/Dice.svelte';
	import { onMount } from 'svelte';
	onMount(async () => {});
</script>

<div class="container center">
	<div class="columns">
		<Counter />
		<Dice />
		<Counter />
	</div>
</div>

<style>
	.center {
		display: flex;
		align-items: center; /* Vertical center alignment */
		justify-content: center; /* Horizontal center alignment */
	}
</style>
