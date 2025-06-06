<script lang="ts">
	import { page } from '$app/state';
    import Countdown from './Countdown.svelte';
</script>

<header>
	<nav>
		<ul>
			<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Hjem</a>
			</li>
			<li aria-current={page.url.pathname === '/program' ? 'page' : undefined}>
				<a href="/program">Program</a>
			</li>
			<li aria-current={page.url.pathname === '/meny' ? 'page' : undefined}>
				<a href="/meny">Meny</a>
			</li>
			<li aria-current={page.url.pathname === '/bordoversikt' ? 'page' : undefined}>
				<a href="/bordoversikt">Bordoversikt</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		background-color: none;
		padding: 1rem;
	}

	nav {
		display: flex;
		justify-content: center;
		background-color: none;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
