<script>
	const getData = async() => {
		const jsonData = await fetch('https://jsonplaceholder.typicode.com/todos/3')
		const data = await jsonData.json()
		return data.title
	}
</script>

<main>
	{#await getData()}
		<p>데이터를 가져오는중..</p>
	{:then data} 
		<p>가져온 데이터는 {data}</p>
	{:catch err}
		<p>{err}</p>
	{/await}
</main>