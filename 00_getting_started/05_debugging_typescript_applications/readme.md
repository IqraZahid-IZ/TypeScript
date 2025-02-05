
# 🛠️ **Debugging TypeScript in VS Code**

Debugging is a vital skill for developers, allowing you to step through code, inspect variables, and quickly resolve issues. In this guide, we'll show you how to debug TypeScript applications in **Visual Studio Code** (VS Code), ensuring smooth and efficient debugging.

---

## 🎯 **What You’ll Need**

- **VS Code** installed on your machine.
- A **TypeScript project** with a configured `tsconfig.json`.
- The ability to **compile TypeScript** with `tsc`.

---

## 📝 **Step-by-Step Debugging Process**

### 1. **Write Some Sample Code**

In your `index.ts`, add a simple logic for debugging:

```typescript
let age: number = 20;

if (age < 15) {
    age += 10;  // Increase age if less than 15
} else {
    age -= 5;   // Decrease age otherwise
}

console.log("Updated age is:", age);
```

### 2. **Compile the Code**

Before debugging, compile the TypeScript file:

```bash
tsc
```

This generates the `index.js` file (or another output file based on your `outDir` in `tsconfig.json`).

### 3. **Open the Debug Panel**

1. Click on the **Run and Debug** icon in the Activity Bar or press `Ctrl+Shift+D` / `Cmd+Shift+D`.
2. If prompted, select **"Create a launch.json file"** and choose **Node.js** as the environment. This creates the `launch.json` file under `.vscode` directory.

### 4. **Configure `launch.json` for TypeScript**

Update your `launch.json` to debug TypeScript:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "program": "${workspaceFolder}/dist/index.js",  // Path to compiled JS
      "preLaunchTask": "tsc: build - tsconfig.json",  // Compile TS before debugging
      "outFiles": ["${workspaceFolder}/dist/**/*.js"], // Map TS to JS
      "sourceMaps": true  // Enable source maps for debugging
    }
  ]
}
```

**Key Settings:**
- **`program`**: Points to the compiled JavaScript file.
- **`preLaunchTask`**: Runs TypeScript compilation before debugging.
- **`sourceMaps`**: Ensures correct mapping from TypeScript to JavaScript for easier debugging.

### 5. **Set a Breakpoint**

1. Open `index.ts`.
2. Click to the left of the line number where you want the debugger to pause (red dot appears).

Example:

```typescript
if (age < 15) {
    age += 10;  // Add a breakpoint here
}
```

### 6. **Start Debugging**

- In the **Debug Panel**, select **Launch Program** and click the **green play button** or press `F5` to start debugging.

### 7. **Explore Debugging Tools**

Once the debugger pauses at the breakpoint, you can use the following tools:

- **Step Over (F10)**: Execute the current line and move to the next.
- **Step Into (F11)**: Dive into function calls to inspect further.
- **Step Out (Shift+F11)**: Exit the current function and return to the caller.
- **Restart (Ctrl+Shift+F5)**: Restart the debugging session.
- **Stop (Shift+F5)**: Stop debugging.

### 8. **Inspect and Modify Variables**

In the **Variables** pane on the left, you can:

- View the current values of variables (e.g., `age`).
- Add variables to the **Watch** pane to track their values dynamically.

### 9. **Refine Code and Debug Again**

Modify your code for more visibility, like so:

```typescript
let age: number = 20;

if (age < 15) {
    age += 10;
    console.log("Age after increment:", age); // Log for better observation
} else {
    age -= 5;
    console.log("Age after decrement:", age); // Log for better observation
}

console.log("Final age is:", age);
```

---

## 🌟 **Benefits of Debugging TypeScript**

- **Catch Errors Early**: TypeScript’s type system + debugging helps spot issues during development.
- **Clarity on Execution**: Step through code to understand logic and pinpoint bugs.
- **Faster Debugging**: Quickly identify and fix issues to improve productivity.



