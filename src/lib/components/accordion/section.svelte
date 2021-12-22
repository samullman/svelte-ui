<script>
	import Accordion from "./Accordion.svelte";
	const array = [{title: "Item 1", description: "foobar"}, {title: "Item 2", description: "foobar"}, {title: "Item 3", description: "foobar"}];
</script>

<section>
	<h2>
		Accordion
		<hr style="margin-top:4px;" /> 
	</h2>

	<div>
		<pre>
			{"import { Accordion } from 'svelte-ui';"}
		</pre>
	</div>

	<Accordion array={ array } />
	
</section>