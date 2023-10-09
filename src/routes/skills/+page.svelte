<script>
	import HTML from '$lib/assets/html5.png'
	import CSS from '$lib/assets/css3.png'
	import GITHUB from '$lib/assets/github.png'
	import JS from '$lib/assets/javascript.png'
	import TS from '$lib/assets/typescript.png'
	import SVELTEKIT from '$lib/assets/sveltekit.png'
	import { fly } from 'svelte/transition'
	import { animationConfig } from '$lib/utils/animation-config'
	import BoxAnimated from '$lib/components/BoxAnimated.svelte'

	// Habilidades
	const skills = [
		{
			name: 'HTML 5',
			img: HTML,
			ms: 200,
		},
		{
			name: 'CSS',
			img: CSS,
			ms: 300,
		},
		{
			name: 'JavaScript',
			img: JS,
			ms: 400,
		},
		{
			name: 'TypeScript',
			img: TS,
			ms: 500,
		},
		{
			name: 'SvelteKit',
			img: SVELTEKIT,
			ms: 600,
		},
		{
			name: 'Github',
			img: GITHUB,
			ms: 700,
		}
	]
</script>

<div class="flex max-w-4xl mx-auto flex-wrap justify-center items-center gap-10">
	{#each skills as skill}
		<BoxAnimated ms={skill.ms}>
			<div
				class="w-40 p-4 flex flex-col gap-2 items-center justify-center bg-white bg-opacity-20 rounded-lg shadow-2xl"
			>
				<img class="h-28 object-cover rounded-xl" src={skill.img} alt={skill.name} />
				<h3 class="mb-2 text-xl font-bold tracking-tight text-gray-900 dark:text-white">
					{skill.name}
				</h3>
			</div>
		</BoxAnimated>
	{/each}
</div>
