![banner](https://github.com/user-attachments/assets/5d21f6f9-e255-4a66-811f-7abb9f61979b)

# Vue.js ❇️
Hey there!👋 Welcome to my Vue.js learning journey! In this section, we'll explore Vue.js 3 and dive deep into the Composition API. Let's start!

## Table of Contents 📜
Explore various topics related to Vue.js 3:

1. [Introduction to Vue.js 3 🌟](#introduction-to-vuejs-3-)
2. [Vue.js 3 Essentials 💡](#vuejs-3-essentials-)
4. [Getting Started with Vue 3 🏁](#getting-started-with-vue-3-)
5. [Understanding the Composition API 🧩](#understanding-the-composition-api-)
6. [Core Concepts of Vue 3 🔑](#core-concepts-of-vue-3-)
7. [Building Your First Vue 3 App 🛠️](#building-your-first-vue-3-app-)

## Introduction to Vue.js 3 🌟

Vue.js 3 is a progressive JavaScript framework for building user interfaces. It builds on top of standard HTML, CSS, and JavaScript and provides a declarative and component-based programming model that helps you efficiently develop user interfaces, be they simple or complex.

> In simple words: Vue.js 3 is like a super-powered toolkit for creating interactive and dynamic web applications with ease!

## Getting Started with Vue 3 🏁

To start with Vue 3, you'll need to set up your development environment:

1. **Install Node.js:** Make sure you have Node.js installed on your machine.
2. **Create a Vue Project:** Use the Vue CLI to create a new project:
```bash
npm create vue@latest
```
3. Navigate to Your Project & Install Dependencies:
```bash
cd your-project-name
npm install
```
4. Run the Development Server:
```bash
npm run dev
```
You should now have your first Vue project running!🪼

## Vue.js 3 Essentials 💡
Let's dive into the essential concepts of Vue.js 3:

### 1. Template Syntax 📝
Vue uses an HTML-based template syntax that allows you to declaratively bind the rendered DOM to the underlying component instance's data.
```vue
<template>
  <div>{{ message }}</div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const message = ref('Hello Vue 3!')
    return { message }
  }
}
</script>
```

## 2. Reactivity Fundamentals ⚛️
Vue's reactivity system allows for automatic tracking of dependencies and efficient updates when data changes.
```vue
import { ref, reactive } from 'vue'

const count = ref(0)
const state = reactive({ name: 'Vue' })
```

## 3. Computed Properties 🧮
Computed properties are cached based on their reactive dependencies and only re-evaluate when needed.
```vue
import { ref, computed } from 'vue'

const count = ref(0)
const doubleCount = computed(() => count.value * 2)
```

## 4. Class and Style Bindings 🎨
Vue provides special enhancements when using v-bind with class and style to make binding dynamic classes and styles more flexible.
```vue
<template>
  <div :class="{ active: isActive }" :style="{ color: activeColor }">
    Dynamic Styling
  </div>
</template>
```

## 5. Conditional Rendering 🔀
Use `v-if`, `v-else-if`, and `v-else` directives to conditionally render elements.
```vue
<template>
  <div v-if="type === 'A'">A</div>
  <div v-else-if="type === 'B'">B</div>
  <div v-else>Not A/B</div>
</template>
```

## 6. List Rendering 📋
Use the `v-for` directive to render a list of items based on an array.
```vue
<template>
  <ul>
    <li v-for="item in items" :key="item.id">{{ item.text }}</li>
  </ul>
</template>
```

## 7. Event Handling 🖱️
Use the `v-on` directive (typically shortened to `@`) to listen to DOM events and run JavaScript when triggered.
```vue
<template>
  <button @click="increment">Increment</button>
</template>
```

## 8. Form Input Bindings 📝
Use `v-model` directive to create two-way data bindings on form input elements.
```vue
<template>
  <input v-model="message" placeholder="edit me">
  <p>Message is: {{ message }}</p>
</template>
```

## 9. Lifecycle Hooks ♻️
Lifecycle hooks allow you to hook into different stages of a component's lifecycle.
```vue
import { onMounted, onUnmounted } from 'vue'

export default {
  setup() {
    onMounted(() => {
      console.log('Component is mounted!')
    })
    onUnmounted(() => {
      console.log('Component is unmounted!')
    })
  }
}
```

## 10. Watchers 👀
Watchers allow you to observe and react to data changes.
```vue
import { ref, watch } from 'vue'

const question = ref('')
const answer = ref('Questions usually contain a question mark. ;-)')

watch(question, async (newQuestion, oldQuestion) => {
  if (newQuestion.indexOf('?') > -1) {
    answer.value = 'Thinking...'
    try {
      const res = await fetch('https://yesno.wtf/api')
      answer.value = (await res.json()).answer
    } catch (error) {
      answer.value = 'Error! Could not reach the API. ' + error
    }
  }
})
```

## 11. Template Refs 🎯
Template refs provide a way to obtain direct references to specific DOM elements or child components.

```vue
<template>
  <input ref="inputRef">
</template>

<script>
import { ref, onMounted } from 'vue'

export default {
  setup() {
    const inputRef = ref(null)

    onMounted(() => {
      inputRef.value.focus()
    })

    return {
      inputRef
    }
  }
}
</script>
```

## 12. Components Basics 🧩
Components are reusable Vue instances with a name. They can be used as custom elements in other components' templates.
```vue
<script setup>
import ButtonCounter from './ButtonCounter.vue'
</script>

<template>
  <h1>Here is a child component!</h1>
  <ButtonCounter />
</template>
```
