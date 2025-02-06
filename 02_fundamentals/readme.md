# 🚀 Understanding Built-in TypeScript Types

Welcome to the section where we explore **built-in types in TypeScript**! TypeScript builds on JavaScript's basic types, introducing new types to enhance type safety, reduce errors, and make your code more robust. This guide will walk you through the core types in both JavaScript and TypeScript, along with practical examples.

---

### 🔢 Built-in Types in JavaScript

JavaScript provides a set of basic types that you're already familiar with. Here’s a quick rundown:

- **`number`**: Represents both integers and floating-point numbers.
  ```typescript
  let sales: number = 12345;
  ```

- **`string`**: Represents text values.
  ```typescript
  let course: string = "TypeScript Basics";
  ```

- **`boolean`**: Represents `true` or `false` values.
  ```typescript
  let isPublished: boolean = true;
  ```

- **`undefined`**: A variable that has been declared but not assigned a value.
  ```typescript
  let myValue: undefined;
  ```

- **`object`**: Used to represent non-primitive values such as arrays, objects, and functions.
  ```typescript
  let user: object = { name: "Alice", age: 30 };
  ```

---

### 🆕 TypeScript-Specific Types

TypeScript enhances JavaScript’s basic types by introducing several new types. These additions improve type safety and help make code more predictable and error-free.

#### 1. **`any`** 🌐
The `any` type allows a variable to hold **any type of value**, meaning it’s highly flexible but also disables type safety. Use this sparingly!

**Example:**
```typescript
let dynamicValue: any = 5;
dynamicValue = "Now a string";  // No error
```
While `any` is useful in specific cases, relying too much on it defeats TypeScript's purpose of type safety. So, try to limit its use.

---

### 🖍️ Type Inference in TypeScript

TypeScript has a powerful feature called **type inference**, which allows the compiler to automatically detect the type of a variable based on its initial value. This means you don’t always need to annotate types manually.

**Example:**
```typescript
let sales = 12345;  // TypeScript infers `number`
let course = "TypeScript Basics";  // TypeScript infers `string`
let isPublished = true;  // TypeScript infers `boolean`
```

**Key Takeaway**:  
- When you initialize a variable, TypeScript automatically infers its type.
- If no value is assigned, TypeScript defaults the type to `any`.

---

### 🔄 Changing Annotations Dynamically

Even if you remove type annotations, TypeScript still uses **type inference** to determine the variable’s type.

**Example with annotations:**
```typescript
let sales: number = 12345;
sales = 67890;  // Valid

// Removing annotation (type inference still works)
let sales = 12345;  // TypeScript knows `sales` is a number
sales = "string";   // Error: Type 'string' is not assignable to type 'number'
```

In the above example:
- Initially, `sales` is explicitly typed as `number`.
- After removing the type annotation, TypeScript still understands that `sales` is a `number` because of the value `12345` assigned at the start.

---

### 📌 Key Points

- **Basic JavaScript Types**: TypeScript builds on JavaScript’s core types, adding new functionalities and stronger type safety.
- **Type Inference**: TypeScript can automatically infer types based on the assigned values, making your code more concise without sacrificing type safety.
- **`any` Type**: While useful, the `any` type should be used cautiously as it bypasses type safety. Overusing it defeats the purpose of using TypeScript.

