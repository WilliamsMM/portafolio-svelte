<script>
	import { page } from '$app/stores'
	import { Links } from '$lib/data/Links'
	import Icon from '@iconify/svelte'

	let currentPath = Links.filter((item) => item.href === $page.url.pathname)[0]

	$: currentPath = Links.filter((item) => item.href === $page.url.pathname)[0]
</script>

<header class="text-white text-center py-5 sm:bg-white sm:bg-opacity-10 sm:mb-10">
	<h1 class="text-4xl flex items-center justify-center gap-2">
		{currentPath.name}
		<Icon icon={currentPath.icon} />
	</h1>
</header>
