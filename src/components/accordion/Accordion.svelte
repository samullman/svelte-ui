<script>
	import AccordionRow from './AccordionRow.svelte';
	export let array = [];
</script>

<div class="accordion">
	{#each array as item}
		<AccordionRow title={item.title} content={item.content} />
	{/each}
</div>

<style>
	.accordion {
		max-width: 400px;
		border-bottom: 1px solid #2d2d2d;
	}
</style>
