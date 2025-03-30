# Django Development Environment (django-env)

The ToolinUp Django Development Environment (django-env) provides a pre-configured setup for Django web development. It installs all the essential tools and dependencies you need to start building Django applications on your local machine.

## Overview

This environment is built on top of the ToolinUp DevKit, designed for Python and Django developers. It includes:

- Python and pip for managing packages
- Virtualenv to create isolated environments for your Django projects
- Django, the web framework for Python
- PostgreSQL adapter (`psycopg2`) for Django with PostgreSQL (if you are using PostgreSQL as your database)
- Node.js (for handling front-end dependencies in modern Django projects)
- Git for version control
- Scoop for managing installations on Windows

## Prerequisites

- **Scoop**: The ToolinUp DevKit uses Scoop to manage software installation. Make sure you've already installed Scoop on your system.

If you don't have Scoop installed, follow the instructions on the [ToolinUp DevKit Installation Guide](https://www.toolingup.com) to install it.

## Installation

1. **Install ToolinUp DevKit**: If you haven't done so already, follow the ToolinUp DevKit installation steps.
   - Install Scoop.
   - Add the ToolinUp DevKit bucket:  
     ```bash
     scoop bucket add toolingup https://github.com/ToolinUp/DevKit
     ```

2. **Install Django Environment**:
   Run the following command to install the `django-env` environment:
   ```bash
   scoop install django-env
   ```

3. **Set up Virtual Environment**:
   After installation, you’ll need to create a virtual environment for your Django project:
   ```bash
   python -m venv myenv
   ```

4. **Activate the Virtual Environment**:
   - **On Windows**: 
     ```bash
     .\myenv\Scripts\activate
     ```
   - **On WSL** (if you are using WSL): 
     ```bash
     source myenv/bin/activate
     ```

5. **Install Django and Dependencies**:
   Inside the virtual environment, install Django and any other dependencies for your project:
   ```bash
   pip install django
   ```

6. **Start Your Django Project**:
   Create a new Django project by running:
   ```bash
   django-admin startproject myproject
   ```

## Tools Included

The `django-env` installation includes the following tools:

- **Python**: The programming language for Django.
- **pip**: Python's package manager for installing dependencies.
- **virtualenv**: Tool to create isolated Python environments.
- **Django**: The web framework for building web applications in Python.
- **psycopg2**: PostgreSQL adapter for Python (if you plan to use PostgreSQL as your database).
- **Git**: Version control to manage your code.
- **Node.js**: For handling front-end dependencies, like in modern Django projects using Webpack or other tools.
- **Scoop**: The Windows package manager to manage the installation of the tools.

## Notes

- After installation, you may need to configure Neovim or other tools as needed (if you’re using them).
- If you're using PostgreSQL, make sure to install and configure it on your system.
- Don’t forget to install any other necessary Python packages for your Django project using `pip`.

## Next Steps

- [Learn Django](https://www.djangoproject.com/start/)
- [Get Started with Virtual Environments](https://realpython.com/python-virtual-environments-a-primer/)
- [Explore Scoop's Documentation](https://scoop.sh/)

## FAQ

**Q1: Can I use this environment with other databases besides PostgreSQL?**

A1: Yes, you can modify the environment to include connectors for other databases like MySQL, SQLite, etc. Just install the necessary dependencies using `pip`.

**Q2: Can I use this setup with WSL?**

A2: Absolutely! The setup works seamlessly in WSL as well. Just make sure to follow the steps to create a virtual environment and activate it inside WSL.

---

For more details, visit the [ToolinUp DevKit Documentation](https://www.toolingup.com).