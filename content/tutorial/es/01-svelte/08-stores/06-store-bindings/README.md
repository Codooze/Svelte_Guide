---
title: Store bindings
---

Si una tienda es escribible, es decir, tiene un método `set`, puedes vincularte a su valor de la misma manera que puedes vincularte al estado local del componente.

In this example we're exporting a writable store `name` and a derived store `greeting` from `stores.js`. Update the `<input>` element in `App.svelte`:

```svelte
/// file: App.svelte
<input +++bind:+++value={$name}>
```

Changing the input value will now update `name` and all its dependents.

We can also assign directly to store values inside a component. Add a `<button>` element after the `<input>`:

```svelte
/// file: App.svelte
<button +++on:click={() => $name += '!'}+++>
	Add exclamation mark!
</button>
```

The `$name += '!'` assignment is equivalent to `name.set($name + '!')`.
