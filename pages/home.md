---
layout: layouts/home.njk
title: Home
date: 2016-01-01T00:00:00.000Z
permalink: /
summary: GenXYZ Home
eleventyNavigation:
  key: Home
  order: 0
---
 
##### Welcome Home Sentient Beings
Home file is eleventy-netlify-boilerplate/pages/home.md
These web pages are a mix of .ntk (nunjucks)  and  .md (markdown text files).

>Look mom, I'm writing text as markdown in eleventy-netlify-boilerplate/pages/home.md
See the Blog section for Jos & Sorrow of Markdown.

##### How does this site work ?
This '11ty app' is in a github repo. 
Tie the github repo to a Netlify site.
Netlify site settings, build settings, Link site to a github repo.

For changes (in my repo) to take effect:
Set Netlify auto-publish ON, or manually trigger a Netlify deploy of this site. 


##### Why use 11ty on Netlify ?
11ty (or Eleventy) an up-and-coming JavaScript static site generator.

Some call 11ty a way to do Component Driven Design.  It feels more like snippet-driven-design. 
Seperate content from layout.
11ty seems to be a tool for people who used to be front end web masters.
There is learning curve to 11ty. There are help and tutorial sites.
https://snipcart.com/blog/choose-best-static-site-generator
11ty might be a quick way to do demos and project ideas without full blown angular.

##### How do I pretty up this ugly site?
I'm trying bulma.css in the ntk files. The site relies on content I write in markdown .md files.

##### how to create blog info. (create 'posts').
Create more .md files in github, and re-publish.
I mean, go to github, folder bla bla /posts, create like ```myNewPostAug2020.md``` file to do a new post. 

 
##### why 11ty  Blog here?
Mainstream blog apps like wordpress might be a better fit for most.
those apps make pretty pages by choosing a template 'off the rack'.
This kind of app is more for tech people learning 11ty and netlify.
 
 ##### Forms, Blog, boiler plate?
 If ya don't wanna capture forms data (like forget the contact page)
and ya don't wanna bother with a blog  (like kill the blog and posts stuff)
and instead, ya wanna create a portfolio-ish 'static' site...
then maybe start with this boiler plate page,  change the nav stuff,
and create a .njk file (and maybe a .md file)  for each nav option.
The .md file has a Front Matter heading area.
In the Front Matter heading, there is a line for which layout (njk file) it should use.
So, for a portfolio, maybe stick nice html into each .njk file.
For example, this markdown file ```home.md``` has a line: ```layout: layouts/home.njk```.

July 2020 I've been working on the .njk templates, 
along with the .md files.
This 11ty example project has a complex folder structure. 
well, i commented out inline.css and replaced it with bulma.css

##### Hey, get with the program
.ntk files are html templates (no content)
.md files are content
ok, .md examples have html shorthand too. 

 



