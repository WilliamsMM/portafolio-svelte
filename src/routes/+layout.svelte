<script>
	import Aside from '$lib/components/Aside.svelte'
	import BackgroundAnimated from '$lib/components/BackgroundAnimated.svelte'
	import Header from '$lib/components/Header.svelte'
	import Icon from '@iconify/svelte'
	import '../app.css'
	import '../bgAnimated.scss'
</script>

<BackgroundAnimated />

<main class="sm:flex-row flex flex-col">
	<Aside />

	<div class="w-full">
		<Header />
		<slot />

		<footer
			class="flex justify-between p-5 w-full"
		>
			<div class="flex items-center gap-1">
				<p>Built with:</p>
				<a href="https://kit.svelte.dev" target="_blank">Sveltekit</a>
			</div>

			<div>
				<a
					class="flex items-center gap-1"
					href="https://www.linkedin.com/in/williamsmm"
					target="_blank"><Icon icon="devicon:linkedin" /> Linkedin</a
				>
			</div>
		</footer>
	</div>
</main>

<style>
	:global(:root) {
		font-family: 'Red Hat Display', sans-serif;
		color: white;
	}
</style>
