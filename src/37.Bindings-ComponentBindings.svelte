<script>
	import Keypad from './37.Keypad.svelte';

	let pin;
	$: view = pin ? pin.replace(/\d(?!$)/g, '•') : 'enter your pin'; // '\d' matches any digit character (0-9). '(?!$)'' is a negative lookahead assertion that ensures the matched digit is not at the end of the string.

	function handleSubmit() {
		alert(`submitted ${pin}`);
	}
</script>

<h1>37. Bindings / Component Bindings </h1>

<h1 style="color: {pin ? '#333' : '#ccc'}">{view}</h1>

<Keypad bind:value={pin} on:submit={handleSubmit}/>