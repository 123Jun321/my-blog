---
title: How to RSS your blog on Linkedin
date: 2026-05-17 07:14:16
tags: Blog
categories: 
  - Hexo
  - [Zapier]
---
Recently I achieved that if I post a new blog, it will generate a new post to my Linkedin like RSS, and I will introduce how to do this in this article.

## What is Zapier
I used Zapier to complete this flow, [Zapier](https://zapier.com/) is a no-code automation platform that connects your favorite apps—like Gmail, Slack, and Salesforce—so they can work together. It automatically moves information between tools, eliminating tedious manual data entry and repetitive tasks.

## Steps to achieve this

1. Install hexo RSS extension
```
npm install hexo-generator-feed --save
```
2. Enable the extension in your blog, go to the _config.tml and append:
```
feed:
  type: rss2
  path: rss.xml
```
After finishing above steps, your blog will have a RSS url, like https://[blog address]/rss.xml. You need to use this on Zapier to trigger your workflow.

3. Register an account on Zapier and create a new Zap.
4. Choose the RSS as the trigger and type the url you got from the Step 2.
5. Create the action to create LinkedIn post and adjust the title and content you want to show.

>Remind: Zapier has their own AI copilot, you can just type your thoughts and let it help you build the flow automatically!