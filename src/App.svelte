<script>
	let count = 0;
	$: double = count*2
	const onClick = () => {
		count++
	}
	$: if(count >= 10) {
		alert(`Counting Number is ${count}`)
	}
</script>

<main>
	<input type="button" on:click={onClick} value="카운트 업!" />
	<p>{double} 회 누르셨습니다.</p>
</main>