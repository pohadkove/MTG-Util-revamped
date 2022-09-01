<script>
	import { onMount } from 'svelte';
	onMount(async () => {});
	let count = 20;

	function p1lps() {
		count -= 1;
	}
	function p1lpa() {
		count += 1;
	}
</script>

<div class="card counter center-text">
	<div class="card-header">
		<h1
			contenteditable="true"
			style="width:fit-content; margin-left: 10px; margin-right: 10pxem;"
			class="center-text"
		>
			Player
		</h1>
	</div>
	<div class="card-image ">
		<i class="bi bi-person" />
	</div>
	<div class="card-body">
		<button class="btn btn-primary" on:click={p1lps}>
			<i class="bi bi-dash" />
		</button>
		{count}
		<button class="btn btn-primary" on:click={p1lpa}><i class="bi bi-plus" /></button>
	</div>
</div>

<style>
	.bi-person {
		font-size: 3em;
	}
</style>
