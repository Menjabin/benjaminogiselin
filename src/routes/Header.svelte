<script lang="ts">
	import { page } from '$app/state';
	import { onMount } from 'svelte';

	let active = false;

	onMount(() => {
		const toggleButton = document.querySelector('.toggle-button');
		toggleButton?.addEventListener('click', () => {
			active = !active;
		});
	});
</script>

<header>
	<nav>
		<div class="links" class:active="{active}">
			<ul>
				<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
					<a href="/">Hjem</a>
				</li>
				<li aria-current={page.url.pathname === '/program' ? 'page' : undefined}>
					<a href="/program">Program</a>
				</li>
				<li aria-current={page.url.pathname === '/onskeliste' ? 'page' : undefined}>
					<a href="/onskeliste">Ønskeliste</a>
				</li>
				<li aria-current={page.url.pathname === '/bordoversikt' ? 'page' : undefined}>
					<a href="/bordoversikt">Bordoversikt</a>
				</li>
			</ul>
		</div>
		<div class="site-title">
			<a href="/">Iselin & Benjamin</a>
		</div>
		<div class="toggle-button" class:active="{active}">
			<i class="fa-solid fa-plus"></i>
		</div>
	</nav>
</header>

<style>
	header {
		padding: 1rem;
	}

	nav {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
	}

	/** Style navigation links */
	nav .links {
		margin: auto;
	}

	nav .links ul {
		padding: 0;
		display: flex;
		justify-content: center;
		list-style: none;
	}

	nav .links ul li[aria-current='page'] {
		text-decoration: underline;
	}

	nav .links ul li a {
		padding: 0 0.5rem;
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	.toggle-button {
		position: absolute;
		top: 1.6rem;
		right: 0.9rem;
		display: none;
		font-size: 1.2rem;
	}

	.toggle-button i {
		transition: transform 0.3s ease-in-out;
	}
	
	.toggle-button.active i {
		transform: rotate(-45deg);
	}

	@media (max-width: 1300px) {
		nav {
			display: flex;
			flex-direction: column-reverse;
		}

		nav .links {
			display: none;
			width: 100%;
			flex-direction: column;
		}

		nav .links.active {
			display: block;
		}

		nav .links ul {
			margin: 0;
			flex-direction: column;
			text-align: right;
		}

		.toggle-button {
			display: inline;
		}
	}

	/** Style site title */
	.site-title {
		margin: auto;
	}

	.site-title a {
		font-weight: bolder;
		font-size: 1.8rem;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	/** Hover effect on all links */
	a:hover {
		color: var(--color-theme-2);
	}
</style>
