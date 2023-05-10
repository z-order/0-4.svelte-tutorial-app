<script>
	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
	<button on:click={toggle}>
		14. Log out
	</button>
{:else}
	<button on:click={toggle}>
		14. Log in
	</button>
{/if}