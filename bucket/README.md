# 📦 ToolinUp DevKit Manifests

The **ToolinUp DevKit** provides pre-configured development environments for Windows, WSL2, Containers, and more.  
Each environment is defined using a **Scoop manifest** and can be installed using **Scoop**.

## 📁 Available Environments

| Environment      | Description |
|-----------------|-------------|
| [`win-env`](./docs/win-env/README.md) | Native Windows development tools |
| [`wsl-env`](./docs/wsl-env/README.md) | WSL2-based Linux development setup |
| [`container-env`](./docs/container-env/README.md) | Docker and containerized development |
| [`python-env`](./docs/python-env/README.md) | Python runtime, package managers, and tools |
| [`php-env`](./docs/php-env/README.md) | PHP development stack with Composer |
| [`django-env`](./docs/django-env/README.md) | Django framework setup (requires `python-env`) |

## 🚀 How to Use These Manifests

### 1️⃣ **Add ToolinUp DevKit to Scoop**
Before installing any environment, add the ToolinUp DevKit Scoop bucket:
```sh
scoop bucket add toolingup https://github.com/ToolinUp/DevKit.git
```

### 2️⃣ **Install an Environment**
Pick an environment and install it:
```sh
scoop install <environment-name>
```
Example:
```sh
scoop install wsl-env
```

### 3️⃣ **Verify Installation**
Check installed tools:
```sh
scoop list
```

## 🛠 Managing Environments

### ✅ **Updating an Environment**
To update all installed environments:
```sh
scoop update *
```

### ❌ **Uninstalling an Environment**
```sh
scoop uninstall <environment-name>
```
Example:
```sh
scoop uninstall python-env
```

## 🔗 Learn More
For detailed setup instructions, visit the [ToolinUp DevKit documentation](https://www.toolingup.com).
