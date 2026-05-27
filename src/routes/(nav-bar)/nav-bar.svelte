<script lang="ts">
	import { resolve } from '$app/paths';
	import DarkMode from './(dark-mode)/dark-mode.svelte';
	import SideBar from '../(side-bar)/side-bar.svelte';

	const navComponent = [
		{
			label: 'Home',
			path: resolve('/')
		},
		{
			label: 'About',
			path: resolve('/#about')
		},
		{
			label: 'Projects',
			path: resolve('/#projects')
		},
		{
			label: 'Tools',
			path: resolve('/#tools')
		},
		{
			label: 'Contact',
			path: resolve('/#contact')
		}
	];
</script>

<main></main>
<nav class="sticky top-0 flex items-center justify-center bg-card px-5 py-3 shadow">
	<DarkMode />
	<ul class="mr-auto ml-auto flex gap-5">
		{#each navComponent as navComponents (navComponents.label)}
			<li>
				<a href={navComponents.path} class="rounded-md p-2 hover:bg-gray-300"
					>{navComponents.label}</a
				>
			</li>
		{/each}
	</ul>
	<SideBar />
</nav>
