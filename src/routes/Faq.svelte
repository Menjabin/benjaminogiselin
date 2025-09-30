<script lang="ts">
    import Collapsable from './Collapsable.svelte';

    let entries = [
            {
                question: "Hva er kleskoden?",
                answer: "Veldig fint, og ikke noe hvitt."
            },
            {
                question: "Hvor kan man parkere?",
                answer: "Giskavollen parkeringshus ligger rett ved siden av kirken. Festen arrangeres i Betlehem, som ligger rett ved klostergarasjen."
            },
        ]
</script>

<div class="faq">
    {#each entries as entry}
        <Collapsable header={entry.question} text={entry.answer} />
    {/each}
</div>
