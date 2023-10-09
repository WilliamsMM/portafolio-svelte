<script>
	import Photo from '$lib/assets/photo.jpg'
	import { animationConfig } from '$lib/utils/animation-config'
	import { fly } from 'svelte/transition'
</script>

<div style="height: calc(100vh - 190px)" class="flex flex-wrap justify-evenly w-full">
	<article class="flex flex-col items-center">
		<img
			in:fly={animationConfig}
			class="w-full my-5 max-w-xs rounded-full pointer-events-none shadow-2xl select-none"
			src={Photo}
			alt="Williams Moya"
		/>

		<article
			in:fly={{ x: 20, y: 30, opacity: 0 }}
			class="flex flex-col items-center p-5 gap-3 sm:gap-6"
		>
			<h1 class="text-3xl sm:text-4xl">I am Williams Moya</h1>
			<h2 class="text-2xl sm:text-3xl">Front-end Developer</h2>
		</article>
	</article>

	<div in:fly={{ x: 20, y: 30, opacity: 0 }} class="py-6 flex max-w-md flex-col items-center">
		<p class="text-xl bg-white bg-opacity-20 p-5 rounded-lg shadow-xl">
			I am a front-end web developer with expertise in creating attractive and functional web
			interfaces. I specialize in HTML, CSS, and JavaScript, and have experience with popular
			frameworks like React, Svelte, and Vue.
		</p>
		<div class="flex justify-evenly w-full">
			<div class="w-5 h-3 bg-white bg-opacity-20" />
			<div class="w-5 h-3 bg-white bg-opacity-20" />
		</div>
		<p class="text-xl bg-white bg-opacity-20 p-5 rounded-lg shadow-2xl">
			I am skilled in UI/UX design, version control, and collaborating with teams. I strive to stay
			updated on the latest technologies and deliver high-quality products that provide excellent
			user experiences. I am eager to contribute to challenging projects and continue growing as a
			developer.
		</p>
	</div>

	<div class="w-full flex justify-center h-14">
		<a
			href="/skills"
			class="relative inline-flex items-center justify-center p-4 px-5 py-3 overflow-hidden font-medium text-indigo-600 transition duration-300 ease-out rounded-full shadow-xl group hover:shadow-2xl"
		>
			<span
				class="absolute inset-0 w-full h-full bg-gradient-to-br from-white via-black to-gray-700"
			/>
			<span
				class="absolute bottom-0 right-0 block w-64 h-64 mb-32 mr-4 transition duration-500 origin-bottom-left transform rotate-45 translate-x-24 bg-pink-50 rounded-full opacity-30 group-hover:rotate-90 ease"
			/>
			<span class="relative text-white">Go to Skills</span>
		</a>
	</div>
</div>
