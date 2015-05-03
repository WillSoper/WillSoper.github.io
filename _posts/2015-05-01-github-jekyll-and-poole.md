---
layout: post
title: "Blogging with GitHub Pages, Jekyll and Poole"
published: true
---

I've deleted my old blog, and started a new one on GitHub. Here's what, how and why.

###Building and hosting this blog
I'm using GitHub Pages to host this blog. [GitHub Pages](https://pages.github.com) is a simple and free way to host a website directly from your GitHub repository. It supports [markdown](https://help.github.com/articles/markdown-basics/) for simple, text based editing and creation of pages on your site. It can also build a site by processing it with Jekyll, which is what I'm doing.

[Jekyll](http://jekyllrb.com) is a static site generator. It's designed to allow full featured blogging (with permalinks, tags and custom layouts, for example) without any databases or scripting languages being required in your hosting environment. You write markdown, Jekyll processes it and produces static content (plain ol' html, css etc) which can you can then put on a web server that's capable of just serving static content. 

When you use GitHub Pages, it can process your markdown files with Jekyll and immediately serve the resulting static content to the internet, which means you only need to care about committing your blog posts as a series of markdown files to GitHub, and not worry about automating a build and transferring the output.

###Making it readable
Whilst I know my way around the building blocks of the web, I am *not* a designer, and I had no intention of spending hours crafting CSS and [SASS](http://sass-lang.com/). One of the main reasons for moving to a text based blogging format was so that I could forget about styling things and making them look pretty, and focus on creating content.  [Poole](http://getpoole.com/) provides a complete Jekyll site, including themes and sample posts. I've used the default style, which is pretty minimal, and helped me not get distracted with messing around with styles.

I had to make only a few amendments to the basic install, if you're interested in the nuts and bolts then you can make use of one of the other nice things about hosting my site on GitHub, and take a look at all of my [Commits](https://github.com/WillSoper/WillSoper.github.io/commits/master) to this site. Here's a brief summary of the changes that I made, though:

- **I updated the _config.yml** file, to ensure it had my details and URL in, rather than those of the [Poole GitHub repository](https://github.com/poole/poole) which I forked.
- **I removed the homepage** which displays the most recent post and **replaced it** with an 'archive' style list of my posts. I'm guessing that most people, if they ever find my blog, will get deep-linked to a post using a search engine. This won't be the kind of blog where you come back to check for new content, so the homepage will be mostly for me - and having a list of all the stuff I might be looking for is helpful. I got the code for the archive style list from [Joshua Lande's blog](http://joshualande.com/jekyll-github-pages-poole/).

...and that was about it! This was enough to get the blog to a state where I was happy that I could read what I'd written.

###Editing and Creating pages
One of the great things about writing content in [markdown](https://help.github.com/articles/markdown-basics/) is that there are a hundred ways in which you can do it. Here are a few that are well suited to using Jekyll and Github, 

[mobile blogging](http://joewiz.org/2013/08/18/mobile-blogging-with-jekyll/)

[online blogging](http://joewiz.org/2013/08/20/jekyll-blogging-in-the-browser-with-prose-io/)