# The way of how to create project, install, and test.

```sh
[~]$ npm init vite

✔ Project name: … 0-4.svelte-tutorial-app
✔ Select a framework: › Svelte
✔ Select a variant: › TypeScript

Scaffolding project in /home/.../0-4.svelte-tutorial-app...

Done. Now run:

  cd 0-4.svelte-tutorial-app
  npm install
  npm run dev
```
<br>

# You can use start-app.sh to start the app in a deployed server system.

```sh
#/bin/sh

# In a deploy server, and serve command can be installed using "npm install -g serve"

serve -n -s -l 3000 dist
```

or for debug mode logging

```sh
#/bin/sh

# In a deploy server, and serve command can be installed using "npm install -g serve"

serve -n -s -l 3000 dist --debug

```

<br>

# src/App.svelte

```html
<script>

	import T01_HelloWrold from './01.HelloWorld.svelte'
	import T02_Introduction_AddingData from './02.Introduction-AddingData.svelte'
	import T03_Introduction_DynamicAttributes from './03.Introduction-DynamicAttributes.svelte'
	import T04_Introduction_Styling from './04.Introduction-Styling.svelte'
	import T05_Introduction_NestedComponents from './05.Introduction-NestedComponents.svelte'
	import T06_Reactivity_Assignments from './06.Reactivity-Assignments.svelte'
	import T07_Reactivity_Declarations from './07.Reactivity-Declarations.svelte'
	import T08_Reactivity_Statements from './08.Reactivity-Statements.svelte'
	import T09_Reactivity_UpdatingArraysAndObjects from './09.Reativity-UpdatingArraysAndObjects.svelte'
	import T10_Props_DeclaringProps from './10.Props-DeclaringProps.svelte'
	import T11_Props_DefaultValues from './11.Props-DefaultValues.svelte'
	import T12_Props_SpreadProps from './12.Props-SpreadProps.svelte'
	import T13_Logic_IfBlocks from './13.Logic-IfBlocks.svelte'
	import T14_Logic_ElseBlocks from './14.Logic-ElseBlocks.svelte'
	import T15_Logic_ElseIfBlocks from './15.Logic-ElseIfBlocks.svelte'
	import T16_Logic_EachBlocks from './16.Logic-EachBlocks.svelte'
	import T17_Logic_KeyedEachBlocks from './17.Logic-KeyedEachBlocks.svelte'
	import T18_Logic_AwaitBlocks from './18.Logic-AwaitBlocks.svelte'
	import T19_Events_DOMEvents from './19.Events-DOMEvents.svelte'
	import T20_Events_InlineHandlers from './20.Events-InlineHandlers.svelte'
	import T21_Events_EventsModifiers from './21.Events-EventsModifiers.svelte'
	import T22_Events_ComponentEvents from './22.Events-ComponentEvents.svelte'
	import T23_Events_EventForwarding from './23.Events-EventForwarding.svelte'
	import T24_Events_DOMEventForwarding from './24.Events-DOMEventForwarding.svelte'
	import T25_Bindings_TextInputs from './25.Bindings-TextInputs.svelte'
	import T26_Bindings_NumericInputs from './26.Bindings-NumericInputs.svelte'
	import T27_Bindings_CheckboxInputs from './27.Bindings-CheckboxInputs.svelte'
	import T28_Bindings_GroupInputs from './28.Bindings-GroupInputs.svelte'
	import T29_Bindings_TextareaInputs from './29.Binding-TextareaInputs.svelte'
	import T30_Bindings_SelectBindings from './30.Bindings-SelectBindings.svelte'
	import T31_Bindings_SelectMultiple from './31.Bindings-SelectMultiple.svelte'
	import T32_Bindings_ContenteditableBindings from './32.Bindings-ContenteditableBindings.svelte'
	import T33_Bindings_EachBlockBindings from './33.Bindings-EachBlockBindings.svelte'
	import T34_Bindings_MediaElements from './34.Bindings-MediaElements.svelte'
	import T35_Bindings_Demensions from './35.Bindings-Demensions.svelte'
	import T36_Bindings_This from './36.Bindings-This.svelte'
	import T37_Bindings_ComponentBindings from './37.Bindings-ComponentBindings.svelte'
	import T38_Bindings_BindingToComponentInstances from './38.Bindings-BindingToComponentInstances.svelte'

</script>

<T01_HelloWrold/>
<T02_Introduction_AddingData/>
<T03_Introduction_DynamicAttributes/>
<T04_Introduction_Styling/>
<T05_Introduction_NestedComponents/>
<T06_Reactivity_Assignments/><p></p>
<T07_Reactivity_Declarations/>
<T08_Reactivity_Statements/>
<T09_Reactivity_UpdatingArraysAndObjects/>
<T10_Props_DeclaringProps/>
<T11_Props_DefaultValues/>
<T12_Props_SpreadProps/>
<T13_Logic_IfBlocks/><p></p>
<T14_Logic_ElseBlocks/>
<T15_Logic_ElseIfBlocks/>
<T16_Logic_EachBlocks/>
<T17_Logic_KeyedEachBlocks/>
<T18_Logic_AwaitBlocks/>
<T19_Events_DOMEvents/>
<T20_Events_InlineHandlers/>
<T21_Events_EventsModifiers/>
<T22_Events_ComponentEvents/>
<T23_Events_EventForwarding/>
<T24_Events_DOMEventForwarding/><p></p>
<T25_Bindings_TextInputs/>
<T26_Bindings_NumericInputs/>
<T27_Bindings_CheckboxInputs/>
<T28_Bindings_GroupInputs/>
<T29_Bindings_TextareaInputs/>
<T30_Bindings_SelectBindings/>
<T31_Bindings_SelectMultiple/>
<T32_Bindings_ContenteditableBindings/>
<T33_Bindings_EachBlockBindings/>
<T34_Bindings_MediaElements/>
<T35_Bindings_Demensions/>
<T36_Bindings_This/>
<T37_Bindings_ComponentBindings/>
<T38_Bindings_BindingToComponentInstances/>
```

