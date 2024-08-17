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

