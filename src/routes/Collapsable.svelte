<script lang="ts">
    let props = $props();
	let active = $state(false);

    const toggle = () => {
        console.log("toggle");
        active = !active;
    }
</script>

<div class="collapsable">
    <div class="question">
        {props.header}
        <div class="toggle-button" class:active onclick={toggle}>
            <i class="fa-solid fa-plus"></i>
        </div>
    </div>
    <div class="answer" class:active>{props.text}</div>
</div>

<style>
    .question {
        border: 1px var(--color-text);
        border-style: solid none;
        padding: 0.3rem;
        display: flex;
        justify-content: space-between;
    }

    .answer {
        display: none;
    }

    .answer.active {
        display: block;
        padding: 0.5rem;
    }

	.toggle-button i {
		transition: transform 0.3s ease-in-out;
	}
	
	.toggle-button.active i {
		transform: rotate(-45deg);
	}
</style>
