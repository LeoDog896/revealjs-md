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
		<section data-markdown>
			<textarea data-template>
			  ## Slide 1
			  A paragraph with some text.
			  ---
			  ## Slide 2
			  ---
			  ## Slide 3
			</textarea>
		</section>
	</div>
</div>
<Tailwindcss />