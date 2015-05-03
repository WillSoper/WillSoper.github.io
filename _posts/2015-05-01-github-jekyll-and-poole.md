---
layout: post
title: Blogging with GitHub Pages, Jekyll and Poole
---
I've deleted my old blog, and started a new one on GitHub. Here's what, how and why.

###Building and hosting this blog
I'm using GitHub Pages to host this blog. [GitHub Pages](https://pages.github.com) is a simple and free way to host a website directly from your GitHub repository. It supports [markdown](https://help.github.com/articles/markdown-basics/) for simple, text based editing and creation of pages on your site. It can also build a site by processing it with Jekyll, which is what I'm doing.

[Jekyll](http://jekyllrb.com) is a static site generator. It's designed to allow full featured blogging (with permalinks, tags and custom layouts, for example) without any databases or scripting languages being required in your hosting environment. You write markdown, Jekyll processes it and produces static content (plain ol' html, css etc) which can you can then put on a web server that's capable of just serving static content. 

When you use GitHub Pages, it can process your markdown files with Jekyll and immediately serve the resulting static content to the internet, which means you only need to care about committing your blog posts as a series of markdown files to GitHub, and not worry about automating a build and transferring the output.

[Poole] is