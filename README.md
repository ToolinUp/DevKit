# ToolinUp DevKit

## Overview
The **ToolinUp DevKit** automates the setup of a web development environment on Windows using **Scoop**. Instead of manually downloading and installing software, this bucket streamlines the process with simple commands.

## 🔧 Tools Available
The ToolinUp DevKit provides quick installation of essential development tools:

- **VS Code** – Lightweight and powerful code editor.
- **Git** – Version control system.
- **XAMPP** – Local web server (Apache, MySQL, PHP).
- **Composer** – PHP dependency manager.
- **Node.js** – JavaScript runtime.
- **PHP CLI** – Command-line interface for PHP.

## ⚙️ Installation

### 1️⃣ Install Scoop (if not already installed)
Open **PowerShell (Administrator)** and run:
```powershell
irm get.scoop.sh | iex
```
If prompted about execution policy, enable it with:
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### 2️⃣ Add the ToolinUp DevKit Bucket
```powershell
scoop bucket add toolingup https://github.com/toolingup/devkit.git
```

### 3️⃣ Install Development Environments
Choose the setup that fits your workflow:

#### **Native Windows Setup**
```powershell
scoop install toolingup/win-env
```
Includes VS Code, Git, XAMPP, and Node.js.

#### **WSL2 (Ubuntu) Setup**
```powershell
scoop install toolingup/wsl-env
```
Configures WSL2 with Ubuntu and installs CLI tools.

#### **Docker Dev Containers Setup**
```powershell
scoop install toolingup/container-env
```
Installs Docker Desktop and related tools for containerized development.

## 📦 Package Details

| Package                  | Environment      | Installs |
|--------------------------|-----------------|----------|
| **toolingup/win-env**    | Windows         | VS Code, Git, XAMPP, Node.js |
| **toolingup/wsl-env**    | WSL2 (Ubuntu)   | Ubuntu, VS Code, Git, Node.js |
| **toolingup/container-env** | Docker Dev Containers | Docker Desktop, CLI tools |

## 🔍 Managing Packages

### List Added Buckets
```powershell
scoop bucket list
```

### Search for Packages
```powershell
scoop search toolingup
```

### List Installed Packages
```powershell
scoop list
```

### Update All Packages
```powershell
scoop update *
```

### Uninstall a Package
```powershell
scoop uninstall vscode
```

### Install Specific Tools
Example: Install XAMPP separately
```powershell
scoop install toolingup/xampp
```

## 🔧 Additional Setup Steps

### Ensure PHP CLI Works with XAMPP
If PHP CLI is not recognized, manually add XAMPP's PHP path:
```powershell
$env:Path += ";C:\xampp\php"
php -v
```
Now, PHP CLI commands will work inside the terminal.

## 💡 Conclusion
The **ToolinUp DevKit** simplifies the setup of your development environment. Whether configuring VS Code, Git, or a full-stack LAMP environment, everything is just a command away.

Start automating your setup today!
## FAQs and Troubleshooting

### **General Questions**  

#### **1️⃣ What is ToolinUp DevKit?**  
ToolinUp DevKit is a set of pre-configured development environments that automate software installation using **Scoop** on Windows. It provides **standalone Windows setups** (`win-env`) and **WSL-based environments** (`wsl-env` with optional add-ons).  

#### **2️⃣ What is the difference between `win-env` and `wsl-env`?**  
- **`win-env`** is for **native Windows development**, installing tools directly on Windows.  
- **`wsl-env`** sets up **WSL2 (Ubuntu)** for a Linux-like development workflow.  

Users should choose **`win-env`** if they want a pure Windows setup and **`wsl-env`** if they prefer working in a Linux-based environment.  

#### **3️⃣ Do I need to install Scoop before using ToolinUp DevKit?**  
Yes, **Scoop** is required. Install it with:  
```powershell
irm get.scoop.sh | iex
```

---

### **Installation & Setup**  

#### **4️⃣ How do I install a ToolinUp DevKit environment?**  
First, add the ToolinUp bucket:  
```powershell
scoop bucket add toolingup https://github.com/toolingup/devkit.git
```  
Then install the desired environment. For example:  
```powershell
scoop install toolingup/wsl-env
```

#### **5️⃣ Should I install `wsl-env` before installing `python-env`, `django-env`, or `container-env`?**  
Yes, `wsl-env` is a **prerequisite** for all add-on environments. Install it first before adding Python, Django, or containerized setups.  

#### **6️⃣ Can I install multiple environments at once?**  
Yes, you can mix and match environments. Example:  
```powershell
scoop install toolingup/wsl-env toolingup/python-env toolingup/container-env
```

#### **7️⃣ What if I already have WSL installed? Can I still use `wsl-env`?**  
Yes! If WSL is already installed, `wsl-env` will configure additional tools needed for development.  

---

### **Usage & Troubleshooting**  

#### **8️⃣ How do I check if a package is installed?**  
Run:  
```powershell
scoop list
```

#### **9️⃣ How do I update my installed environment?**  
Use:  
```powershell
scoop update *
```

#### **🔟 How do I uninstall a ToolinUp environment?**  
For example, to remove `wsl-env`:  
```powershell
scoop uninstall toolingup/wsl-env
```

#### **1️⃣1️⃣ How can I install individual tools separately?**  
You can install any package manually. Example:  
```powershell
scoop install toolingup/vscode
```

#### **1️⃣2️⃣ Why isn't my installed tool available in the command line?**  
Try refreshing the environment:  
```powershell
refreshenv
```
Or restart your terminal.

#### **1️⃣3️⃣ What happens if an installation fails?**  
Check the error message. You can try:  
```powershell
scoop uninstall <package>
scoop install <package>
```
Or manually remove and reinstall the environment.

---

### **Customization & Expansion**  

#### **1️⃣4️⃣ Can I modify an environment after installation?**  
Yes! You can manually install additional packages or customize configurations within WSL.

#### **1️⃣5️⃣ Can I contribute to ToolinUp DevKit?**  
Absolutely! Contributions are welcome on GitHub. You can submit issues, improve manifests, or suggest new environments.

#### **1️⃣6️⃣ Will more environments be added in the future?**  
Yes! Future plans may include **Rust, Go, or .NET environments** depending on community feedback.

---

### **Advanced Topics**  

#### **1️⃣7️⃣ When should I use `container-env` instead of `wsl-env`?**  
Use `container-env` if you want to work with **Docker and containerized development** instead of installing tools directly in WSL.

#### **1️⃣8️⃣ Can I use `win-env` and `wsl-env` together?**  
Yes, but it's best to **pick one as your primary environment** and install additional tools as needed.

#### **1️⃣9️⃣ Can I use this on a remote server?**  
`wsl-env` is designed for **local WSL setups**. If you're working on a remote machine, consider using **VS Code Remote SSH**.
