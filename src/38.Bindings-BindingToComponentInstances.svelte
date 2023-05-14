<script>
	import InputField from './38.InputField.svelte';

	let field;
</script>

<h1>38. Bindings / Bindings to Component Instances </h1>

<div>
    <InputField bind:this={field}/>
    <button on:click={() => field.focus()}>Focus field</button>
</div>

<style>
	div { display: flex; }
</style>