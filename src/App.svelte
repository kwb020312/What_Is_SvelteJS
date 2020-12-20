<script>
	let testObj = {
		name:'woobin',
		gender:'M'
	}
	const onChange = () => {
		testObj.gender = "W"
	}
</script>

<main>
	<p>Name : {testObj.name}</p>
	<p>Gender : {testObj.gender}</p>
	<button on:click={onChange}>Change Gender</button>
</main>