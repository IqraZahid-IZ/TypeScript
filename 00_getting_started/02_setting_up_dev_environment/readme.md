
# 🚀 **Setting Up TypeScript on Your Machine**

Ready to dive into TypeScript? Let’s get your development environment set up so you can start coding! 🌐

## 🔧 **Prerequisites**

Before starting, you’ll need **Node.js** installed on your machine to use **npm** for installing TypeScript.

### ✅ **Check if Node.js is Installed:**
1. Open your terminal (Command Prompt, PowerShell, or iTerm).
2. Run:  
   ```bash
   node -v
   ```
   - If you see a version number (e.g., `v16.18.0`), Node.js is installed! 🎉
   - If not, head over to the [Node.js official website](https://nodejs.org/) and install it.

---

## 📥 **Install the TypeScript Compiler**

Once Node.js is ready, follow these steps to install TypeScript globally on your system:

1. Open your terminal and run:  
   ```bash
   npm i -g typescript
   ```
   This installs TypeScript globally! 🌍
2. Verify the installation by running:  
   ```bash
   tsc -v
   ```
   If you see a version number (e.g., `Version 5.7.2`), TypeScript is good to go! 🎉

---

## 🖥️ **Choosing an IDE**

For this course, we’ll use **Visual Studio Code (VS Code)** – a popular, easy-to-use editor.

1. Download **VS Code** from the [official website](https://code.visualstudio.com/).
2. Install and launch it.

---

## 🛠️ **Configuring VS Code for TypeScript**

### 1. **Install the TypeScript Extension:**
- Open VS Code.
- Go to the Extensions Marketplace (click the square icon or press `Ctrl+Shift+X`).
- Search for **"TypeScript Language Features"** and install it. 🔍

### 2. **Create a New Project:**
- Create a new folder for your TypeScript projects.
- Open it in VS Code (File → Open Folder).
- Create a new `.ts` file, e.g., `index.ts`.

### 3. **Compile TypeScript Code:**
- Open the terminal in VS Code and navigate to your project folder:
  ```bash
  cd path/to/your/project
  ```
- Compile your `.ts` file:
  ```bash
  tsc index.ts
  ```
  This generates a `index.js` file, which you can run with Node.js.

---

## 📦 **Important Notes:**

- **Version Compatibility**: Don’t worry if your TypeScript version differs from this guide. The core concepts stay the same. 🌟
- Use `tsc -v` anytime to check your TypeScript version.

---
