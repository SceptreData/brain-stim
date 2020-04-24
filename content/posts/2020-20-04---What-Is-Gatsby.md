---
slug: what-is-gatsby
draft: false
socialImage: /media/42-line-bible.jpg
template: post
title: What is Gatsby?
date: '2020-04-20T22:40:32.169Z'
description: >-
  What the heck is this Gatsby we've been hearing so much about? Do I care?
  Should you? In this article we briefly go over some of the underlying
  concepts.
category: Gatsby
tags:
  - Design
  - Static Site Generators
  - Web Development
---
* [The Features](#the-features)
* [The Build Process](#the-build-process)
* [Working With Git](#working-with-git)

  ![The Great Gatsby](/media/gatsby_blog-740x370.png "Gatsby")

[GatsbyJS](https://www.gatsbyjs.org) is a free, open source static site generator. It works with [React](https://reactjs.org/) and does everything it can to make your static sites blazing fast.

The nice thing about using Gatsby is that it fits into your existing react workflow. If you're already using React, Gatsby is a snap.

## The Features

All of your react code gets minified, and optimized to pure HTML/JS/CSS. If you're like me, you're used to setting up a complicated gulp/grunt pipeline to properly handle your various optimizations. With Gatsby, you get a lot of this *for free*. No server code has to execute before your page is pushed down the wire which means you get lightning quick connection speeds.

![Kevin Smith](/media/kevin.gif "Silent Bob speaks at last")

One place where Gatsby really shines is image optimization. It uses the image library 'Sharp' underneath the hood to automatically create your images in every format/size that might be needed for a user.
Then when the user navigates to the page, they are automatically served
the most appropriate image format. In effect this means that you will
server ultra-light .webp images to users who can see them, and optimized
.jpg's and .png's where appropriate.

## The Build Process

Gatsby does all this optimization during its build process. What sets Gatsby apart is that you have a lot of control over this process. It's here where you outline the rules that connect your application together.
Additionally, there is a diverse set of open-source plugins for you to make use of.
lets say you wanted to build blog post pages out of markdown files. There's a
gatsby-plugin for that! Working with Gatsby-plugins is a lot like working with legos!

![](/media/lego.png)

## Working with Git

That's all well and good, but What if I want to make changes to the site? Using some of the ultra-modern, and free ( and fast! ) solutions available like [Netlify](https://www.netlify.com/) or [Vercel (formerly Zeit.com)](https://vercel.com/), this could not be easier.\
Gatsby (and the rest of the world honestly) encourages you to use a git repo for your project. If you're hosting your site on Netlify, all you have to do is point it towards your git repo. Whenever you push changes to your repo it triggers a web hook, and
Netlify rebuilds your project, just like that.

There are some drawbacks to this approach, the biggest being that changes to your site don't happen instantly. You have to watit for Gatsby to rebuild your website in the background. This implies a few minutes of delay between changes appearing
on your site. The trade off of course, is the optimized, SEO friendly static
pages that are built as a result.

How fast, you might ask? 

![Road Runner](/media/roadrunner.gif "Road Runner")



Want to learn more? Check out my article on [setting up a blog with Gatsby and NetlifyCMS.](https://brain-stim.netlify.app/posts/set-up-gatsby-netlifycms)