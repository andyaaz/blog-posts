---
title: "Developer blog engine loop"
description: "Ever wonder why it is hard for developers to publish blog posts?"
slug: "developer-blog-engine-loop"
createdAt: "2021-02-03"
tags: ["dev life", "react", "gatsbyjs", "nextjs"]
---

## What is developer blog engine loop?

This is a name that I made up to describe something that maybe many developers have experienced. I call it "developer blog engine loop" because as a developer myself, I have always wanted to build my blog/portfolio website with "coolest" technology that I know. Just to give you some examples: `HTML/CSS(with some Bootstrap themes)` + `JQuery`(maybe), `WordPress`, `Jekyll`, `GatsbyJS` or `NextJS`. [Here is list of them](https://jamstack.org/generators/).

## My Experience

### HTML/CSS

My first ever blog/portfolio was built with HTML/CSS (Bootstrap). At the time I was just learning web development and wanted to make a personal website for myself. Also I just discovered Bootstrap 3 and was really impressed by how many resources there were online and how little I had to do to make a pretty website. So I went with one of the free templates I can find online and made some changes to the content and it was good to go.

I didn't really have the motivation to add or update the information on the site as I was busy with University assignments and other things so after I hosted it on github pages, I never touched it again.

Maybe I switched one theme to another from time to time but nothing serious.

### Jekyll

After my first HTML/CSS site was built, since I hosted on github page I noticed that Github pages by default supports some Jekyll themes that is supposed to be super easy to use. So as always being a curious person, I tried out Jekyll. It didn't take long to set up the site as Github has built in support for it. So you just have to choose a theme and your site is pretty much ready to be published. However, I didn't publish any blog posts on there because I was spending way too much time on how to make it look good. The default theme looked fine but as an aspiring web developer, how could I be possibly satisfied with a default styling solution. I had to make some changes to make it look "cooler" or more unique. And you probably guessed it, I was never satisfied and never publish a single piece of content.

### GatsbyJS

Fast-forward a few years, I started working and entered the world of modern JavaScript. GatsbyJS was the de facto way of building a blog and known for its great plugin system and blazing fast page speed. In the hope of learning and posting some content online, I created a Gatsby blog site using the same theme that [Dan](https://github.com/gaearon) is using. I quickly got it to work but I really didn't like the styling solution came with the theme/starter. So I started to change the styling/theming solution for the site to make it use CSS-in-JS, support dark theme with Material-UI and optimize images, etc.

I posted a few posts on it and it was working just fine. Until I found out that NextJS also supports static site generation (it didn't support it when I started using Gatsby).

### NextJS

This is the latest framework I am trying and so far happy with it. It feels one abstraction layer below Gatsby in that Gatsby wraps everything with GraphQL and plugins while Next provides less support for managing data. I have learnt to appreciate both approaches. In the Gatsby world, you have to be familar with the Gatsby Node API and how its plugin system works in order to have a pleasant experience. For Next, most of the time, I have to figure out a way myself to fetch data and process them in a way that can be used by the UI code. Because of that I really like writing React code in Next with the overhead of learning Gatsby ecosystem knowledge.

## Conclusion

I guess for developers the technology or content is not the most important but the experience. I have learnt so much just by swiching frameworks and styling solutions and it is good practice for any production application you are going to build. I think I will stick with NextJS for now and decouple the content and the code so that content can be reused else where.
