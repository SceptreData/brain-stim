---
title: What is Gatsby?
date: '2020-04-20T22:40:32.169Z'
template: 'post'
draft: false
slug: 'what-is-gatsby'
category: 'Gatsby'
tags:
  - 'Design'
  - 'Static Site Generators'
  - 'Web Development'
description: "What the heck is this Gatsby we've been hearing so much about? Do I care? Should you? In this article we briefly go over some of the underlying concepts."
socialImage: '/media/42-line-bible.jpg'
---

Gatsby is a free, open source static site generator. It works with React and
does as much work as possible to make your static sites blazing fast.

The nice thing about using Gatsby is that it fits into your existing react
workflow. If you're already using React, Gatsby is a snap. All of your react code
gets minified, and optimized to pure HTML/JS/CSS. If you're like me,
you're used to setting up a complicated gulp/grunt pipeline to properly handle your various
optimizations. With Gatsby, you get a lot of this _for free_.
No server code has to execute before your page is pushed down the wire which means
you get lightning quick connection speeds.

One place where Gatsby really shines is image optimization.
It uses the image library 'Sharp' underneath the hood to automatically
create your images in every format/size that might be needed for a user.
Then when the user navigates to the page, they are automatically served
the most appropriate image format. In effect this means that you will
server ultra-light .webp images to users who can see them, and optimized
.jpg's and .png's where appropriate.

Gatsby does all this optimization during its build process. What sets
Gatsby apart is that you have a lot of control over this process.
It's here where you outline the rules that connect your application together.
Additionally, there is a diverse set of open-source plugins for you to make use of.
lets say you wanted to build blog post pages out of markdown files. There's a
gatsby-plugin for that!

That's all well and good, but What if I want to make changes to the site?
Using some of the ultra-modern, and free ( and fast! ) solutions available like
Netlify or Vercel (formerly Zeit.com), this could not be easier.  
Gatsby (and the rest of the world honestly) encourages you to use a git repo for your
project. If you're hosting your site on Netlify, all you have to do is point it towards
your git repo. Whenever you push changes to your repo it triggers a web hook, and
Netlify rebuilds your project, just like that.

There are some drawbacks to this approach, the biggest being that changes to your
site don't happen instantly. You have to watit for Gatsby to rebuild your website
in the background. This implies a few minutes of delay between changes appearing
on your site. The trade off of course, is the optimized, SEO friendly static
pages that are built as a result.
