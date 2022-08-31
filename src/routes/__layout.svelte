<script>
	import { onMount } from 'svelte';
	onMount(async () => {
		if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
			document.body.classList.add('dark');
			var element = document.getElementById('icon');
			element.classList.remove('bi-moon-stars');
			element.classList.add('bi-sun');
		}
		if (window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches) {
			document.body.classList.add('light');
			var element = document.getElementById('icon');
			element.classList.remove('bi-sun');
			element.classList.add('bi-moon-stars');
		}
	});
	function theme() {
		document.body.classList.toggle('dark');
		var element = document.getElementById('icon');
		if (document.body.classList.contains('dark')) {
			element.classList.add('bi-sun');
			element.classList.remove('bi-moon-stars');
		} else {
			element.classList.remove('bi-sun');
			element.classList.add('bi-moon-stars');
		}
	}
</script>

<header class="navbar">
	<section class="navbar-section">
		<a href="/" class="btn btn-link btn-action"><i class="bi bi-house-door" /></a>
		<div class="dropdown">
			<a href="#" class="btn btn-link dropdown-toggle" tabindex="0">
				<i class="bi bi-list" />
			</a>
			<ul class="menu">
				<li><a href="/rules" class="btn btn-link">Rules</a></li>
				<li><a href="/about" class="btn btn-link">About</a></li>
			</ul>
		</div>
	</section>
	<section class="navbar-center" />
	<section class="navbar-section">
		<button on:click={theme} class=" btn btn-link btn-action " style="display:flex;">
			<i id="icon" class="bi bi-sun " />
		</button>
	</section>
</header>
<div class="mainmargin">
	<slot />
</div>

<style>
	@import '../../node_modules/spectre.css/dist/spectre.min.css';
	@import '../../node_modules/bootstrap-icons/font/bootstrap-icons.css';
	@import '../App.css';
	:root {
		--bg-color: #ffffff;
		--font-color: #000000;
		--bg-accent: #d0d0d0;
	}
	:global(body.dark) {
		--bg-color: #282b30;
		--font-color: #ececec;
		--bg-accent: #0f1011;
	}
	:global(body) {
		background-color: var(--bg-color);
		color: var(--font-color);
		font-size: 16px;
	}
	.mainmargin {
		margin: 5px;
	}
	.menu {
		color: var(--font-color);
		background-color: var(--bg-color);
		box-shadow: 0 0.05rem 0.2rem var(--bg-accent);
	}
	.btn-link {
		color: var(--font-color);
	}
	.btn-link:hover {
		color: var(--font-color);
	}
	.btn-link:focus {
		color: var(--font-color);
	}
	.bi {
		font-size: 1.5em;
	}
</style>
