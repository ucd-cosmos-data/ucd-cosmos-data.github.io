---
title: "Lab03: Collaboration"
author: "Wonjun Seo"
summary: "GitHub Collaboration and Workflow"
draft: true
---
**VS Code Extensions**
Install **GitHub Pull Requests** and **GitLens** extensions.

## I. GitHub Collaboration

### Quick Overview

- **Repository (Repo)**: A project's folder tracked by Git, containing all files and their full history of changes.
- **Remote repo**: The copy of the repository hosted on **GitHub**, shared with your team.
- **Local repo**: The copy of the repository on your own computer, where you make and test changes.
- **Clone**: Download a copy of a remote repository to create your local repository.
- **Branch**: A separate line of development.
- **`main`**: The official, stable branch of the project that everyone works from.
- **Stage**: Mark specific changed files to be included in your next commit.
- **Commit**: Save your staged changes as a snapshot in your local repository, along with a message describing what changed.
- **Push**: Upload your local commits to the remote repository.
- **Pull**: Download and merge changes from the remote repository into your local repository.
- **Sync**: A combined pull + push. It first pulls any new remote changes, then pushes your local commits. This is what VS Code's **Sync Changes** button does.
- - **Fetch**: Download new changes from the remote repository without merging them into your local branch.
- **Merge**: Combine the changes from one branch into another, e.g. bringing your branch's changes into `main`.
- **Pull Request (PR)**: A request to merge one branch into another, giving teammates a chance to review the changes before they're merged.
- **Conflict**: Happens when Git can't automatically combine changes. It must be resolved manually before merging can continue.

> **IMPORTANT**: The first thing you should do whenever you open a repo is click **Sync Changes** to make sure `main` is up to date.

### File Status Markers

- U: Untracked (new file not yet added to the repository)
- M: Modified
- D: Deleted

### Practice
Let's practice with our group website repo!

- <a href="/files/git.pdf" download="git.pdf">git.pdf</a>

**Summary**

If you have a new task to complete, follow the steps below:
1. Switch to the `main` branch and click **Sync Changes**.
2. Create a new branch.
3. Make changes, commit changes, and sync changes.
4. Open a Pull Request to merge into `main`.
5. Review & update.
6. Merge by approving the Pull Request.
7. Delete the new branch.

### Conflict
If you encounter a merge conflict or any other Git issues, ask your TA for help immediately.


### Website Repo
However, we don't need to strictly follow the guideline above for the website repo. As long as only one person works on the website repo at a time, you can work directly on the `main` branch. Even so, make sure to sync the `main` branch before starting.

## II. Workflow
In lecture, we learned about the Data Science Pipeline. Today, each group will design a custom Git workflow for their project.

> **IMPORTANT**: **DO NOT** push to the `main` branch directly!

Any changes to the main branch must go through a separate branch and a pull request.

With this rule in mind—and using the workflow pipeline we discussed in the lecture—discuss the following questions with your group:

- When to create a new branch
- What types of work should be done within that branch
- When to merge the branch back into the main workflow

After your internal group discussion, each group will present their strategy to the class. Other groups will then provide feedback and suggestions.

Through this activity, each group is expected to gain a clearer understanding of the overall workflow of the project.

## III. Getting Started
We are now ready to start! Throughout the course, each group will work on several mini projects and the final project. Again, every group will use exactly the same directory structure to avoid conflicts. To do so, we will clone the `26-<GROUP_NAME>-analysis` repo from our GitHub Organization.

### Clone

1. Go to the [GitHub Organization page](https://github.com/ucd-cosmos-data).
2. Click **Repositories**, then select the `26-<GROUP_NAME>-analysis` repository.
3. Click the green **<> Code** button, then copy the URL.
4. Open the `cosmos/` directory in **VS Code**.
5. Press `` Ctrl+Shift+` `` to open the terminal.
6. Type `git clone `, paste the URL, then press `Return`. For example,
   ```bash
   git clone https://github.com/ucd-cosmos-data/26-<GROUP_NAME>-analysis.git
   ```

#### Current Directory Structure

```
cosmos/
├── 26-<GROUP_NAME>-analysis/
│   ├── .git/
│   │   └── ...
│   ├── proj1/
│   │   ├── data/
│   │   │   ├── cleaned/
│   │   │   ├── processed/
│   │   │   └── raw/
│   │   ├── models/
│   │   ├── notebooks/
│   │   ├── results/
│   │   │   └── figures/
│   │   └── README.md
│   ├── proj2/
│   │   └── ...
│   ├── .gitignore
│   └── README.md
├── 26-<GROUP_NAME>/
│   └── ...
├── .venv/
│   └── ...
├── lab/
│   └── ...
├── lecture/
│   └── ...
├── etc/
│   └── ...
└── ...
```

Whenever you start a new project, create a new directory with the same structure.
> ⚠️ Even creating a new directory may result in Git conflict. Make sure that only one person of the group creates the directory, and the others sync it to update.


Start your analysis NOW!