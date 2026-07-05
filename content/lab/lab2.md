---
title: "Lab02: Group Website"
author: "Wonjun Seo"
summary: "Hugo and Markdown"
draft: true
---
## Goal
In today's Lab session, we will:

- Create a group website with hugo.
- Learn Markdown Syntax.

## I. Hugo

> Hugo is a fast, open-source static site generator that builds websites from **Markdown** files.

#### Mac

1. Open **Terminal**.
2. Type the following and press `Return`.
    ```
    brew install hugo
    ```

#### Windows

1. Open **PowerShell**.
2. Type the following and press `Enter`.
    ```
    winget install Hugo.Hugo.Extended
    ```

#### After installation (Mac and Windows)

1. Close all terminals and reopen **Terminal** (Mac) or **PowerShell** (Windows).
2. Type the following and press `Return`. If **Git** is successfully installed, then the version number will be displayed.
    ```
    hugo version
    ```

## II. Group Website
- Every group will maintain a group website to archive its projects.
- Your group website is available at `https://ucd-cosmos-data.github.io/26-<GROUP_NAME>`. You can also find it from the [course website](https://ucd-cosmos-data.github.io/project/)
- This site is built with Hugo and hosted on Github Pages.

### Clone

1. Move to [Github Organization page](https://github.com/ucd-cosmos-data).
2. Click the "Repositories", and then click "<26-GROUP_NAME>" repository.
3. Click the green "<> Code" button, then copy URL.
4. Open the `cosmos/` directory in **VS Code**.
5. Press `` Ctrl+Shift+` `` to open the terminal.
6. Type `git clone --recurse-submodules `, paste the URL, then press `Return`. For example,
   ```bash
   git clone --recurse-submodules https://github.com/ucd-cosmos-data/26-<GROUP_NAME>.git
   ```
7. Move to `26-<GROUP_NAME>/` directory.
   ```bash
   cd 26-<GROUP_NAME>
   ```
8. Run the following:
   ```bash
   hugo server
   ```
   Find the following in the output:
   ```
   Web Server is available at http://localhost:<NUMBERS>/26-<GROUP_NAME>
   ```
9. Copy `https://localhost:<NUMBERS>/26-<GROUP_NAME>`, paste it to the web browser, then press `Return`. This is the **local** preview server, before deployment.
10. Go back to the Terminal tab in VS Code, and press `Ctrl + C` to stop.

The workflow for updating the group website is:

1. Edit the website (e.g. add pages or change config) on your own machine (**local**).
2. Preview your changes with `hugo server`.
3. Have other members review.
4. Deploy (**public**).
5. See the updated live website at `https://ucd-cosmos-data.github.io/26-<GROUP_NAME>`.

The `26-<GROUP_NAME>/.git/` directory connects your local repo to the remote repo, which makes Steps 3 and 4 possible. We will learn more about this in tomorrow's lab session. For the rest of today, we will learn how **Hugo** builds the website and basic **Markdown** syntax.

### How It Works
**Current Directory Structure**

```
cosmos/
├── 26-<GROUP_NAME>/
│   ├── .git                              # Git. It is hidden in VS Code.
│   │   └── ...
│   ├── .github/                          # GitHub config for building website
│   │   └── ...
│   ├── content/                          # Markdown content (pages, posts)
│   │   └── ...
│   ├── layouts/                          # Custom templates that override the theme (optional)
│   │   └── ...
│   ├── static/                           # Static assets served as-is (images, PDFs, favicon, htmls)
│   │   └── ...
│   ├── themes/                           # Hugo themes; PaperMod lives here (themes/PaperMod/)
│   │   └── ...
│   ├── ...
│   ├── .gitignore                        # Contains list of files that git ignores
│   ├── hugo.yaml                         # Website config (baseURL, theme, menus, params)
│   └── README.md                         # Repo description
├── .venv/
│   └── ...
├── lab/
|   └── ...
├── lecture/
|   └── ...
├── etc/
|   └── ...
└── ...
```

- Hugo reads the **Markdown** files in `content/` and converts each one into an HTML page.
- `layouts/` and `themes/` provide the templates that decide how that content is displayed (e.g. header, footer, page style).
- `static/` files (images, PDFs, etc.) are copied over as-is, without any conversion.
- `hugo.yaml` controls site-wide settings (title, menus, theme selection, etc.) that apply across all pages.
- Running `hugo server` combines all of this and serves a live preview of the site locally.

## II. Markdown

- <a href="/files/Markdown.md" download="Markdown.md">Markdown.md</a>

## III. Make yours!

Since we haven't covered **Git** yet, please update the group website directly through the GitHub webpage instead.
Please follow the instructions.

### Assignments
- Update the `hugo.yaml` file.
  - To change the profile photo on the homepage, upload the image to the `static/` directory and update the `imageUrl` field in `hugo.yaml`.
- Update the `README.md` file.
- Update the **Members** tab.
  - Add each member's name and a short introduction. To include photos, upload the image files to the `static/members/` directory, then reference the correct file names in `content/members/_index.md`.
- **(Optional)** If you'd like to change the theme, pick one from [gohugothemes.com/popular/free](https://www.gohugothemes.com/popular/free/) and let me know by this Saturday. I can apply it over the weekend.

#### Need help?
If you run into any issues with your website, don't hesitate to reach out!
