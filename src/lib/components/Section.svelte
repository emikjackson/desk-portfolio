<script>
	export let secondary = false;
	export let divider = true;
</script>

<div class="wrapper" class:secondary>
	<div class="content" class:divider>
		<slot />
	</div>
</div>

<style>
	.wrapper {
		display: flex;
		justify-content: center;
		background-color: #fff;
	}
	.secondary {
		/* background: linear-gradient(#f8f8f8, #fff); */
		background-color: #f9f9f9;
	}
	.content {
		display: flex;
		width: 1000px;
		max-width: 100%;
		margin: 60px 20px;
		box-sizing: border-box;
		justify-content: center;
		align-items: flex-start;
		border-top: none;
		margin-top: 20px;
	}
	.content.divider {
		border-top: 1px solid rgb(231, 231, 231);
		margin-top: 60px;
	}
</style>
