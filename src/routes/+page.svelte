<script>
	import Photo from '$lib/assets/photo.jpg'
	import { fly } from 'svelte/transition'
</script>

<div class="flex gap-5 py-5 w-full">
	<img
		in:fly={{ x: -20, y: -30, opacity: 0 }}
		width="320"
		class="w-full my-5 max-w-xs pointer-events-none rounded-3xl shadow-2xl select-none"
		src={Photo}
		alt="Williams Moya"
	/>

	<article in:fly={{ x: 20, y: 30, opacity: 0 }} class="flex flex-col p-5 gap-6">
		<h1 class="text-5xl">I am Williams Moya</h1>
		<h2 class="text-4xl">Front-end Developer</h2>

		<p class="max-w-md text-lg">
			I am a front-end web developer with expertise in creating attractive and functional web
			interfaces. I specialize in HTML, CSS, and JavaScript, and have experience with popular
			frameworks like React, Svelte, and Vue.
		</p>
	</article>
</div>
