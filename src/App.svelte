<script>
	let point = {x:0 , y:0}
	function MouseMove(e) {
		point.x = e.clientX;
		point.y = e.clientY;
	}
</script>

<main>
	<div on:mousemove={e => point: { point.x = e.clientX , y : clientY}}>
		Your x : {point.x} AND y : {point.y}
		Inline Function Apply
	</div>
</main>

<style>
	div {
		width:100%;
		height:100vh;
	}
</style>