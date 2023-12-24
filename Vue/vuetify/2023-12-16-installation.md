---
title: "[Vuetify] Installation"
author: nijesmik
date: 2023-12-16 00:00
categories: [Vue]
tag: [Vue, Vuetify]
---

## Add Vuetify to an existing project

> **출처** <br>
> [Get started with Vuetify 3 — Vuetify](https://vuetifyjs.com/en/getting-started/installation/#existing-projects)
{: .prompt-info }

1.

```sh
npm i vuetify
```

2. In the file where you create the Vue application, add the following code

```js
import { createApp } from 'vue'
import App from './App.vue'

// Vuetify
import 'vuetify/styles'
import { createVuetify } from 'vuetify'
import * as components from 'vuetify/components'
import * as directives from 'vuetify/directives'

const vuetify = createVuetify({
  components,
  directives,
})

createApp(App).use(vuetify).mount('#app')
```
