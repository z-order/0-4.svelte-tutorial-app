<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
        // below method doesn't work for triggering reactivity
        //numbers.push(numbers.length + 1);
        
        // And this works
		numbers = [...numbers, numbers.length + 1];

        // or this works either
        //numbers[numbers.length] = numbers.length + 1;

        // or this works as well
        //numbers.push(numbers.length + 1);
        //numbers = numbers;
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	09. Add a number
</button>