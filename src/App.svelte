<script>
	let login = false;
	function isLogin() {
		login = !login
	}
</script>

<main>
	{login}
	{#if !login}
	<button on:click={isLogin}>로그인</button>
	{/if}
	{#if login}
	<button on:click={isLogin}>로그아웃</button>
	{/if}
</main>