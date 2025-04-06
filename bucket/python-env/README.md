# Python Development Environment (python-env)

## Overview

The `python-env` setup is designed to provide a comprehensive development environment for Python developers, making it easier to work with Python projects on Windows using Scoop. It includes Python version management, dependency management tools, and other essential tools for Python development.

## Includes:

- **Python**: Python runtime for running Python applications and projects.
- **pyenv-win**: Python version manager for managing multiple versions of Python on Windows.
- **pipx**: A tool to install and run Python applications in isolated environments.
- **Poetry**: Dependency management and packaging tool for Python projects.

## Features:

- **Multiple Python Versions**: Install and manage different versions of Python using `pyenv-win`.
- **Isolated Python Apps**: Run Python applications in isolated environments using `pipx`.
- **Enhanced Dependency Management**: Manage dependencies, virtual environments, and packaging with `Poetry`.

## Installation

To get started, follow these steps:

1️⃣ **Install Scoop** (If not already installed)

First, make sure that Scoop is installed. If it’s not, follow the steps below:

```bash
irm get.scoop.sh | iex
```

If prompted about execution policy, enable it with:

```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

2️⃣ **Add the ToolinUp DevKit Bucket**

To install the `python-env` setup, add the ToolinUp DevKit bucket:

```bash
scoop bucket add toolinup https://github.com/ToolinUp/DevKit.git
```

3️⃣ **Install Python Development Environment**

Now, install the Python development environment using the following command:

```bash
scoop install toolinup/python-env
```

This will install the following tools:

- Python
- pyenv-win
- pipx
- Poetry

## Usage

Once installed, you can start using the Python environment.

### Managing Python Versions with `pyenv`

To install a new version of Python:

```bash
pyenv install 3.x.x  # Replace with the desired version
```

Set a global Python version:

```bash
pyenv global 3.x.x  # Replace with the version you want to set globally
```

### Using `pipx` to Install and Run Python Apps

To install a Python application using `pipx`:

```bash
pipx install <package-name>
```

### Dependency Management with `Poetry`

To initialize a new Python project with Poetry:

```bash
poetry init  # Follow the prompts to create a `pyproject.toml` file
```

To install dependencies:

```bash
poetry install
```

## Additional Setup

### Verifying Python Installation

After installation, verify the Python version with:

```bash
python --version
```

If `pyenv` is managing your versions, check the installed versions with:

```bash
pyenv versions
```

### Managing Virtual Environments with Poetry

To create a virtual environment for a project:

```bash
poetry new my-project
cd my-project
poetry install
```

## Notes

- After installing, you may need to restart your terminal for changes to take effect.
- Poetry will manage your dependencies and virtual environments, making Python development more streamlined.