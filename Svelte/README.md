![Banner](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*efKjr7onmEdOWlrYzasrvQ.png)

# Svelte 🎨
Welcome to the Svelte learning notes! Here, we'll explore Svelte and its various features, providing you with a solid understanding of this powerful and efficient JavaScript framework. Whether you're new to Svelte or looking to expand your knowledge, these notes have got you covered.

## Table of Contents 📚
Explore Svelte step-by-step:

- [Introduction to Svelte 🔍](#introduction-to-svelte-)
- [Getting Started 🚀](#getting-started-)
  - [Installation ⚙](#installation-)
  - [Creating Your First Svelte App 🏗](#creating-your-first-svelte-app-)
- [Svelte Basics 📊](#svelte-basics-)
  - [Components 🧩](#components-)
  - [Reactivity 🔄](#reactivity-)
  - [Props 📨](#props-)
  - [Events 🎉](#events-)
- [Svelte Syntax 📝](#svelte-syntax-)
  - [Conditional Rendering 🔀](#conditional-rendering-)
  - [Loops 🔁](#loops-)
  - [Bindings 🔗](#bindings-)
- [State Management 📦](#state-management-)
  - [Stores 🏪](#stores-)
- [Lifecycle 🔄](#lifecycle-)
- [Styling in Svelte 🎨](#styling-in-svelte-)
- [Routing 🛣️](#routing-%EF%B8%8F)
- [Server-Side Rendering (SSR) 🖥️](#server-side-rendering-ssr-)
- [Best Practices and Tips 💡](#best-practices-and-tips-)

## Introduction to Svelte 🔍

Svelte is a modern JavaScript framework for building user interfaces. Unlike traditional frameworks like React or Vue, Svelte shifts much of its work to a compile step that happens when you build your app.

### Key Features of Svelte 🔗:
1. **Compilation:** Svelte compiles your code to efficient JavaScript at build time, resulting in smaller bundle sizes and better runtime performance.
2. **No Virtual DOM:** Svelte updates the DOM directly when your state changes, avoiding the overhead of a virtual DOM.
3. **Truly Reactive:** Svelte's reactivity is built into the language, making it intuitive and requiring less boilerplate code.
4. **Less Boilerplate:** Svelte requires less code to achieve the same results as other frameworks, leading to more readable and maintainable code.
5. **Built-in State Management:** Svelte includes a simple and powerful state management system out of the box.

### Comparison with React and Vue 👨‍💻:

| Feature | Svelte | React | Vue |
|---------|--------|-------|-----|
| Rendering | Compiles to vanilla JS | Virtual DOM | Virtual DOM |
| Learning Curve | Low | Moderate | Moderate |
| Performance | High | Good | Good |
| Bundle Size | Small | Larger | Moderate |
| Ecosystem | Growing | Very Large | Large |

### When to Use Svelte 🦋:
- For projects where performance and bundle size are critical
- When you want a simpler, more intuitive development experience
- For small to medium-sized applications
- When you're starting a new project and want to try a modern approach

## Getting Started 🚀

### Installation ⚙️

To start developing with Svelte, you'll need to have Node.js installed on your system. Once you have Node.js, you can create a new Svelte project using the official project template.

1. Open your terminal or command prompt.
2. Run the following command to create a new Svelte project:

```bash
npx degit sveltejs/template my-svelte-project
```

3. Navigate to your new project directory:

```bash
cd my-svelte-project
```

4. Install the dependencies:

```bash
npm install
```

### Creating Your First Svelte App 🏗️

Now that you have a Svelte project set up, let's create a simple "Hello, World!" app to get familiar with Svelte's structure.

1. Open the `src/App.svelte` file in your project. This is the main component of your Svelte app.

2. Replace the contents of `App.svelte` with the following code:

```html
<script>
  let name = 'World';
</script>

<main>
  <h1>Hello, {name}!</h1>
  <input bind:value={name}>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
```

3. Start the development server:

```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:8080`. You should see your "Hello, World!" app running.

This simple app demonstrates some key features of Svelte:

- The `<script>` section contains your component's logic.
- Variables (like `name`) are reactive by default.
- You can use curly braces `{}` to insert JavaScript expressions into your HTML.
- The `bind:value` directive creates a two-way binding between the input and the `name` variable.
- The `<style>` section contains component-scoped CSS.

Congratulations! You've just created your first Svelte app. ;)


## Svelte Basics 📊

### Components 🧩

Components are the building blocks of Svelte applications. Each component is a reusable piece of UI that encapsulates HTML, CSS, and JavaScript.

A basic Svelte component looks like this:

```html
<script>
  // Component logic goes here
</script>

<!-- HTML markup goes here -->

<style>
  /* Component-scoped styles go here */
</style>
```

Example: Creating a simple Button component

```html
<!-- Button.svelte -->
<script>
  export let text = 'Click me';
</script>

<button on:click>
  {text}
</button>

<style>
  button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }
</style>
```

### Reactivity 🔄

Svelte's reactivity system automatically updates the DOM when your component's state changes. This is one of Svelte's most powerful features.

Example: Reactive declarations

```html
<script>
  let count = 0;
  $: doubled = count * 2;

  function increment() {
    count += 1;
  }
</script>

<button on:click={increment}>
  Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>The doubled value is {doubled}</p>
```

In this example, `doubled` is a reactive declaration. It will automatically update whenever `count` changes.

### Props 📨

Props allow you to pass data from a parent component to a child component. They are declared using the `export` keyword in the child component.

Example: Using props

Parent component (App.svelte):
```html
<script>
  import Greeting from './Greeting.svelte';
</script>

<Greeting name="World" />
```

Child component (Greeting.svelte):
```html
<script>
  export let name;
</script>

<h1>Hello, {name}!</h1>
```

### Events 🎉

Svelte provides an easy way to handle DOM events and create custom events.

Example: Handling DOM events and creating custom events

```html
<script>
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();
  
  function handleClick() {
    dispatch('message', {
      text: 'Hello from child component!'
    });
  }
</script>

<button on:click={handleClick}>
  Click to send message
</button>
```

Using the custom event in a parent component:

```html
<script>
  import ChildComponent from './ChildComponent.svelte';

  function handleMessage(event) {
    alert(event.detail.text);
  }
</script>

<ChildComponent on:message={handleMessage}/>
```

These examples demonstrate the fundamental concepts of Svelte: components, reactivity, props, and events. Understanding these basics will provide a solid foundation for building more complex Svelte applications.


## Svelte Syntax 📝

Svelte provides a clean and intuitive syntax for building dynamic user interfaces. Let's explore some key syntactic features that make Svelte powerful and easy to use.

### Conditional Rendering 🔀

Svelte offers several ways to conditionally render content, making it easy to show or hide elements based on certain conditions.

#### 1. if Blocks

The most basic form of conditional rendering in Svelte uses the `{#if}` block:

```html
<script>
  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>

{#if user.loggedIn}
  <button on:click={toggle}>
    Log out
  </button>
{:else}
  <button on:click={toggle}>
    Log in
  </button>
{/if}
```

This is similar to React's conditional rendering using ternary operators or && conditions, but Svelte's syntax is more readable and closer to natural language.

#### 2. else if Blocks

For multiple conditions, you can use `{:else if}`:

```html
<script>
  let x = 5;
</script>

{#if x > 10}
  <p>{x} is greater than 10</p>
{:else if 5 > x}
  <p>{x} is less than 5</p>
{:else}
  <p>{x} is between 5 and 10</p>
{/if}
```

#### 3. Inline Conditionals

For simple conditions, you can use inline ternary expressions:

```html
<p>The number is {x > 10 ? 'greater than 10' : 'not greater than 10'}</p>
```

This is similar to how you'd use ternary operators in React JSX.

### Loops 🔁

Svelte provides a powerful and intuitive way to render lists of items using the `{#each}` block.

#### Basic Each Block

```html
<script>
  let fruits = ['apple', 'banana', 'cherry', 'date'];
</script>

<ul>
  {#each fruits as fruit}
    <li>{fruit}</li>
  {/each}
</ul>
```

This is similar to using `map()` in React, but Svelte's syntax is more concise and doesn't require you to explicitly return JSX.

#### Each Block with Index

You can also access the index of each item:

```html
<ul>
  {#each fruits as fruit, index}
    <li>{index + 1}: {fruit}</li>
  {/each}
</ul>
```

#### Destructuring in Each Blocks

If you're iterating over an array of objects, you can use destructuring:

```html
<script>
  let people = [
    { id: 1, name: 'Alice', age: 25 },
    { id: 2, name: 'Bob', age: 30 },
    { id: 3, name: 'Charlie', age: 35 },
  ];
</script>

<ul>
  {#each people as { id, name, age }}
    <li>{id}: {name} is {age} years old</li>
  {/each}
</ul>
```

#### Keyed Each Blocks

When the list changes, Svelte needs to know which items have changed. You can specify a unique identifier for each item using the `(key)` syntax:

```html
<ul>
  {#each people as person (person.id)}
    <li>{person.name} is {person.age} years old</li>
  {/each}
</ul>
```

This is similar to the `key` prop in React, but Svelte's syntax is more integrated with the loop construct.

### Bindings 🔗

Bindings in Svelte allow you to create two-way data flow between your component's state and the DOM. This is one area where Svelte significantly differs from React's one-way data flow philosophy.

#### Text Inputs

```html
<script>
  let name = 'world';
</script>

<input bind:value={name}>

<p>Hello {name}!</p>
```

In React, you'd need to set up an onChange handler and update the state manually:

```jsx
const [name, setName] = useState('world');

<input 
  value={name} 
  onChange={(e) => setName(e.target.value)} 
/>
```

#### Checkboxes

```html
<script>
  let checked = false;
</script>

<label>
  <input type="checkbox" bind:checked>
  Is checked: {checked}
</label>
```

#### Select Dropdowns

```html
<script>
  let selected;
  let options = ['apple', 'banana', 'cherry'];
</script>

<select bind:value={selected}>
  {#each options as option}
    <option value={option}>{option}</option>
  {/each}
</select>

<p>You selected: {selected}</p>
```

#### Component Bindings

You can even bind to component props:

```html
<!-- Parent.svelte -->
<script>
  import Child from './Child.svelte';
  let value = 'Hello';
</script>

<Child bind:value />
<p>Value in parent: {value}</p>

<!-- Child.svelte -->
<script>
  export let value;
</script>

<input bind:value />
```

This allows for easy two-way communication between parent and child components, which can be powerful but should be used judiciously to maintain clear data flow in your application.

Svelte's binding system offers a more straightforward way to handle form inputs and component communication compared to React's controlled components and prop drilling. However, it's important to use bindings responsibly to avoid creating complex and hard-to-track data flows in larger applications.


## State Management 📦

State management is a crucial aspect of any modern web application. While Svelte's reactive declarations can handle local component state effectively, for larger applications or for state that needs to be shared across multiple components, Svelte provides a powerful state management solution called Stores.

### Stores 🏪

Stores in Svelte are objects that hold a value and notify subscribers when that value changes. They provide a centralized way to manage and share state across your application.

#### Types of Stores

Svelte offers three types of stores:

1. Writable Stores
2. Readable Stores
3. Derived Stores

Let's explore each of these in detail:

##### 1. Writable Stores

Writable stores are the most flexible type of store. They can be both read from and written to.

```javascript
import { writable } from 'svelte/store';

const count = writable(0);

// To update the store
count.set(1);
count.update(n => n + 1);

// To subscribe to the store
const unsubscribe = count.subscribe(value => {
    console.log(value);
});

// Don't forget to unsubscribe when the component is destroyed
unsubscribe();
```

In components, you can use the `$` prefix to automatically subscribe to a store:

```html
<script>
import { count } from './stores.js';
</script>

<p>The count is {$count}</p>
<button on:click={() => $count++}>Increment</button>
```

This `$` syntax is unique to Svelte and makes working with stores very convenient compared to other state management solutions like Redux in React or Vuex in Vue.

##### 2. Readable Stores

Readable stores can only be read from, not written to. They're useful for values that are set from outside your application.

```javascript
import { readable } from 'svelte/store';

const time = readable(new Date(), function start(set) {
    const interval = setInterval(() => {
        set(new Date());
    }, 1000);

    return function stop() {
        clearInterval(interval);
    };
});
```

##### 3. Derived Stores

Derived stores are created from one or more other stores. They automatically update when the stores they depend on change.

```javascript
import { derived } from 'svelte/store';

const doubled = derived(count, $count => $count * 2);
```

#### Custom Stores

You can create custom stores to encapsulate more complex logic:

```javascript
function createCounter() {
    const { subscribe, set, update } = writable(0);

    return {
        subscribe,
        increment: () => update(n => n + 1),
        decrement: () => update(n => n - 1),
        reset: () => set(0)
    };
}

export const counter = createCounter();
```

Usage in a component:

```html
<script>
import { counter } from './stores.js';
</script>

<p>The count is {$counter}</p>
<button on:click={counter.increment}>+</button>
<button on:click={counter.decrement}>-</button>
<button on:click={counter.reset}>Reset</button>
```

#### Comparison with Other Frameworks

1. React Context and Redux:
   - Svelte's stores are simpler and require less boilerplate than React's Context API or Redux.
   - The `$` syntax in Svelte makes it easier to use store values in components compared to using `useContext` or `connect` in React.

2. Vue's Vuex:
   - Svelte's stores are more lightweight and don't require a central store configuration like Vuex does.
   - Vuex has a more structured approach with mutations and actions, while Svelte's stores are more flexible.

3. Angular's Services:
   - Svelte's stores are similar to Angular's services in terms of providing a way to share data between components.
   - However, Svelte's reactive `$` syntax makes it easier to use store values in templates compared to Angular's async pipe.

#### Best Practices

1. Use stores for state that needs to be shared across multiple components.
2. Keep your stores as simple as possible. Use derived stores to compute values instead of storing computed values directly.
3. Use custom stores to encapsulate complex logic and provide a clean API for components.
4. Remember to unsubscribe from stores when your component is destroyed to prevent memory leaks.
5. Use the `$` syntax in components for simplicity, but be aware that it's syntactic sugar for `subscribe` under the hood.

Svelte's store system provides a powerful yet simple way to manage state in your applications. Its integration with Svelte's reactivity system makes it a joy to use compared to some more complex state management solutions in other frameworks.

## Lifecycle 🔄

Understanding the lifecycle of a Svelte component is crucial for managing side effects, integrating with external libraries, and optimizing performance. Svelte provides several lifecycle functions that allow you to hook into different stages of a component's existence.

### Lifecycle Functions

Svelte offers four main lifecycle functions:

1. `onMount`
2. `onDestroy`
3. `beforeUpdate`
4. `afterUpdate`

Let's explore each of these in detail:

#### 1. onMount

The `onMount` function is called after the component is first rendered to the DOM. This is the ideal place to run any side effects that require the component to be in the DOM.

```javascript
import { onMount } from 'svelte';

onMount(() => {
    console.log('The component has mounted');
    
    // You can return a cleanup function if needed
    return () => {
        console.log('Cleanup from onMount');
    };
});
```

Use cases for `onMount`:
- Initializing third-party libraries that manipulate the DOM
- Starting timers or intervals
- Making initial API calls

Comparison with React:
- Similar to `useEffect(() => {}, [])` in React hooks
- Or `componentDidMount` in class components

#### 2. onDestroy

The `onDestroy` function is called when the component is unmounted from the DOM. It's used for cleanup tasks.

```javascript
import { onDestroy } from 'svelte';

onDestroy(() => {
    console.log('The component is being destroyed');
    // Perform cleanup tasks here
});
```

Use cases for `onDestroy`:
- Clearing timers or intervals
- Unsubscribing from subscriptions
- Cleaning up resources or event listeners

Comparison with React:
- Similar to the cleanup function returned by `useEffect` in React hooks
- Or `componentWillUnmount` in class components

#### 3. beforeUpdate

The `beforeUpdate` function is called immediately before the component is updated after any state change. This is useful for tasks you need to perform before the DOM is updated.

```javascript
import { beforeUpdate } from 'svelte';

beforeUpdate(() => {
    console.log('Component is about to update');
});
```

Use cases for `beforeUpdate`:
- Saving the current scroll position
- Recording the current state for comparison after update

Comparison with React:
- Similar to `getSnapshotBeforeUpdate` in class components
- No direct equivalent in React hooks, but can be simulated with `useEffect`

#### 4. afterUpdate

The `afterUpdate` function is called after the component updates and the DOM is in sync with your data.

```javascript
import { afterUpdate } from 'svelte';

afterUpdate(() => {
    console.log('Component just updated');
});
```

Use cases for `afterUpdate`:
- Updating the scroll position
- Measuring DOM elements after a change
- Updating third-party libraries that manipulate the DOM

Comparison with React:
- Similar to `componentDidUpdate` in class components
- Or `useEffect` without dependencies in React hooks

### Practical Example

Let's look at a practical example that uses multiple lifecycle functions:

```html
<script>
import { onMount, onDestroy, beforeUpdate, afterUpdate } from 'svelte';

let count = 0;
let timerId;

onMount(() => {
    console.log('Component mounted');
    timerId = setInterval(() => {
        count += 1;
    }, 1000);
});

onDestroy(() => {
    console.log('Component being destroyed');
    clearInterval(timerId);
});

beforeUpdate(() => {
    console.log('Component about to update, count is', count);
});

afterUpdate(() => {
    console.log('Component updated, count is now', count);
});
</script>

<p>Count: {count}</p>
```

This example demonstrates:
- Using `onMount` to set up an interval
- Using `onDestroy` to clean up the interval
- Using `beforeUpdate` and `afterUpdate` to log the state before and after updates

### Best Practices

1. Use `onMount` for initialization that requires the DOM to be present.
2. Always clean up side effects (like timers or subscriptions) in `onDestroy`.
3. Use `beforeUpdate` and `afterUpdate` sparingly, as they run on every state change.
4. Avoid direct DOM manipulation in lifecycle functions when possible; let Svelte handle it.
5. Remember that lifecycle functions are only run on the client-side, not during server-side rendering.

### Comparison with Other Frameworks

- React: Svelte's lifecycle functions are more straightforward compared to React's class lifecycle methods. They're closer to React hooks in terms of simplicity, but with clearer separation of concerns.
- Vue: Svelte's lifecycle functions are similar to Vue's lifecycle hooks, but with slightly different naming (e.g., `onMount` in Svelte vs `mounted` in Vue).
- Angular: Svelte's approach is more lightweight compared to Angular's lifecycle hooks, which are tied to its change detection cycle.

Understanding and effectively using these lifecycle functions will help you manage your Svelte components more efficiently, handle side effects properly, and create more robust applications.
