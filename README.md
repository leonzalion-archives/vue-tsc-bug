# vue-tsc bug

When using union operator in defineEmits (see `src/App-bug.vue`):

```ts
defineEmits<{
  (e: "a" | "b"): string;
}>();
```

vue-tsc is unable to find variables in the component:

![vue-tsc error](images/vue-tsc-error.png)
