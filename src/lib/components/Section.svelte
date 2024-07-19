<script>
	export let secondary = false;
	export let divider = false;
	export let nested = false; // nested section
	export let flip = false; // flip to column-reverse direction on mobile
	export let style = '';
</script>

<div class="wrapper" class:secondary>
	<div class="content" class:divider class:nested class:flip {style}>
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
		gap: 30px;
	}
	.content.divider {
		border-top: 1px solid rgb(231, 231, 231);
		margin-top: 80px;
	}
	.content.nested {
		justify-content: flex-start;
		margin-top: 10px;
	}
	@media (max-width: 1000px) {
		.content {
			flex-direction: column;
		}
		.flip {
			flex-direction: column-reverse;
		}
	}
</style>
