<script>
    import Faq from "../Faq.svelte";

</script>

<svelte:head>
	<title>Praktisk</title>
	<meta name="description" content="Praktisk" />
</svelte:head>

<div class="text-column">
	<h1>Praktisk</h1>

	<h2>Toastmastere</h2>
	<p>Har du noe du vil bidra med under festen? Ta kontakt med toastmasterne våre!</p>
	<ul>
		<li>Anne Berit Fevang: 977 63 159</li>
		<li>Ingvar Hatletvedt: 991 00 722</li>
	</ul>

	<h2>FAQ</h2>
	<Faq />
</div>

<style>
	h1, h2, p, ul {
		margin: .3rem;
	}

	ul {
		font-size: 1.3rem;
		margin-bottom: 1rem;
	}

	.text-column {
		width: 90%;
		padding: 0.3rem;
	}
</style>
