<script>
	import Section from '../../components/section.svelte';
	import Heading from '../../components/heading.svelte';
	import Button from '../../components/anchor.svelte';
	const colors = [
		'red',
		'green',
		'blue',
		'yellow',
		'purple',
		'pink',
		'orange',
		'teal',
		'lime'
	];
</script>

<Section>
	<Heading size="h1">Anchor</Heading>

	<div>
		<pre>
			{"import { A } from 'svelte-ui';"}
		</pre>
	</div>

	{#each colors as color}
		<Button {color}>
			{color}
		</Button>
	{/each}
</Section>
