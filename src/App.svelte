<script>
	import Other from './Other.svelte'
	const TestObj = {
		name:'woobin',
		age:19,
		job:'Programmer'
	}
</script>

<main>
	<Other {...TestObj} />
</main>