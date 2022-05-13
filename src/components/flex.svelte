<script>
	export let color = '';
	export let size = '';
	export let rounded = '';
</script>

<div>
	<slot />
</div>

<style lang="scss">
	div {
		display: flex;
	}
</style>
