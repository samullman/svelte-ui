<script>
	import Section from '../../components/section.svelte';
	import Heading from '../../components/heading.svelte';
	import Button from '../../components/button.svelte';
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
	<Heading size="h1">Buttons</Heading>

	<div>
		<pre>
			{"import { Button } from 'svelte-ui';"}
		</pre>
	</div>

	<Heading size="h4">Button "sm"</Heading>

	<div>
		{#each colors as color}
			<Button {color} size="sm">
				{color}
			</Button>
		{/each}
	</div>

	<br />

	<Heading size="h4">Button "md"</Heading>
	<div>
		{#each colors as color}
			<Button {color}>
				{color}
			</Button>
		{/each}
	</div>

	<br />

	<Heading size="h4">Button "lg"</Heading>

	{#each colors as color}
		<Button {color} size="lg">
			{color}
		</Button>
	{/each}
</Section>
