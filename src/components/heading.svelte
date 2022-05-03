<script>
	export let size = "";
	export let flat = "";
</script>

{#if size == 'h6'}
	<h6 class={ flat }>
		<slot />
	</h6>
{:else if size == 'h5'}
	<h5 class={ flat }>
		<slot />
	</h5>
{:else if size == 'h4'}
	<h4 class={ flat }>
		<slot />
	</h4>
{:else if size == 'h3'}
	<h3 class={ flat }>
		<slot />
	</h3>
{:else if size == 'h2'}
	<h2 class={ flat }>
		<slot />
	</h2>
{:else if size == 'h1'}
	<h1 class={ flat }>
		<slot />
	</h1>
{:else}
	<h2 class={ flat }>
		<slot />
	</h2>
{/if}

<style lang="scss">
	h1,
	h2,
	h3,
	h4,
	h5,
	h6 {
		margin-top: 0;

		&.flat {
			margin-bottom: 0 !important;
		}
	}

	h1 {
		margin-bottom: 1rem;
		font-size: 3em;
	}

	h2 {
		margin-bottom: 0.8rem;
		font-size: 2.4em;
	}

	h3 {
		margin-bottom: 0.6rem;
		font-size: 1.8em;
	}

	h4 {
		margin-bottom: 0.4rem;
		font-size: 1.2em;
	}

	h5 {
		margin-bottom: 0.2rem;
		font-size: 0.8em;
	}

	h6 {
		margin-bottom: 0.1rem;
		font-size: 0.4em;
	}
</style>
