<script>
	export let color;
</script>

<button class={color}>
	<slot />
</button>

<style lang="scss">
	button:focus:not(:focus-visible) {
		outline: none;
	}

	button {
		font-size: inherit;
		font-family: inherit;
		cursor: pointer;
	}

	button {
		border-width: 0.1em;
		font-size: 1em;
		padding: 0.25em 0.5em;
		border-radius: 0.35em;
		transition: all 21s ease;
	}

	button:active {
		position: relative;
		top: 0.1em;
	}

	button {
		margin: 0 0.2em 0.2em 0;
	}

	button:active {
		filter: brightness(95%);
	}

	button.red {
		border-color: var(--red);
		color: var(--red);
	}

	button.blue {
		border-color: var(--blue);
		color: var(--blue);
	}

	button.yellow {
		border-color: var(--yellow);
		color: var(--yellow);
	}

	button.orange {
		border-color: var(--orange);
		color: var(--orange);
	}

	button.purple {
		border-color: var(--purple);
		color: var(--purple);
	}

	button.pink {
		border-color: var(--pink);
		color: var(--pink);
	}

	button.green {
		border-color: var(--green);
		color: var(--green);
	}

	button.lime {
		border-color: var(--lime);
		color: var(--lime);
	}

	button.teal {
		border-color: var(--teal);
		color: var(--teal);
	}
</style>
