# Store-o-saurus

Super simple JSON store for [Deno](https://deno.land).

## Usage

- Use `import` to add `Store` class to your project
- `await` on `Store.open<TYPE>('myStoreName')`
- Use `write()` and `read()` methods of your store instance

```typescript
import {Store} from 'https://raw.githubusercontent.com/felixblaschke/store-o-saurus/master/mod.ts';

const counter = await Store.open<{value: number}>('counter', {
    default: {value: 0}
});

await counter.write( data => data.value++);

await counter.read(data => {
    console.log("Counter: ", data.value);
})
```

See [examples](examples/) for more usages.
