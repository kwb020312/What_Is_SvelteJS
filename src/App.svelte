<script>
	let checked = false
</script>

<main>
	<input type="checkbox" bind:checked={checked} />
	{#if checked}
		<h1>체크 됨</h1>
	{:else}
		<h1>체크되지 않음</h1>
	{/if}
</main>