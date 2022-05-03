<script>
	import Section from '../../components/section.svelte';
	import Heading from '../../components/heading.svelte';
</script>

<Section>
	<Heading size="h1">Input</Heading>

	<div>
		<pre>
			{"import { Input } from 'svelte-ui';"}
		</pre>
	</div>

	<div>
		<div>
			<label>Text</label>
		</div>
		<input />
	</div>

	<div>
		<div>
			<label>Date</label>
		</div>
		<input type="date" />
	</div>

	<div>
		<div>
			<label>Datetime</label>
		</div>
		<input type="datetime-local" />
	</div>

	<div>
		<div>
			<label>Range</label>
		</div>
		<input type="range" />
	</div>

	<div>
		<div>
			<label>Email</label>
		</div>
		<input type="email" placeholder="example@email.com" />
	</div>

	<div>
		<div>
			<label>Email</label>
		</div>
		<textarea />
	</div>

	<div>
		<label>
			<input type="checkbox" />
			<span> Checkbox </span>
		</label>
	</div>

	<div>
		<div>
			<label> Select </label>
		</div>

		<select>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
		</select>
	</div>
</Section>

<style lang="scss">
	input {
		font-size: inherit;
		font-family: inherit;
		cursor: pointer;
	}

	label {
		font-weight: bold;
		font-size: 13px;
		display: inline-block;
		margin-bottom: 3px;
	}

	input {
		font-size: 14px;
		padding: 4px 8px;
		border-radius: 5px;
		margin-bottom: 0.75em;
		min-height: 21px;
	}

	select {
		font-size: 14px;
		border-radius: 5px;
		padding: 5px;
		margin-bottom: 0.75em;
		font-style: normal;
		min-height: 21px;
		border-width: 2px;
		border-style: inset;
		border-color: -internal-light-dark(rgb(118, 118, 118), rgb(133, 133, 133));
	}

	textarea {
		font-size: 14px;
		border-radius: 5px;
		padding: 6px;
		margin-bottom: 0.75em;
		font-style: normal;
		min-height: 21px;
		border-width: 2px;
		border-style: inset;
		border-color: -internal-light-dark(rgb(118, 118, 118), rgb(133, 133, 133));
	}
</style>
