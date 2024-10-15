<script>
	import GamesHeader from '$lib/components/GamesHeader.svelte';
	import '../../app.css';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="true" />
	<link
		href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,600;0,700;1,400&family=Lalezar&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="wrapper">
	<GamesHeader />

	<main>
		<slot />
	</main>
</div>

<style>
	.wrapper {
		background-color: #c3dfec;
		background: linear-gradient(#c3dfec, #b3dddf);
		color: #0f212b;
		min-height: 100vh;
	}
</style>
