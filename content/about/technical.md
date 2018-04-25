---
title: "Technical"
date: 2018-04-25T11:19:15-04:00
draft: false
---

## Summary

This site is a [static site](https://en.wikipedia.org/wiki/Static_web_page), generated with [hugo](https://gohugo.io), written in [markdown](https://en.wikipedia.org/wiki/Markdown), using a modified version of the [Hugo Learn Theme](https://github.com/matcornic/hugo-theme-learn) by [Mathieu Cornic](https://github.com/matcornic). It is autodeployed on [AWS S3](https://aws.amazon.com/s3/) using [AWS CodeBuild](https://aws.amazon.com/codebuild/) whenever the [git repository](https://github.com/mohoromitch/rucs-wiki) on [GitHub](https://github.com) is updated.

## Static Site

A static site is a website with fixed content. Every page is pre-generated and served directly, without any dynamic elements or backend programming logic. This allows for deployment on S3, which makes hosting the website low maintenance and low cost.

## Hugo

Hugo is a static site generator written in the Go programming language. Go being a compiled language allows Hugo to be an incredibly fast site generator. The content for this site is written in the Markdown markup language, then converted into the HTML being served to you.

## Markdown

Markdown is a light text markup language for formatting plain text. You've probably seen it before, using \*'s for making text italicized and bolded. For a concise reference for the syntax, see Adam Pritchard's [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

## Theme

The theme used on the site is a modified version of Mathieu Cornic's port of the [Grav](https://learn.getgrav.org/basics/what-is-grav) documentation site, [Hugo Learn Theme](https://github.com/matcornic/hugo-theme-learn). This theme was chosen specifically since it was designed for code/tool documentation, which works well for reference sites like this.

## Github

[GitHub](https://github.com) is the (self-proclaimed) "...world's leading software development platform". It hosts a plethora of open-source projects, where developers collaborate together using [git](https://try.github.io/levels/1/challenges/1). Git is a version control system which is, and forever will be, better than Fossil. By having this site hosted in a git repo, collaborators will have a chance to practice their git.

