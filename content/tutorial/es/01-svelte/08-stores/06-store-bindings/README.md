---
title: Tienda de encuadernaciones
---

Si una tienda es escribible, es decir, tiene un método `set`, puedes vincularte a su valor de la misma manera que puedes vincularte al estado local del componente.

En este ejemplo, estamos exportando un `name` de tienda grabable y un `greeting` de tienda derivado de `stores.js` . Actualice el elemento `<input>` en `App.svelte` :

```svelte
/// file: App.svelte
<input +++bind:+++value={$name}>
```

Cambiar el valor de entrada ahora actualizará `name` y todos sus dependientes.

También podemos asignar directamente para almacenar valores dentro de un componente. Agrega un elemento `<button>` después de `<input>` :

```svelte
/// file: App.svelte
<button +++on:click={() => $name += '!'}+++>
	Add exclamation mark!
</button>
```

El `$name += '!'` la asignación es equivalente a `name.set($name + '!')` .
