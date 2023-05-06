# Test Vue 3.3

Need `--force` due to a dependency problem.

```
npm i -f
```

Bug with `defineProps` and TypeScript import :\
[MaisonCard.vue](/src/components/MaisonCard.vue)

```ts
// Bug
import type { MaisonResponse } from '@/pocketbase-types'
// Work with extra import `MaisonRecord`
import type { MaisonResponse, MaisonRecord } from '@/pocketbase-types'
defineProps<MaisonResponse>()
```

[pocketbase-types.ts](/src/pocketbase-types.ts)

```ts
export type MaisonResponse = Required<MaisonRecord> & BaseSystemFields
```

Error msg

```
[plugin:vite:vue] [@vue/compiler-sfc] Unresolvable type reference or unsupported built-in utility type

<snip>.../src/components/MaisonCard.vue
<snip>.../src/components/MaisonCard.vue
    at ScriptCompileContext.error (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:15839:11)
    at innerResolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17964:20)
    at resolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17900:35)
    at resolveBuiltin (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:18222:13)
    at innerResolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17952:20)
    at resolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17900:35)
    at <snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17922:31
    at Array.map (<anonymous>)
    at innerResolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17922:20)
    at resolveTypeElements (<snip>.../node_modules/vue/node_modules/@vue/compiler-sfc/dist/compiler-sfc.cjs.js:17900:35
```
