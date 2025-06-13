<script lang="ts">
	import Countdown from './Countdown.svelte';
</script>

<svelte:head>
	<title>Iselin 💞 Benjamin</title>
	<meta name="description" content="Iselin og Benjamin gifter seg!" />
</svelte:head>

<section>
	<!-- <figure>
		<enhanced:img src="$lib/images/beach.jpeg" alt="Main background" />
		<figcaption>
			<time datetime="2026-03-28">28 · 03 · 2026</time>
		</figcaption>
	</figure> -->

	<!-- <div class="container">
		<div class="center-image">
			<enhanced:img src="$lib/images/beach.jpeg" alt="Main background" />
		</div>
		<h1>28 · 03 · 2026</h1>
	</div> -->
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

	figure {
		display: grid;
		width: min(90vw, 600px);
		margin-inline: auto;
	}

	figure > * {
		grid-area: 1 / 1;
	}

	figure time {
		place-self: center;
		letter-spacing: 0.04em;
	}

	/* .container {
		width: 100%;
		height: 100vh;
		display: grid;
		grid-template-columns: repeat(26, 1fr);
		grid-template-rows: repeat(18, 1fr);
	}

	.center-image {
		display: inline;
		z-index: -1;
	}

	h1 {
		display: inline-block;
		text-align: center;
		width: 100%;
	} */
</style>
