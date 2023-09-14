<script>
	/**
	 * @type {any}
	 */
	export let src;
	/**
	 * @type {string}
	 */
	export let alt;
	export let width = '300px';
	export let height = 'auto';
</script>

<img {src} {alt} {width} {height} />

<style>
	img {
		margin: 20px;
		margin-top: 40px;
	}
</style>
