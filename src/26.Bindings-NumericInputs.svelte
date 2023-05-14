<script>
	let a = 1;
	let b = 2;
</script>

<h1>26. input type=number, input type=range</h1>

<label>
	<input type=number bind:value={a} min=0 max=10>
	<input type=range bind:value={a} min=0 max=10>
</label>

<label>
	<input type=number bind:value={b} min=0 max=10>
	<input type=range bind:value={b} min=0 max=10>
</label>

<p>{a} + {b} = {a + b}</p>

<style>
	label { display: flex }
	input, p { margin: 6px }
</style>