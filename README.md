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
