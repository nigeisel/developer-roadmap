# As Any

`any` is a special type in TypeScript that represents a value of any type. When a value is declared with the any type, the compiler will not perform any type checks or type inference on that value.

For example:

```typescript
let anyValue: any = 42;

// we can assign any value to anyValue, regardless of its type
anyValue = 'Hello, world!';
anyValue = true;
```

Asserting any (`as any`) effectively disables TypeScript’s safety for a value:
```typescript
let typedValue: number = 42;
let anyValue = typedValue as any;

// TypeScript will allow it due to the assertion, but this will cause a runtime issue because "anyValue is not a function" 
console.log(anyValue());
```

⚠️ Due to the runtime dangers, `as any` Assertions should be avoided!


Learn more from the following links:

- [@official@any](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#any)
