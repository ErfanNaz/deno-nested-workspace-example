# deno-nested-workspace-example

- goal is to have a nested workspace for app 
- example code will not work -> deno-ns message `'core' is declared but its value is never read.deno-ts`

- deno check 
```
Warning "importMap" field can only be specified in the workspace root deno.json file.
    at file:///C:/.../deno-workspace-example/app/deno.json
Warning "workspace" field can only be specified in the workspace root deno.json file.
    at file:///C:/.../deno-workspace-example/app/deno.json
```

```ts
import { core } from '@example/core' // <- is not working
import { b } from '@example/app/b' // <- or @example/b is not working

export function a() {
  console.log("hallo a")
}
```