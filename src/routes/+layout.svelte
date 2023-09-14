<script>
	import Header from '$lib/components/Header.svelte';
	import '../app.css';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="true" />
	<link
		href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,600;0,700;1,400&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<Header />

<main>
	<slot />
</main>
