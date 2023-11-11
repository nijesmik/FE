# computed()

> [Reactivity API: Core | Vue.js](https://vuejs.org/api/reactivity-core.html#computed)

Takes a getter function and returns a readonly reactive ref object for the returned value from the getter.

```ts
function computed<T>(
  getter: () => T,
  // see "Computed Debugging" link below
  debuggerOptions?: DebuggerOptions
): Readonly<Ref<Readonly<T>>>
```

It can also take an object with get and set functions to create a writable ref object.

```ts
function computed<T>(
  options: {
    get: () => T
    set: (value: T) => void
  },
  debuggerOptions?: DebuggerOptions
): Ref<T>
```