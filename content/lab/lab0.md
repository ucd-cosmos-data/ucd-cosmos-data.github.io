---
title: "Lab00: Package Manager"
author: "Wonjun Seo"
summary: "Homebrew and Winget"
---

## macOS -- Homebrew
> **Homebrew** is the standard command-line package manager for macOS that lets you install software with a single command (e.g., `brew install <PACKAGE_NAME>`) instead of downloading installers from websites.

If you already have **Homebrew** on your Mac, no further steps are required.

### Installation

[Youtube Guide](https://youtu.be/ODVaw70G0ko?si=cfgw3FbKtnGf-iIz) 0:00~2:00.

1. Open **Terminal**.
2. Install **Homebrew**: type the following and press `Return`.

   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

   > ⚠️ If this is your first time using Terminal, you may be prompted to install **Xcode Command Line Tools**. This can take 10–20 minutes depending on your internet connection.

   > ⚠️ Homebrew requires administrator (`sudo`) access. You will be prompted to enter your Mac login password. Nothing will appear on screen as you type — this is normal. If your Mac has no password set, please create one before proceeding.

3. (**YOU MUST DO THIS**) When installation finishes, look for a **Next steps** section in the output. Copy and run the commands listed there (these add **Homebrew** to your PATH).
4. After installation, type the following and press `Return`. If **Homebrew** is successfully installed, then the version number will be displayed.

   ```
   brew --version
   ```

## Windows -- winget
> **Winget** is Windows' built-in command-line package manager that lets you install software with a single command (e.g., `winget install <PACKAGE_NAME>`) instead of downloading installers from websites.

**Winget** comes pre-installed on Windows 10/11.

1. Open **PowerShell**.
2. Type the following and press `enter`.
   ```
   winget --version
   ```

3. If the version number is displayed, **winget** is ready to use. If you get an error, install **App Installer** from the Microsoft Store ([link](https://apps.microsoft.com/detail/9nblggh4nns1?hl=en-US&gl=US)).