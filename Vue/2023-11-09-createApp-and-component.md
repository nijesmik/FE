---
title: "[Vue] createApp() and Component"
author: nijesmik
date: 2023-11-09 01:00
categories: [Vue]
tag: [Vue]
---

## createApp()

> **출처** <br>
> [Creating a Vue Application | Vue.js](https://vuejs.org/guide/essentials/application.html#the-application-instance) <br>
> [Application API | Vue.js](https://vuejs.org/api/application.html#createapp)
{: .prompt-info }

Every Vue application starts by creating a new **application instance** with the `createApp` function:

```js
import { createApp } from 'vue'

const app = createApp({
    /* root component options */
})
```

### Details

```ts
function createApp(rootComponent: Component, rootProps?: object): App
```

* The first argument(`rootComponent`) is the **root component**.
* The second <U>optional</U> argument(`rootProps`) is the **props to be passed to the root component**.



## Root Component

> **출처** <br>
> [Creating a Vue Application | Vue.js](https://vuejs.org/guide/essentials/application.html#the-root-component) <br>
> [Components Basics | Vue.js](https://vuejs.org/guide/essentials/component-basics.html)
{: .prompt-info }

The object we are passing into `createApp` is in fact a component. Every `app` requires a **root component** that can contain other components as its children.

![](https://vuejs.org/assets/components.7fbb3771.png)



## Component

> **출처** <br>
> [Glossary | Vue.js](https://vuejs.org/glossary/#component)
{: .prompt-info }

It describes **a chunk of the UI**, such as a button or checkbox. Components can also be combined to form larger components.

Components are the primary mechanism provided by Vue to split a UI into smaller pieces, both to improve maintainability and to allow for code reuse.

A Vue component is an object. All properties are optional, but either a template or render function is required for the component to render. 
