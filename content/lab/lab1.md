---
title: "Lab01: Software Setup"
author: "Wonjun Seo"
summary: "Git, VS Code, and Python"
---

> ⚠️ **Windows users**
> 
> Open **PowerShell** in **Administrator mode** throughout this lab. Right-click the PowerShell icon and select **Run as administrator**.

## Goal
In today's Lab session, we will:

- Install Git, VS code, and Python (via uv).
- Create a Github account and link it to VS code.
- Create a directory and a virtual environment for our course.

## I. Git
> **Git** is a version control system that tracks changes in your code and lets you collaborate with others without overwriting each other's work.

### Create a Github Account

- If you already have a **Github** account, go to [I.1](#i1-verify-your-installation).
- If not, go to <https://github.com> and create a new account.
    > ⚠️ Use your **primary** email address.
- All students will be invited to the Github Organization.

### Installation

#### Mac

1. Open **Terminal**.
2. Type the following and press `Return`. This command installs **Git** if you don't already have it, or upgrades it if you do.
    ```
    brew install git
    ```

#### Windows

1. Open **PowerShell**.
2. Type the following and press `Enter`. This command installs **Git** if you don't already have it, or upgrades it if you do.
    ```
    winget install --id Git.Git -e --source winget
    ```

#### After installation (Mac and Windows)

1. Close all terminals and reopen **Terminal** (Mac) or **cmd** (Windows).
2. Type the following and press `Return`. If **Git** is successfully installed, then the version number will be displayed.
    ```
    git --version
    ```

### Git Configuration

- Open **Terminal** (Mac) or **cmd** (Windows).
- Set your name: `git config --global user.name <NAME>`.
- Set your email: `git config --global user.email <EMAILADDRESS>`. Here, `<EMAILADDRESS>` should be your **github account email**.
- Set default name of branch `git config --global init.defaultBranch main`. Now, the first branch is **main**.
- To check your configuration: `git config --list`. Press `q` to exit.

## II. VS Code
> **VS Code (Visual Studio Code)** is a free, lightweight code editor made by Microsoft that supports virtually every programming language and can be extended with thousands of plugins.


You may skip this section if all the following are already done before:
1. you have VS Code in your computer.
2. you can see your Github account by clicking the profile icon at the bottom left of VS Code.
3. you already have `Python` and `Jupyter` extensions on VS Code.

If you are not sure about any of these, please follow the instruction accordingly.

### IInstallation

#### Mac

1. Open **Terminal**.
2. Type the following and press `Return`.
    ```
    brew install --cask visual-studio-code
    ```

#### Windows

1. Open **PowerShell**.
2. Type the following and press `Enter`.
    ```
    winget install Microsoft.VisualStudioCode
    ```

#### After installation (Mac and Windows)

1. Close all terminals and reopen **Terminal** (Mac) or **cmd** (Windows).
2. Type the following and press `Return`. If **VS Code** is successfully open, you're done.
    ```
    code .
    ```

### Link to Github

1. Open **VS code**.
2. Click the profile icon at the bottom left.
3. Click `Backup and Sync Settings`.
4. Click `Sign in`, then choose `Sign in with Github` and follow instructions.
5. *(Optional)* Activate **Github Copilot**.

### Extensions
- Click the extension icon on the left sidebar.
- Search and install `Python` and `Jupyter` extensions.

## III. Python (uv)
> **uv** is a fast Python package and project manager.

Before starting, create a directory `cosmos` wherever you prefer. Throughout the summer school, everyone will have the same directory structure to prevent any path conflicts. For now, create subdirectories as follows:

```
cosmos/
├── lecture/
|   ├── notes/          # Put lecture notes here
|   │   └── ...
|   └── code/           # Put code files provided in lectures here
|       └── ...
├── lab/                # Put lab materials here
|   └── ...
└── etc/                # Misc files
    └── ...
```

Later on, we will add more subdirectories.

### Install **uv**

#### Mac

1. Open **Terminal**.
2. Type the following and press `Return`. This installs **uv**.
    ```
    brew install uv
    ```

#### Windows

1. Open **PowerShell**.
2. Type the following and press `Enter`.
    ```
    winget install --id=astral-sh.uv  -e
    ```

#### After installation (Mac and Windows)

1. Close all terminals and reopen **Terminal** (Mac) or **cmd** (Windows).
2. Type the following and press `Return`. If **uv** is successfully installed, the version number will be displayed.
    ```
    uv --version
    ```

### Download Configuration Files

Download the following two files and place them directly inside your `cosmos/` directory:

- <a href="/files/pyproject.toml" download="pyproject.toml">pyproject.toml</a>
- <a href="/files/uv.lock" download="uv.lock">uv.lock</a>

These files specify the Python version and all required packages for the course.

### Setup Python and Virtual Environment

1. Open **Terminal** (Mac) or **cmd** (Windows) at the `cosmos/` directory.
2. Run the following command. **uv** will automatically install the correct Python version and all required packages based on the configuration files you downloaded.
    ```
    uv sync
    ```
3. Open `cosmos/` directory in **VS Code**.
4. Create a new file named `test.ipynb` inside `cosmos/`.
5. Click **Select Kernel** at the top right, then choose **Python Environments** → select `.venv` (the one inside your `cosmos/` directory).
6. In the first cell, type the following and press `Shift+Return` to run:
    ```python
    print("Hello, World!")
    ```
    If `Hello, World!` is printed below the cell, your setup is complete.

> ⚠️ Some lecture code may not run properly due to deprecations. If you run into any issues, please let me know so we can update it.

### How To Add/Remove Packages

If you want to add packages that aren't included in our environment, follow the steps below:

1. Open the `cosmos/` directory in **VS Code**.
2. Press `` Ctrl+Shift+` `` to open the terminal.
3. Run:
   ```bash
   uv add <PACKAGE_NAME>
   ```
   Refer to [PyPI](https://pypi.org) to find the package name.
4. To remove the package,
   ```bash
   uv remove <PACKAGE_NAME>
   ```

### Current Directory Structure
```
cosmos/
├── lecture/
|   ├── notes/
|   │   └── ...
|   ├── code/
|   │   └── ...
|   ├── lab/
|   │   └── ...
│   └── ...
├── etc/
│   └── ...
├── test.ipynb
├── .venv/
├── .python-version
├── pyproject.toml
└── uv.lock
```

## Tomorrow

In tomorrow's lab session, we will create group website and learn Markdown syntax.