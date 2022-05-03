<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import Section from "../components/section.svelte";
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>


<Section>
	visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit
</Section>

</footer>



<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		padding-top: 51px;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		border-top: 1px solid #2d2d2d;
	}

</style>
