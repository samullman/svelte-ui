<script lang="ts">
	import Heading from '../../components/heading.svelte';
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
</script>

<header>
		<div class="title">
			<a sveltekit:prefetch href="/">
				Svelte UI
			</a>
		</div>

	

	<div class="nav">
		
		<ul>
			<li><a sveltekit:prefetch href="/" class:active={$page.path === '/'}>Home</a></li>
			<li><a sveltekit:prefetch href="/about" class:active={$page.path === '/about'}>About</a></li>
			<li><a sveltekit:prefetch href="/todos" class:active={$page.path === '/todos'}>Todos</a></li>
		</ul>
		
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		border-bottom: 1px solid #2d2d2d;
		position: fixed;
		width: 100vw;
		background: white;
		z-index: 1000;
		padding: 1em;
	}

	.nav {
		display: flex;
		align-items: center;
	}

	.title {
		font-size: 1.5em;
		font-weight: bold;
		margin-bottom: 0;
	}
	ul {
		position: relative;
		margin: 0;
		display: flex;
		list-style: none;
		padding-right: 32px;
	}

	li {
		display: inline-block;
		margin-left: 1em;

		
	}

	a {
		color: black;		
	}

	
</style>
