---
title: About Git Submodule
date: 2026-05-04 07:57:28
tags: Git
categories: Git
---
When I set this theme to my blog, I faced an issue is that I use `git clone` to clone the the [theme](https://github.com/Siricee/hexo-theme-Chic) to my theme folder and when I modified the config and committed to my blog git repo, there is an error about submodle, and then I start to learn this term.

# What is Git Submodule
>A Git submodule is a tool that lets you keep a Git repository as a subdirectory of another Git repository. Think of it as a "repository inside a repository" that stays linked to a specific version of the external project.

This is the explanation from Google Search of Submodules, submodule is the other repo that you contains in your own repo. 

You can also refer to this link to learn more details https://git-scm.com/book/en/v2/Git-Tools-Submodules.

# Common Commands
1. Add a submodule:
```
git submodule add <url> <path>
```
2. Pull latest changes from the submodule's source
```
git submodule update --remote
```

Finally, I solved this issue by forking the theme repo, I did the change on this theme repo and I added this repo to my blog repo as submodules. 