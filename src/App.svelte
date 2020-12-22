<script>
	import Inner from './Inner.svelte'
</script>

<main>
	<Inner on:msg={e => console.log(e)} />
</main>

<style>
</style>