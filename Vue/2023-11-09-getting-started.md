# Getting Started

> [Quick Start | Vue.js](https://vuejs.org/guide/quick-start.html)
> [Single-File Components | Vue.js](https://vuejs.org/guide/scaling-up/sfc.html)

## Creating a Vue Application

```bash
npm create vue@latest
```

This command will install and execute [create-vue](https://github.com/vuejs/create-vue), the official Vue project scaffolding tool. The created project will be using a build setup based on [Vite](https://vitejs.dev/) and allow us to use Vue Single-File Components (SFCs).

### Single-File Components

Vue Single-File Components (a.k.a. `*.vue` files, abbreviated as SFC) is a special file format that allows us to encapsulate the template, logic, and styling of a Vue component in a single file.

```vue
<template>
  <p class="greeting">{{ greeting }}</p>
</template>

<script setup>
import { ref } from 'vue'
const greeting = ref('Hello World!')
</script>

<style>
.greeting {
  color: red;
  font-weight: bold;
}
</style>
```

## Using Vue from CDN

### Using the Global Build

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app">{{ message }}</div>

<script>
  const { createApp, ref } = Vue

  createApp({
    setup() {
      const message = ref('Hello vue!')
      return {
        message
      }
    }
  }).mount('#app')
</script>
```

### Using the [ES Module](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) Build

```html
<div id="app">{{ message }}</div>

<script type="module">
  import { createApp, ref } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'

  createApp({
    setup() {
      const message = ref('Hello Vue!')
      return {
        message
      }
    }
  }).mount('#app')
</script>
```
