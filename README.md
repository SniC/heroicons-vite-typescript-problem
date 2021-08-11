# heroicons-vite-typescript-problem
This repo shows the problem with heroicons in combination with vite/vue/typescript.
To reproduce the issue, the following steps where taken:

1. Start vite project using `npm init vite@latest heroicon-vite-typescript-problem -- --template vue-ts`
2. Install `@heroicons/vue`
3. Import and use icon in `App.vue`

Just run `npm run build` to reveal this issue for every icon:

```cmd
node_modules/@heroicons/vue/solid/ZoomOutIcon.d.ts:1:30 - error TS2339: Property 'DefineComponent' does not exist on type 'Promise<{ default: typeof import("d:/git/heroicons-vite-typescript-problem/node_modules/vue/dist/vue"); compile(template: string | HTMLElement, options?: CompilerOptions | undefined): RenderFunction; ... 143 more ...; withScopeId: (_id: string) => (fn: Function, ctx?: ComponentInternalInstance | ... 1 more ... | und...'.

1 export default import("vue").DefineComponent;
```
