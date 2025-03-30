# PHP Development Environment (php-env)

The PHP development environment setup for ToolinUp DevKit installs all the essential tools needed to work with PHP directly on Windows, helping you get started with PHP development quickly.

This setup uses [Scoop](https://scoop.sh) to install and manage the tools, ensuring that you have a lightweight and efficient PHP development environment.

## Features

- **PHP**: The latest PHP runtime for running PHP applications and projects.
- **Composer**: A dependency manager for PHP, essential for managing libraries and packages.
- **PHPUnit**: A framework for unit testing your PHP applications.
- **Xdebug**: A powerful debugger and profiler for PHP, helping with enhanced debugging capabilities.
- **Scoop**: A package manager for Windows, ensuring all dependencies are easily installed and managed.

## Prerequisites

Before installing `php-env`, you need to have [Scoop](https://scoop.sh) installed. If you haven't installed Scoop yet, follow these steps:

1. Open PowerShell (as Administrator) and run the following command:
    ```powershell
    irm get.scoop.sh | iex
    ```

2. If prompted, enable the execution policy by running:
    ```powershell
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

3. Verify the installation by running:
    ```powershell
    scoop --version
    ```

Once Scoop is installed, you can proceed with setting up `php-env`.

## Installation

To install `php-env`, follow these steps:

1. Add the ToolinUp DevKit bucket to Scoop:

    ```powershell
    scoop bucket add toolingup https://github.com/ToolinUp/DevKit
    ```

2. Install the PHP development environment:

    ```powershell
    scoop install php-env
    ```

This command will install the following tools:
- **PHP**
- **Composer**
- **PHPUnit**
- **Xdebug**

## Post-Installation Setup

1. **Verify PHP Installation:**
    Run the following command to check your PHP version:
    ```powershell
    php -v
    ```
    If everything is installed correctly, you should see the PHP version output.

2. **Configure Xdebug:**
    After installing Xdebug, you may need to configure it in your `php.ini` file. Follow the official [Xdebug documentation](https://xdebug.org/docs) for setup instructions.

3. **Composer Setup:**
    You can verify the installation of Composer by running:
    ```powershell
    composer --version
    ```

## Updating Your PHP Development Environment

To keep your `php-env` setup up to date, run:
```powershell
scoop update php-env
```

## Uninstalling PHP Environment

If you want to remove the PHP development environment, run:
```powershell
scoop uninstall php-env
```

This will remove PHP and all its related tools from your system.

## Notes

- After installation, you may need to manually configure some tools (e.g., PHP and Xdebug).
- If you're using a code editor like VS Code, consider installing PHP extensions for enhanced development experience.

For more information on using ToolinUp DevKit and setting up other environments, visit [ToolinUp.com](https://www.toolingup.com).

## Troubleshooting

If you encounter any issues during installation or usage, check the following:
- Ensure that Scoop is properly installed and updated.
- Verify that your system meets the prerequisites for each tool.
- For Xdebug-related issues, check the official [Xdebug documentation](https://xdebug.org/docs).

If you're still having trouble, feel free to open an issue on the [ToolinUp DevKit GitHub repository](https://github.com/ToolinUp/DevKit).