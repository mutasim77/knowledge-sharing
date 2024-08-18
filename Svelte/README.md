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


## Styling in Svelte 🎨

Svelte provides a clean and intuitive way to style your components. It offers component-scoped styles by default, while still allowing for global styles when needed. This approach helps in creating modular, maintainable CSS without the need for additional libraries or complex setup.

### Component-Scoped Styles

In Svelte, styles defined within a component's `<style>` block are automatically scoped to that component. This means the styles only apply to elements within that component, preventing unintended side effects on other parts of your application.

```html
<style>
  p {
    color: purple;
    font-family: 'Comic Sans MS', cursive;
    font-size: 2em;
  }
</style>

<p>This is a purple paragraph with a fun font!</p>
```

Under the hood, Svelte adds a unique class to the component's root element and transforms your selectors to scope them to this class. This is similar to CSS Modules or styled-components in React, but it's built into Svelte with no additional setup required.

### Global Styles

While scoped styles are the default, sometimes you need styles to apply globally. Svelte allows this using the `:global()` modifier:

```html
<style>
  :global(body) {
    background-color: #f0f0f0;
  }

  p {
    color: purple;
  }

  :global(.highlight) {
    background-color: yellow;
  }
</style>

<p>This paragraph is purple.</p>
<p class="highlight">This paragraph is purple with a yellow background.</p>
```

### CSS Variables

Svelte works great with CSS custom properties (variables), allowing for dynamic styling:

```html
<script>
  let color = 'red';
</script>

<style>
  p {
    color: var(--color);
  }
</style>

<p style="--color: {color}">This paragraph's color can be dynamically changed.</p>

<button on:click={() => color = 'blue'}>Change to Blue</button>
```

### Inline Styles

For truly dynamic styles, you can use inline style bindings:

```html
<script>
  let fontSize = 16;
</script>

<p style="font-size: {fontSize}px">
  This text can change size.
</p>

<button on:click={() => fontSize += 2}>Increase Size</button>
```

### CSS in JavaScript

Svelte also allows you to define styles programmatically using template literals:

```html
<script>
  const backgroundColor = 'lightblue';
  const textColor = 'darkblue';

  const style = `
    background-color: ${backgroundColor};
    color: ${textColor};
    padding: 10px;
    border-radius: 5px;
  `;
</script>

<div {style}>
  This div's style is defined in JavaScript!
</div>
```

### External Stylesheets

While Svelte encourages component-scoped styles, you can still use external stylesheets. Simply link them in your `public/index.html` file:

```html
<link rel="stylesheet" href="/global.css">
```

### Preprocessors

Svelte has built-in support for preprocessors like SCSS, Less, and Stylus. You'll need to install the appropriate preprocessor and configure it in your Svelte config. Here's an example using SCSS:

```html
<style lang="scss">
  $color: red;
  p {
    color: $color;
    &:hover {
      color: darken($color, 10%);
    }
  }
</style>
```

### Best Practices

1. Prefer component-scoped styles to keep your components modular and maintainable.
2. Use `:global()` sparingly, only for truly global styles.
3. Leverage CSS variables for dynamic styling that doesn't require JavaScript.
4. Consider using a CSS methodology like BEM or SMACSS for larger applications.
5. Be mindful of specificity when mixing scoped and global styles.

### Comparison with Other Frameworks

1. React: 
   - Svelte's scoped styles are similar to CSS Modules or styled-components in React, but with less setup and boilerplate.
   - Unlike React, Svelte doesn't require additional libraries for scoped styles or CSS-in-JS solutions.

2. Vue: 
   - Svelte's approach is very similar to Vue's scoped styles, but Svelte scopes styles by default without needing a `scoped` attribute.

3. Angular: 
   - Svelte's component-scoped styles are similar to Angular's view encapsulation, but with a simpler implementation.
   - Svelte doesn't require special selectors like `:host` for styling the component root.

4. Vanilla CSS:
   - Svelte's scoped styles solve common problems like naming conflicts and specificity issues that occur in large vanilla CSS codebases.
   - The ability to mix scoped and global styles provides more flexibility than pure vanilla CSS approaches.

Svelte's approach to styling strikes a balance between the simplicity of traditional CSS and the modularity of more modern CSS-in-JS solutions. It provides powerful features out of the box while maintaining a clean and intuitive syntax.

## Routing 🛣️

