<script lang="ts">
	import Header from './Header.svelte';
	import { page } from '$app/state';
	import '../app.css';

	let { children } = $props();
	let background = $derived(page.url.pathname === '/'
		? 'image'
		: 'color');
</script>

<div class="app">
	<Header />

	<main class={background}>
		{@render children()}
	</main>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main.image {
		background-color: none;
	}

	main.color {
		background-color: var(--color-bg-1);
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>
