<script>
	import HTML from '$lib/assets/html5.png'
	import CSS from '$lib/assets/css3.png'
	import GITHUB from '$lib/assets/github.png'
	import JS from '$lib/assets/javascript.png'
	import TS from '$lib/assets/typescript.png'
	import SVELTEKIT from '$lib/assets/sveltekit.png'
	import { fly } from 'svelte/transition'
	import { animationConfig } from '$lib/utils/animation-config'

	// Habilidades
	const skills = [
		{
			name: 'HTML 5',
			img: HTML
		},
		{
			name: 'CSS',
			img: CSS
		},
		{
			name: 'JavaScript',
			img: JS
		},
		{
			name: 'TypeScript',
			img: TS
		},
		{
			name: 'SvelteKit',
			img: SVELTEKIT
		},
		{
			name: 'Github',
			img: GITHUB
		}
	]
</script>

<div in:fly={animationConfig} style="height: calc(100vh - 190px)" class="flex max-w-4xl mx-auto flex-wrap justify-center items-center gap-10">
	{#each skills as skill}
		<div
			
			class="w-40 p-4 flex flex-col gap-2 items-center justify-center bg-white bg-opacity-20 rounded-lg shadow-2xl"
		>
			<img class="h-28 object-cover rounded-xl" src={skill.img} alt={skill.name} />
			<h3 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
				{skill.name}
			</h3>
		</div>
	{/each}
</div>
