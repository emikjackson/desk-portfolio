<script>
	export let link = '';
</script>

<div class="button-wrapper">
	<a class="button-like" href={link} rel="noopener noreferrer" target="_blank"><slot /></a>
</div>

<style>
	.button-wrapper {
		display: inline-block;
	}

	a.button-like {
		position: relative;
		padding: 8px 18px;
		background-color: #d82543;
		color: #fff0f6;
		border-radius: 8px;
		text-decoration: none;
		border-bottom: 4px solid #bd1a35;
		transition: all 0.1s linear;
		display: inline-block;
		margin-top: 0px;
	}

	.button-wrapper:hover a.button-like {
		margin-top: 2px;
		border-bottom: 2px solid #b01730;
		background-color: #d41b3a;
	}
</style>
