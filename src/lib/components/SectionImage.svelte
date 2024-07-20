<script>
	import { onMount } from 'svelte';

	export let src;
	export let alt;
	export let width = 'auto';
	export let height = 'auto';

	let show = false;
	onMount(() => (show = true));
</script>

<div class="wrapper">
	<img class:show {src} {alt} {width} {height} />
</div>

<style>
	.wrapper {
		display: inline-flex;
		justify-content: center;
		align-items: center;
	}
	img {
		margin: 20px;
		margin-top: 40px;
		opacity: 0;
		transition: opacity 1s ease;
	}

	img.show {
		opacity: 1;
		transform: translateY(0px);
	}

	@media (max-width: 1000px) {
		.wrapper {
			display: flex;
			width: 100%;
			padding-top: 20px;
		}
		img {
			max-width: 100%;
			margin: 0px;
			height: auto;
		}
	}
</style>
