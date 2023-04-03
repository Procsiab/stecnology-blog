---
title: "Static Website With Hugo"
date: 2023-04-03
draft: false
---
## Finally I decided to run own blog

I am always looking for feedback on my *arguably useful* experiments with free software and hardware tinkering, and since I think that someone might find my work inspiring or entertaining - other than my poor friends who I constantly bother by asking for feedback on the projects I will document here - I decided to begin running this blog.

Let's be honest: I also was delaying the deployment of this blog not because I was lacking the skills or the infrastructure, but because I did not want to fumble for a static site generator that I liked and I could start working with almost immediately.

In the end, I choose to try [Hugo](https://gohugo.io/getting-started/quick-start/) and I could deploy this very website inside my infrastructure in almost 10 minutes.

## What makes this website static?

The files that make up this blog were generated from the Hugo binary using a template and a configuration file, which determined how to produce the HTML, CSS and JS files that your browser is presenting to you right now.

These files are passed to your browser through a *reverse proxy*, a piece of software which handles application level communications between web services; I am running [Caddy](https://caddyserver.com/) for this purpose, following my principle that if I can get up and running fast enough then I go on with my life and do other stuff.

The *components* of the blog's files are in fact YAML and MarkDown files, which are easy to maintain under a version control system (VCS) like [Git](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control), which I am using at the moment to track and manage changes to this website.

### Over-engineering this deployment

To reflect a change in a configuration or template file to this blog, the static *products* must be generated again by Hugo and then deployed inside the infrastructure to which your browser connected to download and show this page; this can be done manually by copying the exact static file's directory to the web server, or it can be automated through a so-called *pipeline*, a procedure which is triggered by a Git-related activity, for example the commit of a new blog post, and then it performs integration and delivery tasks like calling Hugo to build the website and copying its static files to the web server without interaction.

There are many services which offer pipeline integrations with Git, but the one that I am most interested in at the moment is [Forgejo](https://forgejo.org/2023-03-release-v1/), which has introduced pipelines as its parent project [Gitea](https://blog.gitea.io/2022/12/feature-preview-gitea-actions/) has.

## Looking forward

I would like to use this blog as a public repository for updates and documentation regarding my projects, both the past ones and the one's I am still too lazy to begin tinkering with. Also, this is the chance to get more proficient with Hugo and in general with regularly updating a blogging site.

## Is that it about "the infrastructure"

Well, there's more to it, but to keep this post short I would comment the underlying moving parts saying that I chose and I am sticking to each one because of the few time I have spend on unexpected events and for the initial configuration; that being said, do not imagine an enterprise grade deployment: It's **good enough™**.
