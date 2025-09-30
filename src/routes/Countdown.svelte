<script lang="ts">
	import { Spring } from 'svelte/motion';

    const endDate = new Date('2026-03-28T12:30:00+02:00');
    let diff = endDate.getTime() - new Date().getTime();

    $: days    = Math.floor(diff / (1000 * 60 * 60 * 24));
    $: hours   = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    $: minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    $: seconds = new Spring(Math.floor((diff % (1000 * 60)) / 1000));

    setInterval(() => {
        diff = endDate.getTime() - new Date().getTime();
    }, 1000);
</script>

<div class="countdown standout">
    <div class="days"><strong>{days}</strong> dager,</div>
    <div class="hours"><strong>{hours}</strong> timer,</div>
    <div class="minutes"><strong>{minutes}</strong> minutter,</div>
    <div class="seconds"><strong>{seconds.current}</strong> sekunder</div>
</div>

<style>
	.countdown {
		text-align: center;
        font-size: 3rem;
        display: flex;
        gap: 1rem;
	}

    @media (max-width: 1300px) {
        .countdown {
            flex-direction: column;
            gap: 0;
        }
    }
</style>
