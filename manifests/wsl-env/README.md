# 🐧 WSL Development Environment (`wsl-env`)

The **WSL Development Environment (`wsl-env`)**  in the ToolinUp DevKit provides a sets up a **fully optimized WSL2 environment** for web development. It includes key tools to enhance performance, package management, and compatibility between Windows and Linux.

## 🚀 Features
✅ **WSL2** – Full Linux compatibility on Windows  
✅ **Ubuntu (Default Distro)** – A stable Linux distribution for development  
✅ **Windows Terminal** – Modern terminal with multiple tab support  
✅ **Git for Windows & WSL** – Version control for both environments  
✅ **fzf, zoxide, sudo** – Productivity enhancements for CLI navigation  

## 🛠 Installation

### **Prerequisites**
- Ensure you have added the **ToolinUp DevKit** bucket to Scoop:  
  ```sh
  scoop bucket add toolingup https://github.com/ToolinUp/DevKit.git
  ```

### **Install `wsl-env`**
```sh
scoop install wsl-env
```

### **Post-Installation Steps**
1️⃣ **Restart your system** to apply WSL changes.  
2️⃣ **Check WSL version**:
   ```sh
   wsl --list --verbose
   ```
   Ensure your distribution is running with **WSL2** (not WSL1).  
3️⃣ **Set Ubuntu as the default distro**:
   ```sh
   wsl --set-default Ubuntu
   ```

## 🔥 Why Use `wsl-env`?
- 🐧 **Full Linux development experience inside Windows**
- ⚡ **Performance optimizations for WSL2**
- 🔄 **Seamless interoperability between Windows & Linux**

## 🎯 Next Steps
- Install additional environments:  
  - **Python**: `scoop install python-env`  
  - **Django**: `scoop install django-env`  
  - **Containers**: `scoop install container-env`  
- Customize your WSL setup:  
  ```sh
  nano ~/.bashrc
  ```
- Use **Windows Terminal** for an improved CLI experience.

For more details, visit [ToolinUp DevKit Documentation](https://www.toolingup.com).  