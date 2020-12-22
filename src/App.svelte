<script>
	import Outer from './Outer.svelte';
</script>

<main>
	<Outer on:msg={e => console.log(e)} />
</main>

<style>
</style>