<br>

## 01.HelloWorld.svelte

Refs: [https://svelte.dev/tutorial/basics](https://svelte.dev/tutorial/basics)

```html
<script>
	let name = 'world';
</script>

<h1>Hello {name}!</h1>
```

<br>

## 02.Introduction-AddingData.svelte

Refs: [https://svelte.dev/tutorial/adding-data](https://svelte.dev/tutorial/adding-data)

```html
<script>
	let name = 'world';
</script>

<h1>02. Hello {name.toUpperCase()}!</h1>
```

<br>

## 03.Introduction-DynamicAttributes.svelte

Refs: [https://svelte.dev/tutorial/dynamic-attributes](https://svelte.dev/tutorial/dynamic-attributes)

```html
<script>
    let src = '/tutorial/rickroll-roll.gif';
    let name = 'Rick Astley';
</script>

<img src={src} alt="03-1. {name} dances.">
<img {src} alt="03-2. {name} dances.">
```

<br>

## 04.Introduction-Styling.svelte

Refs: [https://svelte.dev/tutorial/styling](https://svelte.dev/tutorial/styling)

```html
<p>04. This is a paragraph.</p>

<style>
	/* Write your CSS here */
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}    
</style>
```

<br>

## 05.Introduction-NestedComponents.svelte

Refs: [https://svelte.dev/tutorial/nested-components](https://svelte.dev/tutorial/nested-components)

```html
<script>
	import Nested from './05.Nested.svelte';
</script>

<p>05. This is a paragraph.</p>
<Nested/>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>
```
## 05.Nested.svelte

```html
<p>05. This is another paragraph in 05.Nested.svelte.</p>
```

<br>

## Introduction / Making an app

Refs: [https://svelte.dev/tutorial/making-an-app](https://svelte.dev/tutorial/making-an-app)

This tutorial is designed to get you familiar with the process of writing components. But at some point, you'll want to start writing components in the comfort of your own text editor.

First, you'll need to integrate Svelte with a build tool. We recommend using [SvelteKit](https://kit.svelte.dev), which sets up [Vite](https://vitejs.dev/) with [vite-plugin-svelte](https://github.com/sveltejs/vite-plugin-svelte/) for you...

```bash
npm create svelte@latest myapp
```

There are also a number of [community-maintained integrations](https://sveltesociety.dev/tools).

Don't worry if you're relatively new to web development and haven't used these tools before. We've prepared a simple step-by-step guide, [Svelte for new developers](/blog/svelte-for-new-developers), which walks you through the process.

You'll also want to configure your text editor. There are [plugins](https://sveltesociety.dev/tools#editor-support) for many popular editors as well as an official [VS Code extension](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

<!-- 
NOTE: Removed until we have better place for setting-up-your-editor guide. See https://github.com/sveltejs/svelte/pull/7310#issuecomment-1049923609
If your editor does not have a Svelte plugin then you can follow [this guide](/blog/setting-up-your-editor) to configure your text editor to treat `.svelte` files the same as `.html` for the sake of syntax highlighting. -->

Then, once you've got your project set up, using Svelte components is easy. The compiler turns each component into a regular JavaScript class — just import it and instantiate with `new`:

```js
import App from './App.svelte';

const app = new App({
	target: document.body,
	props: {
		// we'll learn about props later
		answer: 42
	}
});
```

You can then interact with `app` using the [component API](/docs#run-time-client-side-component-api) if you need to.

<br>

## 06.Reactivity-Assignments.svelte

Refs: [https://svelte.dev/tutorial/reactive-assignments](https://svelte.dev/tutorial/reactive-assignments)

```html
<script>
	let count = 0;

	function incrementCount() {
		count += 1;
	}
</script>

<button on:click={incrementCount}>
	06. Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
```

<br>

## 07.Reactivity-Declarations.svelte

Refs: [https://svelte.dev/tutorial/reactive-declarations](https://svelte.dev/tutorial/reactive-declarations)

```html
<script>
	let count = 0;
	$: doubled = count * 2;

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	07. Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {doubled}</p>
```

<br>

## 08.Reactivity-Statements.svelte

Refs: [https://svelte.dev/tutorial/reactive-statements](https://svelte.dev/tutorial/reactive-statements)

```html
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
```

<br>

## 09.Reativity-UpdatingArraysAndObjects.svelte

Refs: [https://svelte.dev/tutorial/updating-arrays-and-objects](https://svelte.dev/tutorial/updating-arrays-and-objects)

```html
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
```

<br>

## 10.Props-DeclaringProps.svelte

Refs: [https://svelte.dev/tutorial/declaring-props](https://svelte.dev/tutorial/declaring-props)

```html
<script>
	import Nested from './10.Nested.svelte';
</script>

<Nested answer={42}/>
```

## 10.Nested.svelte

```html
<script>
	export let answer;
</script>

<p>10. The answer is {answer}</p>
```

<br>

## 11.Props-DefaultValues.svelte

Refs: [https://svelte.dev/tutorial/default-values](https://svelte.dev/tutorial/default-values)

```html
<script>
	import Nested from './11.Nested.svelte';
</script>

<Nested answer={'42'}/>
<Nested/>
```

## 11.Nested.svelte

```html
<script>
	export let answer = 'a mystery';
</script>

<p>11. The answer is {answer}</p>
```

<br>

## 12.Props-SpreadProps.svelte

Refs: [https://svelte.dev/tutorial/spread-props](https://svelte.dev/tutorial/spread-props)

```html
<script>
	import Info from './12.Info.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<!-- Use this -->
<Info {...pkg}/>

<!-- Instead of using below
<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
-->
```

## 12.Info.svelte

```html
<script>
	export let name;
	export let version;
	export let speed;
	export let website;
</script>

<p>
	12. The <code>{name}</code> package is {speed} fast.
	Download version {version} from <a href="https://www.npmjs.com/package/{name}">npm</a>
	and <a href={website}>learn more here</a>
</p>
```

<br>

## 13.Logic-IfBlocks.svelte

Refs: [https://svelte.dev/tutorial/if-blocks](https://svelte.dev/tutorial/if-blocks)

```html
<script>
	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

{#if user.loggedIn}
	<button on:click={toggle}>
		13. Log out
	</button>
{/if}

{#if !user.loggedIn}
	<button on:click={toggle}>
		13. Log in
	</button>
{/if}
```

<br>

## 14.Logic-ElseBlocks.svelte

Refs: [https://svelte.dev/tutorial/else-blocks](https://svelte.dev/tutorial/else-blocks)

```html
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
```

<br>

## 15.Logic-ElseIfBlocks.svelte

Refs: [https://svelte.dev/tutorial/else-if-blocks](https://svelte.dev/tutorial/else-if-blocks)

```html
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
```

<br>

## 16.Logic-EachBlocks.svelte

Refs: [https://svelte.dev/tutorial/each-blocks](https://svelte.dev/tutorial/each-blocks)

```html
<script>
	let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];
</script>

<h1>16-1. The Famous Cats of YouTube</h1>

<ul>
	{#each cats as cat}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={cat.id}" rel="noreferrer">
			{cat.name}
		</a></li>
	{/each}
</ul>

<h1>16-2. The Famous Cats of YouTube</h1>

<ul>
	{#each cats as { id, name }, i}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={id}" rel="noreferrer">
			{i + 1}: {name}
		</a></li>
	{/each}
</ul>
```

<br>

## 17.Logic-KeyedEachBlocks.svelte

Refs: [https://svelte.dev/tutorial/keyed-each-blocks](https://svelte.dev/tutorial/keyed-each-blocks)

```html
<script>
	import Thing from './17.Thing.svelte';

	let things = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' },
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<button on:click={handleClick}>
	17. Remove first thing
</button>

{#each things as thing (thing.id) }
	<Thing name={thing.name}/>
{/each}
```

## 17.Thing.svelte

```html
<script>
	import { onDestroy } from 'svelte';

	const emojis = {
        apple: "🍎",
        banana: "🍌",
        carrot: "🥕",
        doughnut: "🍩",
        egg: "🥚"
	}

	// the name is updated whenever the prop value changes...
	export let name;

	// ...but the "emoji" variable is fixed upon initialisation of the component
	const emoji = emojis[name];

	// observe in the console which entry is removed
	onDestroy(() => {
		console.log('thing destroyed: ' + name)
	});
</script>

<p>
	<span>The emoji for { name } is { emoji }</span>
</p>

<style>
	p {
		margin: 0.8em 0;
	}
	span {
		display: inline-block;
		padding: 0.2em 1em 0.3em;
		text-align: center;
		border-radius: 0.2em;
		background-color: #24285f;
	}
</style>
```

<br>

## 18.Logic-AwaitBlocks.svelte

Refs: [https://svelte.dev/tutorial/await-blocks](https://svelte.dev/tutorial/await-blocks)

```html
<script>
	async function getRandomNumber() {
        const res = await fetch(`https://svelte.dev/tutorial/random-number`);
        console.log(res);
		const text = await res.text();
        console.log(text);

		if (res.ok) {
			return text;
		} else {
			throw new Error(text);
		}
	}
	
	let promise = getRandomNumber();

	function handleClick() {
		promise = getRandomNumber();
	}
</script>

<button on:click={handleClick}>
	generate random number
</button>

{#await promise}
	<p>...waiting</p>
{:then number}
	<p>The number is {number}</p>
{:catch error}
	<p style="color: red">{error.message}</p>
{/await}
```

<br>

## 19.Events-DOMEvents.svelte

Refs: [https://svelte.dev/tutorial/dom-events](https://svelte.dev/tutorial/dom-events)

```html
<script>
	let m = { x: 0, y: 0 };

	function handleMousemove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}
</script>

<div on:mousemove={handleMousemove}>
	19. The mouse position is {m.x} x {m.y}
</div>

<style>
	div { width: 100%; height: 100%; }
</style>
```

<br>

## 20.Events-InlineHandlers.svelte

Refs: [https://svelte.dev/tutorial/inline-handlers](https://svelte.dev/tutorial/inline-handlers)

```html
<script>
	let m = { x: 0, y: 0 };
</script>

<div on:mousemove="{e => m = { x: e.clientX, y: e.clientY }}">
	20. The mouse position is {m.x} x {m.y}
</div>

<style>
	div { width: 100%; height: 100%; }
</style>
```

<br>

## 21.Events-EventsModifiers.svelte

Refs: [https://svelte.dev/tutorial/event-modifiers](https://svelte.dev/tutorial/event-modifiers)

DOM event handlers can have *modifiers* that alter their behaviour. For example, a handler with a `once` modifier will only run a single time:

```html
<script>
	function handleClick() {
		alert('no more alerts')
	}
</script>

<button on:click|once={handleClick}>
	21. Click me
</button>
```

The full list of modifiers:

* `preventDefault` — calls `event.preventDefault()` before running the handler. Useful for client-side form handling, for example.
* `stopPropagation` — calls `event.stopPropagation()`, preventing the event reaching the next element
* `passive` — improves scrolling performance on touch/wheel events (Svelte will add it automatically where it's safe to do so)
* `nonpassive` — explicitly set `passive: false`
* `capture` — fires the handler during the *capture* phase instead of the *bubbling* phase ([MDN docs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#Event_bubbling_and_capture))
* `once` — remove the handler after the first time it runs
* `self` — only trigger handler if event.target is the element itself
* `trusted` — only trigger handler if `event.isTrusted` is `true`. I.e. if the event is triggered by a user action.

You can chain modifiers together, e.g. `on:click|once|capture={...}`.

<br>

## 22.Events-ComponentEvents.svelte

Refs: [https://svelte.dev/tutorial/component-events](https://svelte.dev/tutorial/component-events)

```html
<script>
	import Inner from './22.Inner.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}
</script>

<Inner on:message={handleMessage}/>
```

## 22.Inner.svelte

```html
<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function sayHello() {
		dispatch('message', {
			text: 'Hello!'
		});
	}
</script>

<button on:click={sayHello}>
	22. Click to say hello
</button>
```

<br>

## 23.Events-EventForwarding.svelte

Refs: [https://svelte.dev/tutorial/event-forwarding](https://svelte.dev/tutorial/event-forwarding)

```html
<script>
	import Outer from './23.Outer.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}
</script>

<Outer on:message={handleMessage}/>
```

## 23.Outer.svelte

```html
<script>
	import Inner from './23.Inner.svelte';
</script>

<Inner on:message/>
```

## 23.Inner.svelte

```html
<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function sayHello() {
		dispatch('message', {
			text: 'Hello!'
		});
	}
</script>

<button on:click={sayHello}>
	23. Click to say hello
</button>
```

<br>

---
`Event forwarding`
---

Unlike DOM events, component events don't *bubble*. If you want to listen to an event on some deeply nested component, the intermediate components must *forward* the event.

In this case, we have the same `App.svelte` and `Inner.svelte` as in the [previous chapter](/tutorial/component-events), but there's now an `Outer.svelte` component that contains `<Inner/>`.

One way we could solve the problem is adding `createEventDispatcher` to `Outer.svelte`, listening for the `message` event, and creating a handler for it:

```html
<script>
	import Inner from './Inner.svelte';
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	function forward(event) {
		dispatch('message', event.detail);
	}
</script>

<Inner on:message={forward}/>
```

But that's a lot of code to write, so Svelte gives us an equivalent shorthand — an `on:message` event directive without a value means 'forward all `message` events'.

```html
<script>
	import Inner from './Inner.svelte';
</script>

<Inner on:message/>
```

<br>

## 24.Events-DOMEventForwarding.svelte

Refs: [https://svelte.dev/tutorial/dom-event-forwarding](https://svelte.dev/tutorial/dom-event-forwarding)

```html
<script>
	import CustomButton from './24.CustomButton.svelte';

	function handleClick() {
		alert('Button Clicked');
	}
</script>

<CustomButton on:click={handleClick}/>
```

## 24.CustomButton.svelte

```html
<button on:click>
	24. Click me
</button>

<style>
	button {
		background: #E2E8F0;
		color: #64748B;
		border: unset;
		border-radius: 6px;
		padding: .75rem 1.5rem;
		cursor: pointer;
	}
	button:hover {
		background: #CBD5E1;
		color: #475569;
	}
	button:focus {
		background: #94A3B8;
		color: #F1F5F9;
	}
</style>
```

<br>

---
DOM event forwarding
---

Event forwarding works for DOM events too.

We want to get notified of clicks on our `<CustomButton>` — to do that, we just need to forward `click` events on the `<button>` element in `CustomButton.svelte`:

```html
<button on:click>
	Click me
</button>
```

<br>

## 25.Bindings-TextInputs.svelte

Refs: [https://svelte.dev/tutorial/text-inputs](https://svelte.dev/tutorial/text-inputs)

```html
<script>
	let name = 'world';
</script>

<input bind:value={name}> 

<h1>25. Hello {name}!</h1>
```

<br>

## 26.Bindings-NumericInputs.svelte

Refs: [https://svelte.dev/tutorial/numeric-inputs](https://svelte.dev/tutorial/numeric-inputs)

```html
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
```

<br>

## 27.Bindings-CheckboxInputs.svelte

Refs: [https://svelte.dev/tutorial/checkbox-inputs](https://svelte.dev/tutorial/checkbox-inputs)

```html
<script>
	let yes = false;
</script>

<h1> 27. Binding - Checkbox Inputs</h1>

<label>
	<input type=checkbox bind:checked={yes}>
	Yes! Send me regular email spam
</label>

{#if yes}
	<p>Thank you. We will bombard your inbox and sell your personal details.</p>
{:else}
	<p>You must opt-in to continue. If you're not paying, you're the product.</p>
{/if}

<button disabled={!yes}>
	Subscribe
</button>
```

<br>

## 28.Bindings-GroupInputs.svelte

Refs: [https://svelte.dev/tutorial/group-inputs](https://svelte.dev/tutorial/group-inputs)

```html
<script>
	let scoops = 1;
	let flavours = ['Mint choc chip'];

	let menu = [
		'Cookies and cream',
		'Mint choc chip',
		'Raspberry ripple'
	];

	function join(flavours) {
		if (flavours.length === 1) return flavours[0];
		return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
	}
</script>

<h1>28. Bindings / Group Inputs</h1>

<h2>Size</h2>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={1}>
	One scoop
</label>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={2}>
	Two scoops
</label>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={3}>
	Three scoops
</label>

<h2>Flavours</h2>

{#each menu as flavour}
	<label>
		<input type=checkbox bind:group={flavours} name="flavours" value={flavour}>
		{flavour}
	</label>
{/each}

{#if flavours.length === 0}
	<p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
	<p>Can't order more flavours than scoops!</p>
{:else}
	<p>
		You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
		of {join(flavours)}
	</p>
{/if}
```

<br>

## 29.Binding-TextareaInputs.svelte

Refs: [https://svelte.dev/tutorial/textarea-inputs](https://svelte.dev/tutorial/textarea-inputs)

```html
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
```

<br>

## 30.Bindings-SelectBindings.svelte

Refs: [https://svelte.dev/tutorial/select-bindings](https://svelte.dev/tutorial/select-bindings)

```html
<script>
	let questions = [
		{ id: 1, text: `Where did you go to school?` },
		{ id: 2, text: `What is your mother's name?` },
		{ id: 3, text: `What is another personal fact that an attacker could easily find with Google?` }
	];

	let selected;

	let answer = '';

	function handleSubmit() {
		alert(`answered question ${selected.id} (${selected.text}) with "${answer}"`);
	}
</script>

<h1>30. Bindings / Select Bindings</h1>

<h2>Insecurity questions</h2>

<form on:submit|preventDefault={handleSubmit}>
	<select bind:value={selected} on:change="{() => answer = ''}">
		{#each questions as question}
			<option value={question}>
				{question.text}
			</option>
		{/each}
	</select>

	<input bind:value={answer}>

	<button disabled={!answer} type=submit>
		Submit
	</button>
</form>

<p>selected question {selected ? selected.id : '[waiting...]'}</p>

<style>
	input {
		display: block;
		width: 500px;
		max-width: 100%;
	}
</style>
```

<br>

Note that the `<option>` values are objects rather than strings. Svelte doesn't mind.

> Because we haven't set an initial value of `selected`, the binding will set it to the default value (the first in the list) automatically. Be careful though — until the binding is initialised, `selected` remains undefined, so we can't blindly reference e.g. `selected.id` in the template. If your use case allows it, you could also set an initial value to bypass this problem.

<br>

Now, let's understand the purpose of `preventDefault`:

The `preventDefault` modifier is used to prevent the default behavior of an event from occurring. In this case, when the form is submitted, the default behavior is for the browser to reload the page. By using `preventDefault`, we are instructing the browser not to perform the default behavior.

In the given code, when the form is submitted, the `handleSubmit` function will be called, but the default behavior of the form submission (i.e., page reload) will be prevented. This allows you to handle the form submission in a custom way using the `handleSubmit` function without the page being reloaded.

By using `preventDefault`, you have the flexibility to perform additional operations, such as making an asynchronous request, validating the form, or updating the UI, before taking any action like page navigation or reloading.

It's a common pattern to use `preventDefault` in form submissions to customize the behavior and perform additional actions using JavaScript before allowing the default form submission behavior to occur.


<br>

## 31.Bindings-SelectMultiple.svelte

Refs: [https://svelte.dev/tutorial/multiple-select-bindings](https://svelte.dev/tutorial/multiple-select-bindings)

```html
<script>
	let scoops = 1;
	let flavours = ['Mint choc chip'];

	let menu = [
		'Cookies and cream',
		'Mint choc chip',
		'Raspberry ripple'
	];

	function join(flavours) {
		if (flavours.length === 1) return flavours[0];
		return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
	}
</script>

<h1>31. Bindings / Select Multiple</h1>

<h2>Size</h2>

<label>
	<input type=radio bind:group={scoops} value={1}>
	One scoop
</label>

<label>
	<input type=radio bind:group={scoops} value={2}>
	Two scoops
</label>

<label>
	<input type=radio bind:group={scoops} value={3}>
	Three scoops
</label>

<h2>Flavours</h2>

<select multiple bind:value={flavours}>
	{#each menu as flavour}
		<option value={flavour}>
			{flavour}
		</option>
	{/each}
</select>

{#if flavours.length === 0}
	<p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
	<p>Can't order more flavours than scoops!</p>
{:else}
	<p>
		You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
		of {join(flavours)}
	</p>
{/if}
```

<br>

## 32.Bindings-ContenteditableBindings.svelte

Refs: [https://svelte.dev/tutorial/contenteditable-bindings](https://svelte.dev/tutorial/contenteditable-bindings)

```html
<script>
	let html = '<p>Write some text!</p>';
</script>

<h1>32. Bindings / Contenteditable Bindings</h1>

<div
	contenteditable="true"
	bind:innerHTML={html}
></div>

<pre>{html}</pre>

<style>
	[contenteditable] {
		padding: 0.5em;
		border: 1px solid #eee;
		border-radius: 4px;
	}
</style>
```

<br>

Elements with the `contenteditable` attribute support the following bindings:
- [`innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)
- [`innerText`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText)
- [`textContent`](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent)

There are slight differences between each of these, read more about them [here](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent#Differences_from_innerText).

```html
<div
	contenteditable="true"
	bind:innerHTML={html}
></div>
```

<br>

## 33.Bindings-EachBlockBindings.svelte

Refs: [https://svelte.dev/tutorial/each-block-bindings](https://svelte.dev/tutorial/each-block-bindings)

```html
<script>
	let todos = [
		{ done: false, text: 'finish Svelte tutorial' },
		{ done: false, text: 'build an app' },
		{ done: false, text: 'world domination' }
	];

	function add() {
		todos = todos.concat({ done: false, text: '' });
	}

	function clear() {
		todos = todos.filter(t => !t.done);
	}

	$: remaining = todos.filter(t => !t.done).length;
</script>

<h1>33. Bindings / Each Block Bindings</h1>

<h1>Todos</h1>

{#each todos as todo}
	<div class:done={todo.done}>
		<input
			type=checkbox
			bind:checked={todo.done}
		>

		<input
			placeholder="What needs to be done?"
			bind:value={todo.text}
		>
	</div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add}>
	Add new
</button>

<button on:click={clear}>
	Clear completed
</button>

<style>
	.done {
		opacity: 0.4;
	}
</style>
```

<br>


In the given code, `class:done={todo.done}` is a Svelte syntax used to conditionally apply a CSS class based on the value of `todo.done`. Let's break it down:

```html
{#each todos as todo}
	<div class:done={todo.done}>
		<!-- Inputs and other elements -->
	</div>
{/each}
```

- `{#each todos as todo}` is a Svelte block directive that iterates over the `todos` array and assigns each element to the variable `todo` within the block.
- `<div class:done={todo.done}>` is a `<div>` element with a dynamic class binding. The class name `done` is conditionally applied based on the value of `todo.done`.

Here's what class:done={todo.done} means:

- `class:` is a special syntax in Svelte used for class bindings.
- `done` is the name of the CSS class.
- `=` is the assignment operator.
- `{todo.done}` is the expression that determines whether the class should be applied or not. If `todo.done` evaluates to a truthy value (e.g., `true`), the class `done` will be added to the element. If `todo.done` evaluates to a falsy value (e.g., `false`), the class will not be added.

In the context of a to-do list, this code allows the class `done` to be applied dynamically to the `<div>` element when the `todo` is marked as done. This class can then be used to style the completed to-do items differently from the incomplete ones, providing visual feedback to the user.

You can define CSS rules for the `done` class to change the appearance of the associated elements, such as adding a strike-through effect or changing the color, to indicate completed tasks.

<br>

## 34.Bindings-MediaElements.svelte

Refs: [https://svelte.dev/tutorial/media-elements](https://svelte.dev/tutorial/media-elements)

```html
<script>
	// These values are bound to properties of the video
	let time = 0;
	let duration;
	let paused = true;

	let showControls = true;
	let showControlsTimeout;

	// Used to track time of last mouse down event
	let lastMouseDown;

	function handleMove(e) {
		// Make the controls visible, but fade out after
		// 2.5 seconds of inactivity
		clearTimeout(showControlsTimeout);
		showControlsTimeout = setTimeout(() => showControls = false, 2500);
		showControls = true;

		if (!duration) return; // video not loaded yet
		if (e.type !== 'touchmove' && !(e.buttons & 1)) return; // mouse not down

		const clientX = e.type === 'touchmove' ? e.touches[0].clientX : e.clientX;
		const { left, right } = this.getBoundingClientRect();
		time = duration * (clientX - left) / (right - left);
	}

	// we can't rely on the built-in click event, because it fires
	// after a drag — we have to listen for clicks ourselves
	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		// @ts-ignore
		if (new Date() - lastMouseDown < 300) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

	function format(seconds) {
		if (isNaN(seconds)) return '...';

		const minutes = Math.floor(seconds / 60);
		seconds = Math.floor(seconds % 60);
		if (seconds < 10) seconds = '0' + seconds;

		return `${minutes}:${seconds}`;
	}
</script>

<h1>34. Bindings / Media Elements</h1>
<h2>Caminandes: Llamigos</h2>
<p>From <a href="https://studio.blender.org/films">Blender Studio</a>. CC-BY</p>

<div>
	<video
		poster="https://sveltejs.github.io/assets/caminandes-llamigos.jpg"
		src="https://sveltejs.github.io/assets/caminandes-llamigos.mp4"
		on:mousemove={handleMove}
		on:touchmove|preventDefault={handleMove}
		on:mousedown={handleMousedown}
		on:mouseup={handleMouseup}
		bind:currentTime={time}
		bind:duration
		bind:paused>
		<track kind="captions">
	</video>

	<div class="controls" style="opacity: {duration && showControls ? 1 : 0}">
		<progress value="{(time / duration) || 0}"/>

		<div class="info">
			<span class="time">{format(time)}</span>
			<span>click anywhere to {paused ? 'play' : 'pause'} / drag to seek</span>
			<span class="time">{format(duration)}</span>
		</div>
	</div>
</div>

<style>
	div {
		position: relative;
	}

	.controls {
		position: absolute;
		top: 0;
		width: 100%;
		transition: opacity 1s;
	}

	.info {
		display: flex;
		width: 100%;
		justify-content: space-between;
	}

	span {
		padding: 0.2em 0.5em;
		color: white;
		text-shadow: 0 0 8px black;
		font-size: 1.4em;
		opacity: 0.7;
	}

	.time {
		width: 3em;
	}

	.time:last-child { text-align: right }

	progress {
		display: block;
		width: 100%;
		height: 10px;
		-webkit-appearance: none;
		appearance: none;
	}

	progress::-webkit-progress-bar {
		background-color: rgba(0,0,0,0.2);
	}

	progress::-webkit-progress-value {
		background-color: rgba(255,255,255,0.6);
	}

	video {
		width: 100%;
	}
</style>
```

<br>

## 35.Bindings-Demensions.svelte

Refs: [https://svelte.dev/tutorial/dimensions](https://svelte.dev/tutorial/dimensions)

```html
<script>
	let w;
	let h;
	let size = 42;
	let text = 'edit me';
</script>

<h1>35. Bindings / Demensions</h1>

<input type=range bind:value={size}>
<input bind:value={text}>

<p>size: {w}px x {h}px</p>

<div bind:clientWidth={w} bind:clientHeight={h}>
	<span style="font-size: {size}px">{text}</span>
</div>

<style>
	input { display: block; }
	div { display: inline-block; }
	span { word-break: break-all; }
</style>
```

<br>

Every block-level element has `clientWidth`, `clientHeight`, `offsetWidth` and `offsetHeight` bindings:

```html
<div bind:clientWidth={w} bind:clientHeight={h}>
	<span style="font-size: {size}px">{text}</span>
</div>
```

These bindings are readonly — changing the values of `w` and `h` won't have any effect.

> Elements are measured using a technique similar to [this one](http://www.backalleycoder.com/2013/03/18/cross-browser-event-based-element-resize-detection/). There is some overhead involved, so it's not recommended to use this for large numbers of elements.
>
> `display: inline` elements cannot be measured with this approach; nor can elements that can't contain other elements (such as `<canvas>`). In these cases you will need to measure a wrapper element instead.


<br>

## 36.Bindings-This.svelte

Refs: [https://svelte.dev/tutorial/bind-this](https://svelte.dev/tutorial/bind-this)

```html
<script>
	import { onMount } from 'svelte';

	let canvas;

	onMount(() => {
		const ctx = canvas.getContext('2d');
		let frame = requestAnimationFrame(loop);

		function loop(t) { // t variable represents the current timestamp passed to the requestAnimationFrame callback (start from 0 in ms unit).
			frame = requestAnimationFrame(loop);

			const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);

			for (let p = 0; p < imageData.data.length; p += 4) { // 4 bytes : R + G + B + Alpha
				const i = p / 4; // pixel index
				const x = i % canvas.width; // x coordination of the current p position of the pixel
				const y = i / canvas.width >>> 0; // y coordination of the current p position of the pixel

				const r = 64 + (128 * x / canvas.width) + (64 * Math.sin(t / 1000)); // Math.sin(t / 1000): Spanning from -1 to 1 for a cycle of a sign curve during 6 seconds
				const g = 64 + (128 * y / canvas.height) + (64 * Math.cos(t / 1000)); // Math.cos(t / 1000): The 90-degree phase with a difference value of 0.5 against sin() function.
				const b = 128;

				imageData.data[p + 0] = r;
				imageData.data[p + 1] = g;
				imageData.data[p + 2] = b;
				imageData.data[p + 3] = 255;
			}

			ctx.putImageData(imageData, 0, 0);
		}

		return () => {
			cancelAnimationFrame(frame);
		};
	});
</script>

<h1>36. Bindings / This </h1>

<canvas
	bind:this={canvas}
	width={32}
	height={32}
></canvas>

<style>
	canvas {
		width: 100%;
		height: 100%;
		background-color: #666;
		-webkit-mask: url(/svelte-logo-mask.svg) 50% 50% no-repeat;
		mask: url(/svelte-logo-mask.svg) 50% 50% no-repeat;
	}
</style>
```

<br>

In the given code, the `t` variable in the `loop(t)` function represents the current timestamp passed to the `requestAnimationFrame` callback.

Here's an explanation of its usage:

1. The `loop(t)` function is a callback function passed to `requestAnimationFrame`, which is a method that schedules a function to be executed before the next repaint of the browser. This creates a loop that continuously updates the canvas animation.
2. When the `requestAnimationFrame` callback is invoked, it passes the current timestamp as an argument to the callback function. This timestamp represents the time elapsed since the document started running, typically in milliseconds.
3. The `t` parameter in the `loop(t)` function serves as a reference to this timestamp value. It allows you to use the current timestamp to create dynamic and time-based animations or effects.

In the provided code, the `t` variable is used in calculations to generate dynamic color values for the pixels in the canvas animation. The `t` value is divided by 1000 and used with `Math.sin` and `Math.cos` functions to create smooth color transitions over time.

For example, `const r = 64 + (128 * x / canvas.width) + (64 * Math.sin(t / 1000));` calculates the red component of the pixel color based on the position x and the time `t`.

By using the current timestamp (`t`), you can create time-based animations that change dynamically over time, allowing for smooth transitions and effects in the canvas animation.

Note: The `t` variable itself is not predefined. It is automatically passed as an argument by the `requestAnimationFrame` method when invoking the `loop` callback function.


<br>

## 37.Bindings-ComponentBindings.svelte

Refs: [https://svelte.dev/tutorial/component-bindings](https://svelte.dev/tutorial/component-bindings)

```html
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
```

Use component bindings sparingly. It can be difficult to track the flow of data around your application if you have too many of them, especially if there is no 'single source of truth'.

## 37.Keypad.svelte

```html
<script>
	import { createEventDispatcher } from 'svelte';

	export let value = '';

	const dispatch = createEventDispatcher();

	const select = num => () => value += num;
	const clear  = () => value = '';
	const submit = () => dispatch('submit');
</script>

<div class="keypad">
	<button on:click={select(1)}>1</button>
	<button on:click={select(2)}>2</button>
	<button on:click={select(3)}>3</button>
	<button on:click={select(4)}>4</button>
	<button on:click={select(5)}>5</button>
	<button on:click={select(6)}>6</button>
	<button on:click={select(7)}>7</button>
	<button on:click={select(8)}>8</button>
	<button on:click={select(9)}>9</button>

	<button disabled={!value} on:click={clear}>clear</button>
	<button on:click={select(0)}>0</button>
	<button disabled={!value} on:click={submit}>submit</button>
</div>

<style>
	.keypad {
		display: grid;
		grid-template-columns: repeat(3, 5em);
		grid-template-rows: repeat(4, 3em);
		grid-gap: 0.5em
	}

	button {
		margin: 0
	}
</style>
```

<br>

## 38.Bindings-BindingToComponentInstances.svelte

Refs: [https://svelte.dev/tutorial/component-this](https://svelte.dev/tutorial/component-this)

```html
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
```

Just as you can bind to DOM elements, you can bind to component instances themselves. For example, we can bind the instance of `<InputField>` to a variable named `field` in the same way we did when binding DOM Elements

## 38.InputField.svelte

```html
<script>
	let input;

	export function focus() {
		input.focus();
	}
</script>

<input bind:this={input} />
```

<br>






<br>
<br>

# And the original README.md file from `npm init vite` is as follows: <br><br> Svelte + TS + Vite

This template should help get you started developing with Svelte and TypeScript in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.

## Technical considerations

**Why use this over SvelteKit?**

- It brings its own routing solution which might not be preferable for some users.
- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.

This template contains as little as possible to get started with Vite + TypeScript + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.

Should you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.

**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

Setting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

**Why include `.vscode/extensions.json`?**

Other templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

**Why enable `allowJs` in the TS template?**

While `allowJs: false` would indeed prevent the use of `.js` files in the project, it does not prevent the use of JavaScript syntax in `.svelte` files. In addition, it would force `checkJs: false`, bringing the worst of both worlds: not being able to guarantee the entire codebase is TypeScript, and also having worse typechecking for the existing JavaScript. In addition, there are valid use cases in which a mixed codebase may be relevant.

**Why is HMR not preserving my local component state?**

HMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/rixo/svelte-hmr#svelte-hmr).

If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

```ts
// store.ts
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```
