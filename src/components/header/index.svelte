<script lang="ts">
	import Sidebar from '../../components/sidebar.svelte';
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
	import { linear } from 'svelte/easing';
	import Heading from '../heading.svelte';

	let visible = false;
</script>

<header>
	<div class="title">
		<a sveltekit:prefetch href="/"> Svelte UI </a>
	</div>

	<div class="nav">
		<ul>
			<li>
				<a sveltekit:prefetch href="/" class:active={$page.url.pathname === '/'}>Home</a
				>
			</li>

			<li>
				<a
					sveltekit:prefetch
					href="/about"
					class:active={$page.url.pathname === '/about'}>About</a
				>
			</li>

			<li>
				<a
					sveltekit:prefetch
					href="/todos"
					class:active={$page.url.pathname === '/todos'}>Todos</a
				>
			</li>

			<li>
				<a>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 22 22"
						width="22"
						height="22"
						><path fill="none" d="M0 0h24v24H0z" /><path
							d="M12 2C6.475 2 2 6.475 2 12a9.994 9.994 0 0 0 6.838 9.488c.5.087.687-.213.687-.476 0-.237-.013-1.024-.013-1.862-2.512.463-3.162-.612-3.362-1.175-.113-.288-.6-1.175-1.025-1.413-.35-.187-.85-.65-.013-.662.788-.013 1.35.725 1.538 1.025.9 1.512 2.338 1.087 2.912.825.088-.65.35-1.087.638-1.337-2.225-.25-4.55-1.113-4.55-4.938 0-1.088.387-1.987 1.025-2.688-.1-.25-.45-1.275.1-2.65 0 0 .837-.262 2.75 1.026a9.28 9.28 0 0 1 2.5-.338c.85 0 1.7.112 2.5.337 1.912-1.3 2.75-1.024 2.75-1.024.55 1.375.2 2.4.1 2.65.637.7 1.025 1.587 1.025 2.687 0 3.838-2.337 4.688-4.562 4.938.362.312.675.912.675 1.85 0 1.337-.013 2.412-.013 2.75 0 .262.188.574.688.474A10.016 10.016 0 0 0 22 12c0-5.525-4.475-10-10-10z"
						/></svg
					>
				</a>
			</li>
			<li>
				<a>
					<Sidebar right bind:visible>
						<div slot="toggle">
							<svg
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 22 22"
								width="22"
								height="22"
								><path fill="none" d="M0 0h24v24H0z" /><path
									d="M3 4h18v2H3V4zm0 7h18v2H3v-2zm0 7h18v2H3v-2z"
								/></svg
							>
						</div>

						<div slot="content" class="list">
							<Heading size="h4">Components</Heading>

							<ul>
								<li>
									<a sveltekit:prefetch href="/components/anchor"> Anchor </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/button"> Button </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/dashed"> Dashed </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/flex"> Flex </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/grid"> Grid </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/loader"> Loader </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/input"> Input </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/section"> Section </a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/breadcrumb">
										Breadcrumb
									</a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/accordion">
										Accordion
									</a>
								</li>

								<li>
									<a sveltekit:prefetch href="/components/tabs"> Tabs </a>
								</li>

								<li>Container</li>

								<li>
									Tooltip

									<ul>
										<li>Light</li>
										<li>Dark</li>
									</ul>
								</li>
								<li>
									<a sveltekit:prefetch href="/components/input"> Input </a>

									<ul>
										<li>Text</li>
										<li>Checkbox</li>
										<li>Radio</li>
										<li>Select</li>
										<li>Colorwheel</li>
									</ul>
								</li>
							</ul>
						</div>
					</Sidebar>
				</a>
			</li>
		</ul>
	</div>
</header>

<style lang="scss">
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
	.nav > ul {
		position: relative;
		margin: 0;
		display: flex;
		list-style: none;
		padding-right: 32px;
	}

	li {
		display: flex;
		align-items: center;
		margin-left: 1em;
	}

	svg {
		color: black;
		cursor: pointer;
		opacity: 1;
		&:hover {
			opacity: 0.6;
		}
	}

	.list ul {
		list-style: none;
		padding-inline-start: 0;

		li {
			margin-left: 0;
			margin-bottom: 0.25em;
		}
	}
</style>
