<script>
	function Say() {
		alert('Hello!!')
	}
</script>

<main>
	<button on:click|once|preventDefault={Say}>Say Hello</button>
</main>

<style>
</style>