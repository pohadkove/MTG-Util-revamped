<script>
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
		<h1 contenteditable="true" style="width:fit-content;">Player 2</h1>
	</div>
	<div class="card-image ">
		<i class="bi bi-person" />
	</div>
	<div class="card-body">
		<button class="btn btn-primary" on:click={p1lps}><i class="bi bi-dash" /></button>
		{count}
		<button class="btn btn-primary" on:click={p1lpa}><i class="bi bi-plus" /></button>
	</div>
</div>

<style>
</style>
