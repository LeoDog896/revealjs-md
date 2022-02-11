<script lang="ts">
	import Tailwindcss from "./Tailwindcss.svelte"
	import Reveal from 'reveal.js';
	import { marked } from "marked"
	import { onMount } from "svelte"

	const text = `
	# Test 1
	%
	# Test 2
	`

	onMount(() => {
		let deck = new Reveal()

		deck.initialize();
	})
</script>
<div class="reveal">
	<div class="slides">
		<div class="slides text-white text-4xl">
			{#each text.split("%") as slide}
				<section data-background-color="#0c2f5c">
					{@html marked.parse(slide)}
				</section>
			{/each}
		  </div>
	</div>
</div>
<Tailwindcss />