Routing is a crucial part of any web application, allowing for navigation between different views or pages. In Svelte applications, routing is typically handled using [SvelteKit](https://kit.svelte.dev/), the official application framework for Svelte. SvelteKit provides a file-based routing system that's both powerful and intuitive.

### SvelteKit Routing Basics

SvelteKit uses a file-based routing system. This means that the structure of your `src/routes` directory determines your application's routes.

#### Basic Routes

To create a basic route, simply create a `+page.svelte` file in the `src/routes` directory:

```
src/routes/
├── +page.svelte
├── about/
│   └── +page.svelte
└── contact/
    └── +page.svelte
```

In this structure:
- `/` will render `src/routes/+page.svelte`
- `/about` will render `src/routes/about/+page.svelte`
- `/contact` will render `src/routes/contact/+page.svelte`

#### Layout Files

You can create layout files (`+layout.svelte`) to share common elements across multiple pages:

```svelte
<!-- src/routes/+layout.svelte -->
<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
  <a href="/contact">Contact</a>
</nav>

<slot></slot>

<footer>© 2024 My Svelte App</footer>
```

This layout will be applied to all pages in your app.

### Dynamic Routes

SvelteKit supports dynamic routes using square brackets `[]` in the file or directory name:

```
src/routes/
└── blog/
    ├── +page.svelte
    └── [slug]/
        └── +page.svelte
```

In this structure, `/blog/my-first-post` will render the `+page.svelte` file inside the `[slug]` directory. You can access the `slug` parameter in your page:

```svelte
<!-- src/routes/blog/[slug]/+page.svelte -->
<script>
  export let data;
</script>

<h1>{data.post.title}</h1>
<div>{@html data.post.content}</div>
```

The `data` prop is populated by a corresponding `+page.js` (or `+page.server.js`) file:

```javascript
// src/routes/blog/[slug]/+page.js
export function load({ params }) {
  return {
    post: {
      title: `Blog post ${params.slug}`,
      content: 'This is a blog post.'
    }
  };
}
```

### Nested Routes

SvelteKit allows for nested routes, which can be useful for creating complex layouts:

```
src/routes/
└── dashboard/
    ├── +layout.svelte
    ├── +page.svelte
    ├── users/
    │   └── +page.svelte
    └── settings/
        └── +page.svelte
```

In this structure, the `dashboard/+layout.svelte` file can contain layout elements specific to the dashboard section of your app.

### Programmatic Navigation

SvelteKit provides a `goto` function for programmatic navigation:

```svelte
<script>
  import { goto } from '$app/navigation';

  function handleClick() {
    goto('/about');
  }
</script>

<button on:click={handleClick}>Go to About</button>
```

### Route Parameters and Query Strings

You can access route parameters and query strings in your `load` functions:

```javascript
// src/routes/search/+page.js
export function load({ url }) {
  const query = url.searchParams.get('q');
  // Fetch search results based on query
  return { searchResults };
}
```

### Server-Side Rendering (SSR)

SvelteKit supports server-side rendering out of the box. You can use `+page.server.js` files to run code exclusively on the server:

```javascript
// src/routes/blog/[slug]/+page.server.js
export async function load({ params }) {
  const post = await fetchPostFromDatabase(params.slug);
  return { post };
}
```

### Comparison with Other Frameworks

1. React (Next.js):
   - SvelteKit's file-based routing is similar to Next.js, but with a simpler file naming convention.
   - Both support dynamic routes and nested layouts.

2. Vue (Nuxt.js):
   - SvelteKit's routing is very similar to Nuxt.js, with both using a file-based system.
   - SvelteKit's `+page.svelte` is analogous to Nuxt's `index.vue`.

3. Angular:
   - Unlike Angular's module-based routing, SvelteKit uses a more intuitive file-based system.
   - SvelteKit doesn't require a separate routing configuration file like Angular's `app-routing.module.ts`.

### Best Practices

1. Keep your route structure shallow and meaningful.
2. Use layout files to avoid repeating common elements across pages.
3. Leverage dynamic routes for content-driven pages like blog posts or product details.
4. Use `+page.server.js` for server-side operations and to protect sensitive data.
5. Implement proper error handling for your routes, including a 404 page.

SvelteKit's routing system provides a powerful yet intuitive way to structure your Svelte applications. Its file-based approach, combined with features like nested layouts and server-side rendering, makes it easy to create complex, performant web applications.

## Server-Side Rendering (SSR) 🖥️

Server-Side Rendering (SSR) is a technique where the initial content of a web page is generated on the server rather than in the browser. SvelteKit, the official application framework for Svelte, provides built-in support for SSR, making it easy to create fast, SEO-friendly applications.

### Benefits of SSR

1. **Improved Initial Load Time:** The server sends pre-rendered HTML, allowing users to see content faster.
2. **Better SEO:** Search engines can easily crawl and index the content of your pages.
3. **Enhanced Performance on Low-Power Devices:** Less JavaScript needs to be parsed and executed on the client.
4. **Improved Accessibility:** Content is available even if JavaScript fails or is disabled.

### How SSR Works in SvelteKit

In SvelteKit, every page component (`+page.svelte`) can have an associated `+page.server.js` file that runs on the server to prepare data for the page.

#### Basic SSR Example

```javascript
// src/routes/blog/[slug]/+page.server.js
export async function load({ params }) {
  const post = await fetchBlogPost(params.slug);
  return { post };
}
```

```svelte
<!-- src/routes/blog/[slug]/+page.svelte -->
<script>
  export let data;
</script>

<h1>{data.post.title}</h1>
<div>{@html data.post.content}</div>
```

In this example, `fetchBlogPost` would be a function that retrieves the blog post data from a database or API. The `load` function runs on the server, and its return value is passed as the `data` prop to the page component.

### Server-Only Code

SvelteKit allows you to write server-only code using the `+page.server.js` file. This is useful for operations that should never be exposed to the client, such as database queries or API calls with sensitive information.

```javascript
// src/routes/dashboard/+page.server.js
import { redirect } from '@sveltejs/kit';

export function load({ locals }) {
  if (!locals.user) {
    throw redirect(307, '/login');
  }

  return {
    user: locals.user
  };
}
```

### Handling Forms with SSR

SvelteKit provides a way to handle form submissions on the server, which is great for progressive enhancement:

```javascript
// src/routes/contact/+page.server.js
export const actions = {
  default: async ({ request }) => {
    const data = await request.formData();
    const name = data.get('name');
    const email = data.get('email');
    const message = data.get('message');

    // Process the form data (e.g., send an email, save to database)
    await sendEmail({ name, email, message });

    return { success: true };
  }
};
```

```svelte
<!-- src/routes/contact/+page.svelte -->
<script>
  export let form;
</script>

<form method="POST">
  <input name="name" required>
  <input name="email" type="email" required>
  <textarea name="message" required></textarea>
  <button>Send</button>
</form>

{#if form?.success}
  <p>Message sent successfully!</p>
{/if}
```

### Hydration

After the initial server-rendered content is delivered to the browser, SvelteKit "hydrates" the page, attaching event listeners and making it interactive. This process is automatic and seamless.

### SSR vs Static Site Generation (SSG)

SvelteKit also supports Static Site Generation, where pages are pre-rendered at build time. You can choose between SSR and SSG on a per-route basis:

```javascript
// src/routes/blog/[slug]/+page.js
export const prerender = true;

export async function load({ params }) {
  const post = await fetchBlogPost(params.slug);
  return { post };
}
```

Setting `prerender = true` tells SvelteKit to generate this page at build time rather than on each request.

### Customizing SSR Behavior

SvelteKit allows you to customize SSR behavior through the `handle` hook in your `src/hooks.server.js` file:

```javascript
/** @type {import('@sveltejs/kit').Handle} */
export async function handle({ event, resolve }) {
  // You can modify the request here
  event.locals.user = await getUser(event.request.headers.get('cookie'));

  const response = await resolve(event);

  // You can modify the response here
  response.headers.set('x-custom-header', 'potato');

  return response;
}
```

### Comparison with Other Frameworks

1. React (Next.js):
   - Both SvelteKit and Next.js provide built-in SSR support.
   - SvelteKit's approach is more straightforward, with less boilerplate code.

2. Vue (Nuxt.js):
   - Nuxt.js and SvelteKit have similar SSR implementations.
   - Both use file-based routing and support server-side data fetching.

3. Angular (Universal):
   - Angular Universal requires more setup compared to SvelteKit's out-of-the-box SSR support.
   - SvelteKit's SSR is more tightly integrated with its routing system.

### Best Practices

1. Use `+page.server.js` for server-side operations and to protect sensitive data.
2. Implement proper error handling for your server-side code.
3. Be mindful of the data you're sending to the client to avoid exposing sensitive information.
4. Use SSG for pages that don't require real-time data.
5. Optimize your server-side data fetching to ensure fast response times.
6. Use streaming SSR for large pages to improve Time to First Byte (TTFB).

Server-Side Rendering in SvelteKit provides a powerful way to create fast, SEO-friendly, and accessible web applications. Its seamless integration with Svelte's reactivity system and SvelteKit's routing make it a joy to work with compared to SSR implementations in some other frameworks.
