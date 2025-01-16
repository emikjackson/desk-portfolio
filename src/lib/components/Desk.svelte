<script>
	/**
	 * Hero display of large desk image & intro text
	 */
	import deskImg from '$lib/assets/full_desk.png';
	import { onMount } from 'svelte';

	let show = false;
	onMount(() => (show = true));
</script>

<div class="wrapper">
	<div class="column">
		<img
			class:show
			src={deskImg}
			alt="Sketch of office setup with a laptop, art supplies, & a sewing machine. A cat is below the desk."
		/>
		<div class="text" class:show>
			<h1>Welcome!</h1>
			<p>I'm Emi, a web developer based out of Detroit, Michigan.</p>
			<p class="second-line">You've made it to my desk.</p>
		</div>
	</div>
</div>

<style>
	.wrapper {
		display: flex;
		justify-content: center;
	}
	.column {
		max-width: 100%;
		display: flex;
		margin-bottom: 40px;
		gap: 0px;
	}
	img {
		width: 700px;
		height: 525px;
		opacity: 0;
		transform: translateY(5px);
		transition: opacity 1.5s ease, transform 1.5s ease;
	}
	.show,
	.show h1,
	.show p {
		opacity: 1;
		transform: translateY(0px);
	}
	.text {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		padding-right: 60px;
	}
	p {
		margin-top: 0px;
	}
	h1,
	p {
		opacity: 0;
		transform: translateY(5px);
	}
	h1 {
		margin-bottom: 30px;
		transition: all 2s ease;
		transition-delay: 0.5s;
	}
	p {
		transition: all 1.5s ease;
		transition-delay: 1.5s;
	}
	p.second-line {
		transition-delay: 2.5s;
	}

	@media (max-width: 1000px) {
		.column {
			flex-direction: column;
			gap: 10px;
			margin-bottom: 0px;
			align-items: center;
			text-align: center;
		}
		.text {
			padding: 20px;
			align-items: center;
			padding-bottom: 0px;
		}
		img {
			max-width: 100%;
			max-height: auto;
			max-height: calc(100vw * (525 / 700));
		}
	}
</style>
