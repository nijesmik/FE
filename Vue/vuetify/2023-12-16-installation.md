# Add Vuetify to an existing project

> [Get started with Vuetify 3 — Vuetify](https://vuetifyjs.com/en/getting-started/installation/#existing-projects)

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
