<svelte:head>
	<title>Ønskeliste</title>
	<meta name="description" content="Meny" />
</svelte:head>

<div class="text-column">
	<h1>Ønskeliste</h1>

	<a class="kitchn" target="_blank" href="https://www.kitchn.no/bryllup/vis-liste/223349/">
		Kitchn
	</a>

	<a class="vipps" target="_blank" href="https://qr.vipps.no/wish-list/2a96f888-8679-481b-4c6c-08ddf3c193f3">
		Vipps
	</a>
</div>

<style>
	h1 {
		margin: 0;
	}

	.text-column {
		width: 70%;
		padding: 0.3rem;
	}

	a {
		text-align: center;
		display: block;
		margin: 1rem 0;
		padding: 0.5rem 1rem;
		font-size: 1.2rem;
		border: none;
		border-radius: 5px;
		cursor: pointer;
	}

	.kitchn {
		background-color: #000000;
		color: white;
	}

	.vipps {
		background-color: #ec6739;
		color: white;
	}
</style>
