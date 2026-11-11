<script lang="ts">
	import favicon from '#lib/assets/favicon.svg';
	import type { LayoutProps } from './$types';
	import '../app.css';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav class="flex gap-4 p-4 bg-gray-200">
	<img src={favicon} alt="Favicon" class="w-6 h-6" />
	<ul class="flex flex-row gap-4">
		<li><a href="/">Home</a></li>
		<li><a href="/about">About</a></li>
		<li><a href="/contact">Contact</a></li>
	</ul>
</nav>

{@render children()}
