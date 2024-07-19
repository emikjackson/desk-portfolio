<script>
	export let title = '';
	export let id = '';
	export let subtitle = false; // use h3 instead of h2
</script>

<div class="text">
	{#if subtitle}
		<h3 {id}>{title}</h3>
	{:else}
		<h2 {id}>{title}</h2>
	{/if}
	<slot />
</div>

<style>
	.text {
		flex-grow: 1;
	}
	h2 {
		padding-top: 40px;
	}
	h3 {
		margin-top: 0px;
		padding-top: 0px;
		font-size: 1.3rem;
	}
	@media (max-width: 1000px) {
		h2,
		h3 {
			padding-top: 0px;
		}
	}
</style>
