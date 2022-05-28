<script>
	let show = false;

	function showMenu() {
		show = true;
	}
	function hideMenu() {
		show = false;
	}
</script>

<div>
	<span on:mouseenter={showMenu}>Mouse over ME</span>
</div>

{#if show}
	<div class="card" on:mouseenter={showMenu} on:mouseleave={hideMenu}>
		<div>
			<span class="cardTitle">Card Title</span>
		</div>
		<div class="cardStrokeInfo">
			<span>Field 1</span>
			<span>Inf 1</span>
		</div>
		<div class="cardStrokeInfo">
			<span>Field 2</span>
			<span>Inf 2</span>
		</div>
		<div class="cardStrokeInfo">
			<span>Field 3</span>
			<span>Inf 3</span>
		</div>
	</div>
{/if}

<style>
	.card {
		border: 1px solid black;
		display: flex;
		flex-direction: column;
		width: 200px;
		padding: 4px 10px;
		background-color: #f6d886;
	}
	.cardTitle {
		font-size: 22px;
		font-weight: 600;
	}
	.cardStrokeInfo {
		margin-top: 8px;
		display: flex;
		justify-content: space-between;
		flex-direction: row;
		align-items: center;
	}
</style>
