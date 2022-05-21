---
layout: note
title: "Making a github-hosted website"
date: "2021-10-05"
tags: [coding, tool, how-to]
---

I use Jekyll for static-site generation, combining with Atom for git and Obsidian for writing. Here are the resources I use to pimp this site.

## How I do it
- First, I pull the theme from [gradfolio](https://github.com/jitinnair1/gradfolio/) to my repo and download the content to my machine.
- Install Jekyll locally so I can preview the website before `git push`
- I want to have a note section instead of blog post. So I use bi-directional link feature from [notenote.link](https://github.com/Maxence-L/notenote.link) inspired from [[Obsidian]].
- The notes are showed randomly using the code in [generating a list of random notes](https://thornelabs.net/posts/a-better-way-to-display-random-jekyll-posts-on-page-load-or-refresh-using-jquery-and-json.html)
