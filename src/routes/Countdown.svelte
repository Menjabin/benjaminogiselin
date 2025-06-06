<script lang="ts">
	import { Spring } from 'svelte/motion';

    const endDate = new Date('2026-03-28T13:00:00+02:00');
    let diff = endDate.getTime() - new Date().getTime();

    $: days    = Math.floor(diff / (1000 * 60 * 60 * 24));
    $: hours   = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    $: minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    $: seconds = new Spring(Math.floor((diff % (1000 * 60)) / 1000));

    setInterval(() => {
        diff = endDate.getTime() - new Date().getTime();
    }, 1000);
</script>

<div class="countdown">
    <strong>{days}</strong> dager, <strong>{hours}</strong> timer, <strong>{minutes}</strong> minutter og <strong>{seconds.current}</strong> sekunder
</div>

<style>
	.countdown {
		text-align: center;
        font-size: 3rem;
	}
</style>
