# deno-nested-workspace-example

- goal is to have a nested workspace for app 
- example code will not work -> deno-ns message `'core' is declared but its value is never read.deno-ts`

```ts
import { core } from '@example/core' // <- is not working
import { b } from '@example/app/b' // <- or @example/b is not working

export function a() {
  console.log("hallo a")
}
```