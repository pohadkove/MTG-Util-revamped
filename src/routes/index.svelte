<script>
	import Counter from '$lib/counter.svelte';
	import Dice from '$lib/Dice.svelte';
	import { onMount } from 'svelte';
	onMount(async () => {});
</script>

<div class="container">
	<div class="columns">
		<Counter />
		<Dice />
		<Counter />
	</div>
</div>

<style>
</style>
