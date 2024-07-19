<script>
	import { fade } from 'svelte/transition';

	export let src;
	export let alt;
	export let width = 'auto';
	export let height = 'auto';
</script>

<div class="wrapper">
	<img transition:fade {src} {alt} {width} {height} />
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
		}
	}
</style>
