<script>
	import Footer from '../lib/components/Footer.svelte'
	import Aside from '$lib/components/Aside.svelte'
	import BackgroundAnimated from '$lib/components/BackgroundAnimated.svelte'
	import Header from '$lib/components/Header.svelte'
	import '../app.css'
	import '../bgAnimated.scss'
</script>

<BackgroundAnimated />

<main class="sm:flex-row flex flex-col">
	<Aside />

	<div class="w-full">
		<Header />

		<div style="min-height: calc(100vh - 190px)">
			<slot />
		</div>

		<Footer />
	</div>
</main>

<style>
	:global(:root) {
		font-family: 'Red Hat Display', sans-serif;
		color: white;
	}
</style>
