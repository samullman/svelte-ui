<script>
	import Section from '../../components/section.svelte';
	import Heading from '../../components/heading.svelte';
	import Dashed from '../../components/dashed.svelte';
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
	<Heading size="h1">Dashed</Heading>

	<div>
		<pre>
			{"import { Dashed } from 'svelte-ui';"}
		</pre>
	</div>

	<Heading size="h4">Button "sm"</Heading>

	<div>
		{#each colors as color}
			<Dashed {color} size="sm" rounded="rounded">
				{color}
			</Dashed>
		{/each}
	</div>

	<br />
</Section>
