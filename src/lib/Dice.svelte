<script>
	let from;
	let to;
	let rng = '5';
	function generate() {
		rng = Math.floor(1 + Math.random() * to + from);
	}
</script>

<div class="card center-text" style="margin-left: 10px; margin-right: 10px;">
	<h1>Random #</h1>
	<p>{rng}</p>
	<input type="text" placeholder="from" bind:value={from} />
	<input type="text" placeholder="to" bind:value={to} />
	<div class="is-horizontal-align">
		<button class="btn btn-primary" style=" width: 100%;" on:click={generate}>
			<i class="bi bi-arrow-clockwise" />
		</button>
	</div>
</div>

<style>
	input {
		padding: 12px 20px;
		margin: 8px 0;
		box-sizing: border-box;
		border: none;
		border-bottom: 1.5px solid var(--font-color);
	}
	input[type='text'] {
		margin: 5px;
		background-color: var(--bg-accent);
		color: var(--font-color);
	}

	button {
		color: white;
		margin: 0;
	}
</style>
