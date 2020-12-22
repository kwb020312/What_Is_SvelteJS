<script>
	import Button from "./Button.svelte";
	function onClick () {
		alert('클릭되었음!')
	}
</script>

<main>
	<Button on:click={onClick} />
</main>