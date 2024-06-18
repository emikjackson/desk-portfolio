<script>
	/**
	 * A link that's styled a bit more like a button!
	 * For CTA use on the project cards
	 */
	export let href = '/';
	export let secondary = false;
</script>

<a {href} rel="noopener noreferrer" target="_blank" class:secondary>
	<slot />
</a>

<style>
	a {
		padding: 4px 8px;
		border-radius: 4px;
		background-color: #0a7350;
		box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.1);
		color: white;
		margin-right: 2px;
		text-decoration: none;
		border: 1px solid white;
	}
	a.secondary {
		color: #0a7350;
		background-color: white;
		border: 1px solid #0a7350;
	}
</style>
