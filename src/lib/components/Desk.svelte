<script>
	/**
	 * Hero display of large desk image & intro text
	 */
	import deskImg from '$lib/assets/full_desk.png';
</script>

<div class="wrapper">
	<div class="column">
		<img
			src={deskImg}
			alt="Sketch of office setup with a laptop, art supplies, & a sewing machine. A cat is below the desk."
		/>
		<div class="text">
			<h2>Hi, welcome to my desk! I'm Emi.</h2>
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
	}
	img {
		width: 700px;
	}
	.text {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		padding-right: 60px;
	}
</style>
