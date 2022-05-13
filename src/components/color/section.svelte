<script>
	import Color from './color.svelte';
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

<section>
	<h2>
		Buttons
		<hr style="margin-top:4px;" />
	</h2>

	<div>
		<pre>
			{"import { Button } from 'svelte-ui';"}
		</pre>
	</div>

	{#each colors as color}
		<Color {color}>
			{color}
		</Color>
	{/each}
</section>
