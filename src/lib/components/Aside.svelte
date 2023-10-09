<script>
	import { Links } from '$lib/data/Links'
	import Icon from '@iconify/svelte'
</script>

<aside class="flex flex-col gap-2">
	{#each Links as item}
		<a
			class="flex items-center gap-2 text-xl py-3 hover:text-red-500 hover:translate-x-1 transition"
			href={item.href}
			target={item.target ?? null}
		>
			<Icon icon={item.icon} /> {item.name}</a
		>
	{/each}
</aside>
