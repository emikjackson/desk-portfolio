<script>
	export let title = '';
	export let id = '';
</script>

<div class="section">
	<h2 {id}>{title}</h2>
	<slot />
</div>

<style>
	h2 {
		padding-top: 40px;
	}
</style>
