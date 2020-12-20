<script>
	let point = {x:0 , y:0}
	function MouseMove(e) {
		point.x = e.clientX;
		point.y = e.clientY;
	}
</script>

<main>
	<div on:mousemove={MouseMove}>
		Your x : {point.x} AND y : {point.y}
	</div>
</main>

<style>
	div {
		width:100%;
		height:100vh;
	}
</style>