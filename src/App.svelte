<script lang="ts">
	import Tailwindcss from "./Tailwindcss.svelte"
	import Reveal from 'reveal.js';
	import { marked } from "marked"
	import { onMount } from "svelte"

	const text = `
# Test 1
## The chronicles
woah
%%
# Test 2`

	onMount(() => {
		let deck = new Reveal()

		deck.initialize();
	})
</script>
<div class="reveal">
	<div class="slides">
		<div class="slides text-white leading-[4rem]">
			{#each text.split("%%") as slide}
				<section data-background-color="#0c2f5c">
					{@html marked.parse(slide)}
				</section>
			{/each}
		  </div>
	</div>
</div>
<style global>
	h1 {
		font-size: 4rem;
	}

	h2 {
		font-size: 3rem;
	}

	p {
		font-size: 2rem;
	}
</style>
<Tailwindcss />