# ToolinUp DevKit

## Overview
The **ToolinUp DevKit** automates the setup of a web development environment on Windows using **Scoop**. Instead of manually downloading and installing software, this bucket streamlines the process with simple commands.

## 🔧 Tools Available
The ToolinUp DevKit provides quick installation of essential development tools:

- **VS Code** – Lightweight and powerful code editor.
- **Git** – Version control system.
- **Composer** – PHP dependency manager.
- **Node.js** – JavaScript runtime.
- **PHP CLI** – Command-line interface for PHP.

## ⚙️ Installation

### 1️⃣ Install Scoop (if not already installed)
Open **PowerShell (Administrator)** and run:
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex
```

### 2️⃣ Add the ToolinUp DevKit Bucket
```powershell
scoop bucket add toolinup https://github.com/toolinup/devkit.git
```

### 3️⃣ Install Development Environments
Choose the setup that fits your workflow:

#### **Native Windows Setup**
```powershell
scoop install toolinup/win-env
```
Includes VS Code, Git, and Node.js.

## 🔍 Managing Packages

### List Added Buckets
```powershell
scoop bucket list
```

### Search for Packages
```powershell
scoop search toolinup
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
scoop install xampp
```

## 🔧 Additional Setup Steps

## 💡 Conclusion
The **ToolinUp DevKit** simplifies the setup of your development environment on Windows. Whether configuring VS Code, Git, or a full-stack LAMP environment, everything is just a command away.

Start automating your setup today!
## FAQs and Troubleshooting

### **General Questions**

#### ** What is ToolinUp DevKit?**
ToolinUp DevKit is a set of pre-configured development environments that automate software installation using **Scoop** on Windows. It provides **standalone Windows setups** (`win-env`) and **WSL-based environments** (`wsl-env` with optional add-ons).

#### ** Do I need to install Scoop before using ToolinUp DevKit?**
Yes, **Scoop** is required. Install it with:
```powershell
irm get.scoop.sh | iex
```

### **Installation & Setup**

#### ** How do I install a ToolinUp DevKit environment?**
First, add the ToolinUp bucket:
```powershell
scoop bucket add toolinup https://github.com/toolinup/devkit.git
```
Then install the desired environment. For example:
```powershell
scoop install toolinup/win-env
```

---

### **Usage & Troubleshooting**

#### ** How do I check if a package is installed?**
Run:
```powershell
scoop list
```

#### ** How do I update my installed environment?**
Use:
```powershell
scoop update *
```

#### ** How do I uninstall a ToolinUp environment?**
For example, to remove `win-env`:
```powershell
scoop uninstall toolinup/win-env
```

#### ** How can I install individual tools separately?**
You can install any package manually. Example:
```powershell
scoop install vscode
```

#### ** Why isn't my installed tool available in the command line?**
Try refreshing the environment:
```powershell
refreshenv
```
Or restart your terminal.

#### ** What happens if an installation fails?**
Check the error message. You can try:
```powershell
scoop uninstall <package>
scoop install <package>
```
Or manually remove and reinstall the environment.

---

### **Customization & Expansion**

#### ** Can I modify an environment after installation?**
Yes! You can manually install additional packages or customize configurations within WSL.

#### ** Can I contribute to ToolinUp DevKit?**
Absolutely! Contributions are welcome on GitHub. You can submit issues, improve manifests, or suggest new environments.

#### ** Will more environments be added in the future?**
Yes! Future plans may include **Rust, Go, or .NET environments** depending on community feedback.

