<script>
	export let color = '';
	export let size = '';
	export let rounded = '';
</script>

<div>
	<div class={`dashed ${color} ${size} ${rounded}`}>
		<slot />
	</div>
</div>

<style lang="scss">
	.dashed {
		padding: 1em;
		border: 2px dashed black;
		margin-bottom: 1em;
		display: inline-block;
	}

	.rounded {
		border-radius: 0.5em;
	}

	.dashed.red {
		border-color: var(--red);
	}

	.dashed.blue {
		border-color: var(--blue);
	}

	.dashed.yellow {
		border-color: var(--yellow);
	}

	.dashed.orange {
		border-color: var(--orange);
	}

	.dashed.purple {
		border-color: var(--purple);
	}

	.dashed.pink {
		border-color: var(--pink);
	}

	.dashed.green {
		border-color: var(--green);
	}

	.dashed.lime {
		border-color: var(--lime);
	}

	.dashed.teal {
		border-color: var(--teal);
	}
</style>
