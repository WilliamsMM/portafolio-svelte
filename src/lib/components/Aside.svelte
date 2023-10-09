<script>
	import { page } from '$app/stores'
	import { Links } from '$lib/data/Links'
	import Icon from '@iconify/svelte'

	let currentPath = Links.filter((item) => item.href === $page.url.pathname)[0]
	$: currentPath = Links.filter((item) => item.href === $page.url.pathname)[0]
</script>

<aside
	class="flex justify-center py-4 sm:px-2 sm:py-2 flex-wrap sm:justify-start sm:flex-col gap-3 sm:gap-2 sm:h-screen w-full sm:w-52 z-10 sm:bg-white sm:bg-opacity-10"
>
	{#each Links as item}
		<a
			class="flex items-center gap-1 text-xl p-2 sm:py-3 rounded-lg transition-all {currentPath.href ===
			item.href
				? 'bg-white text-black sm:pl-5'
				: 'hover:bg-opacity-20 sm:hover:pl-5 hover:text-black hover:bg-white px-2'}"
			href={item.href}
			target={item.target ?? null}
		>
			<Icon icon={item.icon} /> {item.name}</a
		>
	{/each}
</aside>
