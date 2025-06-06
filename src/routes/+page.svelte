<script lang="ts">
	import Countdown from './Countdown.svelte';
</script>

<svelte:head>
	<title>Benjamin 💞 Iselin</title>
	<meta name="description" content="Benjamin og Iselin gifter seg!" />
</svelte:head>

<section>
	<enhanced:img class="background" src="$lib/images/rose.jpg" alt="Background image" />

	<h1>Benjamin og Iselin</h1>
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

	.background {
		position: fixed;
		inset: 0;
		width: 100vw;
		height: 100vh;
		object-fit: cover;
		object-position: center;
		z-index: -1;
		pointer-events: none;
	}
</style>
