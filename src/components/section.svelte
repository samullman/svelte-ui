<script>
	export let size = '';
</script>

<section class={size}>
	<slot />
</section>

<style lang="scss">
	section,
	section.md {
		padding: 1em;
	}

	section.sm {
		padding: 0.5em;
	}

	section.lg {
		padding: 2em;
	}

	section.xl {
		padding: 3em;
	}

	section.xxl {
		padding: 4em;
	}

	section:not(:last-child) {
		margin-bottom: 1em;
	}
</style>
