<script lang="ts">
	import Countdown from './Countdown.svelte';
</script>

<svelte:head>
	<title>Iselin 💞 Benjamin</title>
	<meta name="description" content="Iselin og Benjamin gifter seg!" />
</svelte:head>

<section>
	<p class="standout">Gifter seg 28. mars 2026, om</p>
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
</style>
