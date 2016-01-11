---
layout: post
title: "Blogging with GitHub Pages, Jekyll and Poole"
published: true
---

I've deleted my old blog, and started a new one on GitHub. Here's what, how and why (not necessarily in that order).

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
One of the great things about writing content in [markdown](https://help.github.com/articles/markdown-basics/) is that there are a hundred ways in which you can do it.

Here are a few that are well suited to using Jekyll and Github, the most useful information I found these was on [Joe Wicentowski](https://twitter.com/joewiz)'s blog posts on [mobile blogging with jekyll](http://joewiz.org/2013/08/18/mobile-blogging-with-jekyll/) and [blogging in the browser with jekyll](http://joewiz.org/2013/08/20/jekyll-blogging-in-the-browser-with-prose-io/).

<div class="message">
    NB: see updates below, my  tools have changed since this was first published!
</div>
- When I'm on an internet connected PC, I use [Prose.io](http://prose.io/) to create and edit blog posts, and commit them directly to GitHub. It supports in browser previewing of your markdown, so you can see what it will look like without setting up your own Jekyll server or publishing it to GitHub, and requires nothing but a browser and providing OAuth access to your GitHub repositiory.
- When I'm on an iPad or iPhone, I use [Octopage](https://itunes.apple.com/us/app/octopage-blogging-jekyll-markdown/id649843345?mt=8) to connect directly to GitHub, and amend posts or drafts there. It, too, supports previewing of your posts, and OAuth (when Joe wrote his blog post, above, it required that you supply username and password directly to the app - this is no longer the case). It costs £0.79 in the uk, which is less than I spend on a cup of coffee.

###Fast and simple
It took me longer to write this blog post than it did to get GitHub, Jekyll and Poole all working together seamlessly. Apart from the £0.79 I spent on an iPhone app (which I really didn't have to do), it has cost me nothing. I started with no knowledge of any of the tools that I ended up using (I know git, but didn't even have a GitHub account setup when I started), and I'm happy with the result! What's even better is that everything I've used is open source - so if I want to change it to do something different, I can - and if I decide to do something totally different, all of my content is stored in simple markdown, which I can take anywhere! 

###Updates

- I'm thinking about moving my blog from GitHub and hosting it myself in the future; now that I'm happy with using Jekyll, and I like this format of blogging, it feels worth it to move for a few reasons:

1) *GitHub already recommends that you test your compilation of your site using Jekyll locally, and I've had a build error that took me ages to work out because they don't really give you much information in the event that a build fails.*
    
2) *I always feel kinda weird that the first time I find out whether the post works exactly in the way that I expected is when I actually publish it live!*
    
3) *If I'm going to the effort of putting together my own Jekyll build process, I might as well publish the __exact__ output that it produces to a cheap static hosting site, and do away with needing to publish all of my blog posts publicly on GitHub!*
    
- With all that said - there's a lot good about GitHub Pages, and I'm sticking with it until I get stuck on a rainy day and need a project to move! Expect a new blog post as and when I do that. 
          
- I don't really use Prose.io so much anymore, mainly because I like to be able to work locally and in a disconnected way. I find it much more natural to be able to start working on a blog post and write it in a couple of sittings on my local machine, than to commit a half written post with the 'published: false' flag to GitHub.

- Instead of Prose.io, when I'm on my own PC, I use VS Code. You can [read more about editing and previewing Markdown in VS Code](https://code.visualstudio.com/Docs/languages/markdown) on the VS Code website directly. It supports live previewing, and although the default theme doesn't look a lot like my website, it allows me to check that my Markdown is valid and does what I expected before publishing which is all I need. If you need to see how your post will look, you can link to a custom css file (there are steps on the page that I linked to).

- I don't really publish blog posts from my iPhone, so whilst the Octopage app is still installed (and I'm sure I'll use it occasionally in the future), instead I prefer to write down ideas and drafts in [OneNote](https://itunes.apple.com/gb/app/microsoft-onenote-lists-photos/id410395246?mt=8), and then write them up properly on my PC.