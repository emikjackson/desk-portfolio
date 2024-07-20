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
			<h2 class="desktop">Hi, welcome to my desk! I'm Emi.</h2>
			<h2 class="mobile">Hi, welcome to my desk!<br />I'm Emi.</h2>
			<p>I like to make <strong>web tools</strong> and do other things.</p>
			<p>Scroll on to see what I'm working on these days.</p>
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
		transition: all 1.5s ease;
	}
	.show,
	.show h2,
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
	h2,
	p {
		opacity: 0;
		transform: translateY(5px);
		transition: all 1.5s ease;
		transition-delay: 0.5s;
	}
	p {
		transition-delay: 1s;
	}
	.desktop {
		display: block;
	}
	.mobile {
		display: none;
		line-height: 2.2rem;
	}

	@media (max-width: 1000px) {
		.desktop {
			display: none;
		}
		.mobile {
			display: block;
		}
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
