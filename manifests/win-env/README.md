# 🏁 Native Windows Development (`win-env`)

The **Windows Development Environment (`win-env`)** provides a **lightweight, optimized development setup for Windows** without WSL. It includes essential CLI tools to enhance productivity.

## 🚀 Features
✅ **Git** – Version control system  
✅ **Neovim** – Lightweight and customizable code editor  
✅ **7zip** – File archiving and extraction  
✅ **fzf** – Fuzzy file finder for faster navigation  
✅ **zoxide** – Smart `cd` alternative for jumping between directories  
✅ **Scoop** – Simplified package manager for Windows  

## 🛠 Installation

### **Prerequisites**
- Ensure you have added the **ToolinUp DevKit** bucket to Scoop:
  ```sh
  scoop bucket add toolingup https://github.com/ToolinUp/DevKit.git
  ```

### **Install `win-env`**
```sh
scoop install win-env
```

### **Post-Installation Steps**
1️⃣ **Restart your terminal** to apply environment changes.  
2️⃣ **Verify installed tools**:
   ```sh
   git --version
   nvim --version
   fzf --version
   ```

## 🔥 Why Use `win-env`?
- 🏁 **Optimized for native Windows development**
- 🔄 **Lightweight and fast installation**
- ⚡ **Includes essential CLI tools for productivity**

## 🎯 Next Steps
- Install additional environments:
  - **WSL2**: `scoop install wsl-env`
  - **Containers**: `scoop install container-env`
  - **Python**: `scoop install python-env`
- Customize **Neovim**:
  ```sh
  nvim ~/.config/nvim/init.vim
  ```
- Use **Scoop** to install more tools:
  ```sh
  scoop install <package-name>
  ```

For more details, visit [ToolinUp DevKit Documentation](https://www.toolingup.com).  