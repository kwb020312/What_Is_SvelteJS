<script>
	let count = 0;
	const onClick = () => {
		count++
	}
</script>

<main>
	<input type="button" on:click={onClick} value="카운트 업!" />
	<p>{count} 회 누르셨습니다.</p>
</main>