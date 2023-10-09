<script>
	export let ms = 200
	let isActive = false

	setTimeout(() => {
		isActive = true
	}, ms)
</script>

<div class={`transition-all duration-[${ms}] ${!isActive ? 'opacity-0 scale-50' : null}`}>
	<slot />
</div>
