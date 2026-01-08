# Guide to Adding Docs

## Overview

This document provides step by step guidance for creating docs in this repository for the QAT standards.

## Required Software

You will need to have the following installed to work with the docs effectively, all are available on service now):

- github desktop
- vscode

### Optional Software

You do not need these software components, but you can also install them as it may help deal with specific problems:

- git (it's called `GIT (x64)` on service now)

### Unavailable Software

Ideally, you'd have these installed as well:

- nodejs
- docker

However, `docker` isn't installable on UKHSA laptops, and `nodejs` is installable but only an old version which doesn't work with our code.

You can still edit documentation in this repo without these components, but it will make it harder.

## Required Access

You will need access to the `ukhsa-collaboration` org and you will need to be added to the [`qat-standards-contributors`][1] team.
This should give you access to the `standards-qat` repository (i.e. the repository this file is in).

## Setup your dev environment

### Clone the Code

To access the code you can use github desktop (you can also use the `git` command line program if you have it installed, see optional software above).

To clone the [repository][2] with github desktop you can follow the github guide to [authenticate][3] and then [clone][4] the repository.

This should mean you now have the repository on your laptop.

### Install a VS Code Extension

To make it possible to get a simple preview of the page you're editing, you can use a VS Code extension.

You will need to install this:

1. Open Visual Studio Code.
1. On the leftside of the window, click on the *"Extensions"* button (yours may not look exactly like this):

![vscode extensions][5]

3. This should open a tab with a search bar at the top, in the search bar, search for `markdown-all-in-one`

![vscode extensions][6]

4. Click on the *"Install"* button. If asked whether you trust the publisher, click *"Trust Publisher & Install"*.
   The extension will now be installed, and you can close the main tab it has opened.
   Click on the *"Explorer"* button to get back to the project (yours may not look exactly like the below image).

![vscode extensions][7]

## Work With the Documentation

All documentation and related assets must be placed in the `docs/` directory.

Within this directory there must be:

- `standards-qat.11tydata.json`
- `index.md`

These two files must be present in this docs folder for the site to work.
You shouldn't need to edit the `standards-qat.11tydata.json` file unless you want to change the layout of the site.

The `index.md` is the home page of the QAT standards site.

## Making Changes

Due to limitations with the UKHSA laptops and the software you are able to install (you can't install the `package.json`
and therefore can't run the pre-commit scripts...), all changes that you make will be stored in the `dev` branch of the
repository, and then we will merge these into the `main` branch periodically after checking and formatting the changes
to adhere to our required standards.

This means we will follow the [GitHub flow][8] but using the `dev` branch as the *base branch* instead of `main`.

### Opening the Project

1. Click on the *"Fetch origin"* button at the top to ensure you have the latest changes on your laptop.

![fetch origin][9]

2. Ensure the *"Current branch"* button at the top shows that you are on the `dev` branch.
   If it doesn't, click on it and select `dev`. If `dev` isn't listed, select `origin/dev`.

![dev branch selection][10]

3. To create a new branch for your changes, click the *"Current branch"* button from the previous step and then click
   the *"New branch"* button. In this popup:

   - enter a name for your branch, it **must** start with `qat-` and should describe the changes you're going to make
   - you **must** select `dev` as the *base branch*

   Click create once you have done this.

![create a branch][11]

4. This should have changed the *"Current branch"* at the top to your branch, and the button next to it should now say
   *"Publish branch"* instead of *"Fetch origin"*:

![branch change][12]

5. To start making changes, click on the *"Open in Visual Studio Code"*, this will launch VS Code:

![vscode][13]

6. With the *"Explorer"* tab selected, you should see all the files in the respository:

![create a branch][14]

### Editing a Page

1. Expand the `docs` directory and click on the file (e.g. `index.md` in the image below):

![edit a file][15]

2. To preview any markdown file to see how the formatting will be rendered, press `ctrl-k` and then `v`.
   Making changes on the left in the markdown will immediately be presented on the right to show you how it looks.
   This isn't an exact match to the way it will be rendered on the website, however, it is the best we can do without
   docker installed.

![preview an md file][16]

### Creating a Page

1. To create a new page, right-click on the `docs` directory and click *"New File..."*.

![new page][17]

2. You can call your file anything as long as it doesn't have spaces and ends with the markdown file extension: `.md`.
   At the top of the file you have now opened, you will need to add what is called *front matter*.
   This *front matter* defines metadata about the page and must be included on every page.
   The *front matter* must be defined between two sets of `---` and takes the form of `<key>: <value>` pairs.
   For example, the index page has this *front matter*:

![front matter][18]

Note that this *front matter* isn't rendered in the preview tab.

3. Your page won't need as much *front matter* as this as all you need to provide is an `order` value.
   This defines the order in which the page appears in the left hand navigation bar, for example on the live development
   standards website:

![dev standards side bar][19]

the *Environments* page at the top of the list has `order: 2` in its *front matter*, and the *Source control* page
next on the list has `order: 3` and so on.
The `index.md` page must have `order: 1` in it.
When you create a new page you will need to ensure the order value you set will produce the correct order in the side
bar so that this is ordered to your liking.
This again is a task that would be easier if you could use docker as you have no way of checking if you've done it
correctly, but that's where we are so we'll deal with it during reviews.

4. In addition to the `order` value in the *front matter* you must also provide a title for the page.
   This isn't done in the *front matter*, it is done as part of the actual page content, using the markdown `#` title
   syntax.
   You must only have **one** title on each page (so you can only use `#` once, but you can use `##`, `###` etc as many
   times as you like).
   Putting this together, your new page should have something like this at the top:

```yaml
---
order: 2
---

# My Exciting New Page
```

[1]: https://github.com/orgs/ukhsa-collaboration/teams/qat-standards-contributors
[2]: https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop#part-1-installing-and-authenticating
[3]: https://github.com/ukhsa-collaboration/standards-qat
[4]: https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop
[5]: ./.github/guide_assets/vscode_exts.png
[6]: ./.github/guide_assets/vscode_find_markdown_all_in_one.png
[7]: ./.github/guide_assets/vscode_explorer.png
[8]: https://docs.github.com/en/get-started/using-github/github-flow
[9]: ./.github/guide_assets/ghd_home_main.png
[10]: ./.github/guide_assets/ghd_main_switch_branch.png
[11]: ./.github/guide_assets/create_branch.png
[12]: ./.github/guide_assets/branch_change.png
[13]: ./.github/guide_assets/vscode_home.png
[14]: ./.github/guide_assets/vscode_all_the_files.png
[15]: ./.github/guide_assets/vscode_open_file.png
[16]: ./.github/guide_assets/vscode_preview_md.png
[17]: ./.github/guide_assets/vscode_new_file.png
[18]: ./.github/guide_assets/vscode_front_matter.png
[19]: ./.github/guide_assets/dev_standards_side_bar.png
