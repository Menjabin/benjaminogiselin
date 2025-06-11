<script lang="ts">
	import Countdown from './Countdown.svelte';
</script>

<svelte:head>
	<title>Iselin 💞 Benjamin</title>
	<meta name="description" content="Benjamin og Iselin gifter seg!" />
</svelte:head>

<section>
	<!-- <enhanced:img class="left" src="$lib/images/beach.jpeg" alt="Background image" />
	<enhanced:img class="right" src="$lib/images/beach.jpeg" alt="Background image" /> -->

	<h1>Iselin og Benjamin</h1>
	<p>Gifter seg 28. mars 2026, om</p>
	<Countdown />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	.left {
		position: fixed;
		inset: 0;
		width: auto;
		height: 100vh;
		object-fit: cover;
		object-position: center;
		z-index: -1;
		pointer-events: none;
	}

	.right {
		position: fixed;
		inset: 0;
		width: auto;
		height: 100vh;
		object-fit: cover;
		object-position: center;
		z-index: -1;
		pointer-events: none;
	}
</style>
