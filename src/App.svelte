<script>
	let num = 0;
	function Increase() {
		num++
	}
</script>

<main>
	{#if num === 0}
		<h1>변수가 초기값입니다.</h1>
	{:else if num < 5}
		<h1>변수가 5 미만 입니다.</h1>
	{:else}
		<h1>변수가 5 이상 입니다.</h1>
	{/if}
	<button on:click={Increase}>변수 값 증가</button>
</main>