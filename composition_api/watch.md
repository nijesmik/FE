# watch()

> [Reactivity API: Core | Vue.js](https://vuejs.org/api/reactivity-core.html#watch)

Watches one or more reactive data sources and invokes a callback function when the sources change.

```ts
function watch<T>(
  source: WatchSource<T>,
  callback: WatchCallback<T>,
  options?: WatchOptions
): StopHandle
```

## Details

### source

The source can be one of the following:

* A getter function that returns a value
* A ref
* A reactive object
* ...or an array of the above.

### callback

```ts
type WatchCallback<T> = (
  value: T,
  oldValue: T,
  onCleanup: (cleanupFn: () => void) => void
) => void
```

The callback receives three arguments:
* the new value
* the old value
* a function for registering a side effect cleanup callback

The cleanup callback will be called right before the next time the effect is re-run, and can be used to clean up invalidated side effects, e.g. a pending async request.

## Example

Watching a ref:

```js
const count = ref(0);

watch(count, (count, prevCount) => {
  /* ... */
})
```
