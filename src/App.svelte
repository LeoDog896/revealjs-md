<script lang="ts">
	import Tailwindcss from "./Tailwindcss.svelte"
	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown.esm.js';
	import { onMount } from "svelte"

	onMount(() => {
		let deck = new Reveal({
			plugins: [ Markdown ]
		})

		deck.initialize();
	})
</script>
<div class="reveal">
	<div class="slides">
		<div class="slides">
			<section data-background-color="#0c2f5c">Slide 1</section>
			<section data-background-color="#0c2f5c">Slide 2</section>
		  </div>
	</div>
</div>
<Tailwindcss />