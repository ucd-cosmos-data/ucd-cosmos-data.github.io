---
title: "Lab02: Group Website"
author: "Wonjun Seo"
summary: "Hugo and Markdown"
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

1. Close all terminals and reopen **Terminal** (Mac) or **cmd** (Windows).
2. Type the following and press `Return`. If **Git** is successfully installed, then the version number will be displayed.
    ```
    hugo version
    ```

## II. Group Website
Every group will maintain a group website to archive projects.


### Clone

1. Move to (https://github.com/ucd-cosmos-data).
2. Click the "Repositories", and then click "<GROUP_NAME>" repository.
3. Click the green "<> Code" button, then copy URL.
4. Open the `cosmos/` directory in **VS Code**.
5. Press `` Ctrl+Shift+` `` to open the terminal.
6. Type `git clone --recurse-submodules `, paste the URL, then press `Return`. For example,
   ```bash
   git clone --recurse-submodules https://github.com/ucd-cosmos-data/<GROUP_NAME>.git
   ```
7. Move to `<GROUP_NAME>/` directory.
   ```bash
   cd <GROUP_NAME>
   ```
8. Run the following:
   ```bash
   hugo server
   ```
   This is the **local** preview server, before deployment.

The workflow for updating the group website is:

1. Edit the website (e.g. add pages or change config) on your own machine.
2. Preview your changes with `hugo server`.
3. Have other members review.
4. Deploy.
5. See the updated live website.

We will use **Git** for the Steps 3 and 4, which will be covered in tomorrow's Lab session. For the remaining today, we will learn how **hugo** builds the website and basic **Markdown** syntax.

### How It Works

#### Current Directory Structure

```
cosmos/
├── <GROUP_NAME>/                         # Group website repo
│   ├── .github/                          # GitHub config for building website. DO NOT edit this directory.
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
├── lecture/
│   └── ...
├── etc/
│   └── ...
└── ...
```

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
If you run into any issues with your website, don't hesitate to reach out. Just add me as a collaborator so I can take a look.