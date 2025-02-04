🚀 **Creating and Compiling Your First TypeScript Project**  
In this section, we’ll guide you through the process of creating your first TypeScript project, compiling your code, and learning the basics of type annotations. Let’s take it step by step! 🌟

📂 **Step 1: Set Up Your Project Folder**  
1. **Create a New Folder**  
   - Navigate to your Desktop (or another location of your choice).  
   - Create a folder for your project, for example, `hello-world`:  
     `mkdir hello-world`  
     `cd hello-world`  
   - You can name the folder whatever you like and place it wherever you prefer on your machine.  

2. **Open the Folder in VS Code**  
   - Drag and drop the folder into the Visual Studio Code window.  
   - Alternatively, you can open it through the terminal using:  
     `code .`  

📝 **Step 2: Writing Your First TypeScript File**  
1. **Create the TypeScript File**  
   - Inside the folder you just created, create a new file named `index.ts`. This will be your main TypeScript file.  

2. **Write Basic Code**  
   - Open `index.ts` and add the following code:

     ```typescript
     let age: number = 25;  // Declaring the `age` variable as a number
     console.log("Hello, brother! Your age is:", age);
     ```

   **Key Points:**  
   - **Type Annotation:** `let age: number` ensures that `age` is only assigned a number.  
   - **Type Safety:** If you try to assign a string to `age`, like `age = "twenty-five"`, TypeScript will throw an error:  
     `Type 'string' is not assignable to type 'number'.`

🖥️ **Step 3: Compile TypeScript Code**  
1. **Open the Terminal**  
   - In VS Code, go to the View menu and select **Terminal** (shortcut: `Ctrl + ~` on Windows/Linux or `Cmd + ~` on Mac).  

2. **Compile the TypeScript File**  
   - Use the TypeScript compiler (`tsc`) to compile `index.ts`:  
     `tsc index.ts`  
   - This will generate an `index.js` file in the same folder. The `index.js` file will contain plain JavaScript that browsers or Node.js can run.

3. **Run the Compiled JavaScript Code**  
   - Run the JavaScript file using Node.js:  
     `node index.js`  
   - **Output:**  
     `Hello, brother! Your age is: 25`

💡 **Why Use TypeScript?**  
- **Static Typing for Safety**  
   - The `let age: number` declaration ensures the variable `age` can only store numbers. If you try to assign a value of a different type (like a string), TypeScript will catch the error before the code runs.
   
   **Example Error:**  
   `Type 'string' is not assignable to type 'number'.`

- **Compile-Time Error Detection**  
   - TypeScript helps detect potential errors early during development, which reduces the chances of runtime bugs and saves time.

- **JavaScript Compatibility**  
   - TypeScript code is ultimately compiled into plain JavaScript, which can run on all modern browsers and environments, ensuring compatibility across platforms.