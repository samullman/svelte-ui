<script>
	import Section from '../../components/section.svelte';
	import Heading from '../../components/heading.svelte';
	const colors = ['red', 'green', 'blue', 'yellow', 'purple', 'pink', 'orange', 'teal', 'lime'];
</script>

<Section size="md">
	<Heading size="h2">Section</Heading>

	<div>
		<pre>
			{"import { Section } from 'svelte-ui';"}
		</pre>
	</div>


	<div class="section-border">
		<Section size="sm">
			This element has padding
		</Section>
		</div>

	<br />

	<div class="section-border">
	<Section size="md">
		This element has padding
	</Section>
	</div>

	<br />

	<div class="section-border">
	<Section size="lg">
		This element has padding
	</Section>
	</div>

	<br />

	<div class="section-border">
	<Section size="xl">
		This element has padding
	</Section>
	</div>
</Section>


<style lang="scss">
	.section-border {
		border: 1px dashed green;
	}

</style>