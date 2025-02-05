
# 🚀 **Creating and Compiling Your First TypeScript Project**

Ready to create your first TypeScript project? Let's get started by setting up the project folder, writing TypeScript code, compiling it, and running it! 🌟

---

## 📂 **Step 1: Set Up Your Project Folder**

1. **Create a New Folder**  
   Navigate to your preferred location and create a project folder (e.g., `hello-world`):  
   ```bash
   mkdir hello-world  
   cd hello-world
   ```

2. **Open the Folder in VS Code**  
   - Drag and drop the folder into **Visual Studio Code**.  
   - Or open it from the terminal:  
     ```bash
     code .
     ```

---

## 📝 **Step 2: Writing Your First TypeScript File**

1. **Create a New TypeScript File**  
   Inside the folder, create a file named `index.ts`.

2. **Add Basic TypeScript Code**  
   Open `index.ts` and add the following code:

   ```typescript
   let age: number = 25;  // Declaring `age` as a number
   console.log("Hello, brother! Your age is:", age);
   ```

   **Key Points:**  
   - **Type Annotation** ensures `age` is a number.  
   - TypeScript will throw an error if you assign a string to `age`.

---

## 🖥️ **Step 3: Compile and Run Your TypeScript Code**

1. **Open the Terminal**  
   In VS Code, go to **View → Terminal** or press `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac).

2. **Compile the TypeScript Code**  
   Run the following command to compile `index.ts` into JavaScript:  
   ```bash
   tsc index.ts
   ```

3. **Run the Compiled JavaScript**  
   Use Node.js to run the compiled `index.js`:  
   ```bash
   node index.js
   ```

   **Output:**  
   ```bash
   Hello, brother! Your age is: 25
   ```

---

## 💡 **Why Use TypeScript?**

- **Static Typing**: Ensures variables like `age` are used correctly, avoiding errors during development.
  - **Example Error**: `Type 'string' is not assignable to type 'number'.`
  
- **Compile-Time Error Detection**: Catch bugs early before they hit runtime, saving you time and reducing errors.

- **JavaScript Compatibility**: TypeScript compiles to plain JavaScript, ensuring compatibility with all modern browsers and environments.

---
