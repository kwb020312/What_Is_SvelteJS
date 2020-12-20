<script>
	const Person = [
		{
			name:'woobin',
			age:19
		},
		{
			name:'woohyuk',
			age:21
		},
		{
			name:'eungu',
			age:49
		}
	]
</script>

<main>
	{#each Person as {name,age} }
		<h1>He's name : {name} , and {age}</h1>
	{/each}
</main>