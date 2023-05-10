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
