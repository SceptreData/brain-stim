---
template: post
title: Using the gatsby MDX plugin
slug: gatsby-mdx
draft: false
date: 2020-04-24T21:24:06.086Z
description: >-
  In this very brief article we discuss using the MDX plugin, a tool which
  allows you to write react components in your markdown. Wow!
category: Gatsby
tags:
  - Design
  - Web Development
  - Gatsby
---
# What's MDX?

MDX is markdown with super powers. It lets you write React's JSX inside your markdown documents. Why would you want this? It lets you do a lot less typing! You don't need to spec out a whole react component every time you need a new blog post, you just include the component in your markdown file.

## Installation

In order to use gatsby-plugin-mdx we need a few plugins. Let's install them now.

```shell
npm install gatsby-source-filesystem gatsby-plugin-mdx @mdx-js/mdx @mdx-js/react
```

We use Gatsby source filesystem to load our markdown files and we use the rest of the plugins for our MDX files.

## Configure

Now lets add gatsby-plugin-mdx to our plugins list in  gatsby-config.js.

```javascript
module.exports = {
  plugins: [
    {
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `pages`,
        path: `${__dirname}/src/pages/`,
      },
    },
    `gatsby-plugin-mdx`,
  ],
}
```

We're doing two things here: We are telling the gatsby to load our markdown files form the src/pages directory, and we are loading our plugin 'gatsby-plugin-mdx'. That's it! Now our markdown files can use React components. How exactly does that work?

Imagine we have a really basic component like this colored Box component. It takes its children and wraps them in a red  box:

```jsx
// TomatoBox.js
export default ({children}) => (
<div style={{ background: `tomato`, color: '#fff'}}>
  {children}
</div>
)
```

We can use it in our markdown file like this:

```mdx
import TomatoBox from 'TomatoBox.js'

# Hello Tomato lovers!

Check out this cooooool Div.

<TomatoBox>
  I Love tomatoes!
</TomatoBox>
```
<div style={{background: 'tomato', color: 'white'}}>
  I love tomatoes!
</div>


That's it.  Just like that, we have React components in our markdown.

![Asplode](/media/asplode.gif "Boom baby!")