<script>
	let x = 7;
</script>

{#if x > 10}
	<p>15. {x} is greater than 10</p>
{:else if 5 > x}
	<p>15. {x} is less than 5</p>
{:else}
	<p>15. {x} is between 5 and 10</p>
{/if}