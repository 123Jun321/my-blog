---
title: How to build a free blog using Cloudflare Page+hexo+Github
date: 2026-05-04 07:56:19
tags: Blog
categories: Hexo, Github
---

I build this blg based on Cloudflare Pages+Hexo+Github, and this is totally free if you can accept the free domain of Cloudflare Pages, anyway, I'm okay with that. I will introduce how to achieve it in this article.

## Before Start
At the first, I will introduce to you what are they:
1. Cloudflare Pages: It is a JAMstack platform for frontend developers to collaborate and deploy websites.It can help you to build and deploy the site and it will also give a free domain to use!
2. Hexo: A fast, simple & powerful blog framework
3. Github: It is a cloud-based platform that allows developers to store, manage, and collaborate on code projects

This blog frame is hexo, we will use Github to store our blogs, and Cloudflare will help us to build,  publish and host the blog.

## Install Hexo and build your blog
1. Install the hexo on your laptop or server, you can follow this article https://hexo.io/docs/ to install it.
2. Build your own blog, https://hexo.io/docs/setup:  
```
hexo init <folder> 
cd my-blog
npm install
```


3. Write your own post with [Markdown](https://www.markdownguide.org/cheat-sheet/) format, https://hexo.io/docs/writing:  
```
hexo new [layout] <title>
```

4. Now your own blog has built and you can use this command to preview it in the blog folder:  
```
hexo server
```

## Init Github repo
1. Install git: https://git-scm.com/install/linux
2. Register Github account if you don't have: https://github.com/
3. Generate your own ssh key and upload the public key to the github: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account, about ssh, you can refer to my previous [blog](https://my-blog-12c.pages.dev/2026/05/03/What-is-SSH/)
4. Create a new repo on Github: https://docs.github.com/en/get-started/start-your-journey/hello-world#step-1-create-a-repository
5. Go to your blog folder and upload the blog files to Github:
```
git init
git add .
git commit -m "init blog"
git branch -M main
git remote add origin <your repo git url>
git push -u origin main
```

## Build by Cloudflare Pages
1. Sign in Cloudflare pages: https://pages.cloudflare.com/
2. Go to Pages and create Project
3. Connect to your Github blog repo
4. Configure the parameters:
   >Framework preset: None  
   >Build command: `npm install && npx hexo generate`  
   >Output directory: public
5. Click Deploy

There will be a domain generated and then your blog is public and ready to be visited!

Every time when you push your commit to the repo, it will trigger the Cloudflare Page to rebuild and republish it! 
<u>Now, just tell others your blog domain and share your life!</u>