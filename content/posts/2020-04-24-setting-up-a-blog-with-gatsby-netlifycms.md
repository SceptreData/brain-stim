---
template: post
title: Setting up a Blog with Gatsby + NetlifyCMS
slug: set-up-gatsby-netlifycms
draft: false
date: 2020-04-24T19:14:01.686Z
description: >-
  In this article, we go over the basics of setting up Gatsby and NetlifyCMS.
  It's easy to get started, so lets go!
category: Gatsby
tags:
  - Design
  - Web Development
---

1. Install Gatsby

2. Start Project

```
gatsby new netlify-cms-tutorial https://github.com/gatsbyjs/gatsby-starter-hello-world
```

3. Set up project

```shell
yarn add netlify-cms-app gatsby-plugin-netlify-cms
```

4. gatsby-config.js
   module.exports

5. Set up config.yml
   This is our Advanced Custom Fields. It's also where we list the git repo.

6. Git Gateway

NOTE: Make sure that your package.json and other config files point
towards the correct repo and file structure.
