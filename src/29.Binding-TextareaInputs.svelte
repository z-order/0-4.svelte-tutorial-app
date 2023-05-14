<script>
	import { marked } from 'marked';
	let value = `Some words are *italic*, some are **bold**`;
</script>

<h1>29. Bindings / Textarea Inputs</h1>

{@html marked(value)}

<label>
    <pre><code>&lt;textarea bind:value=&#123;value&#125;&gt;&lt;/textarea&gt;</code></pre>
    <textarea bind:value={value}></textarea>
</label>

<label>
    <pre><code>&lt;textarea bind:value&gt;&lt;/textarea&gt;</code></pre>
    <textarea bind:value></textarea>
    </label>
<style>
	textarea { width: 100%; height: 200px; }
</style>