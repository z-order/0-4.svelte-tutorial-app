<script>
	let count = 0;

    $: console.log('08-1. the count is ' + count);

    $: {
	    console.log('08-2. the count is ' + count);
    }

	$: if (count >= 10) {
		alert('08-3. count is dangerously high!');
		count = 9;
	}

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	08. Clicked {count} {count === 1 ? 'time' : 'times'}
</button>