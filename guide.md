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

To access the code you can use github desktop (you can also use the `git` command line program if you have it installed, see optional software above).

To clone the [repository][2] with github desktop you can follow the github guide to [authenticate][3] and then [clone][4] the repository.

This should mean you now have the repository on your laptop.

## Work With the Documentation

All documentation and related assets must be placed in the `docs/` directory.

Within this directory there must be:

- `standards-qat.11tydata.json`
- `index.md`

These two files must be present in this docs folder for the site to work.
You shouldn't need to edit the `standards-qat.11tydata.json` file unless you want to change the layout of the site.

The `index.md` is the home page of the QAT standards site.

[1]: https://github.com/orgs/ukhsa-collaboration/teams/qat-standards-contributors
[2]: https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop#part-1-installing-and-authenticating
[3]: https://github.com/ukhsa-collaboration/standards-qat
[4]: https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop
