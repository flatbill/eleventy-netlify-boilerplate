---
layout: layouts/home.njk
title: Home
date: 2016-01-01T00:00:00.000Z
permalink: /
eleventyNavigation:
  key: Home
  order: 0
---
# Welcome Home Sentient Beings
home file is eleventy-netlify-boilerplate/pages/home.md
this web page is a mix of .ntk (nunjucks)  and  .md (markdown text files)

> paragraph starts here.  
Look mom, i'm writing text as markdown in eleventy-netlify-boilerplate/pages/home.md
See the BLOG section for notes on markdown.

>Why use this approach of Netlify + 11ty ?
I don't know why.  I suppose it's OK if you already love 11ty,
along with the static page and snippet-driven-design.
OK, some call this Component Driven Design.  Sheesh.
If you are using Netlify, then maybe this approach gets you started.
But there is a learning curve to 11ty.  
It seems to be a tool for tech people, 
who want to hand-craft their website.
I built an ugly site here.  Maybe somebody 11ty-oriented could pretty it up.


>Also, this 11ty template is big on the blog thing. 
But I cant find docs on how to create blog info. (create 'posts').
It seems like you create more .md files in github, and re-publish.
I mean, go to github, folder bla bla bla, create sixthPost.md file 
to do a new post?  
geez.

>Wordpress approach might be better, if ya wanna blog... 
there are zillions of starting points,
that make prettier pages.
Maybe you can host a wordpress site on netlify somehow?


>maybe a pure html css template as starting point instead of all this 11ty shit?
Or, just do Angular, and leave the alternatives to other thinkers.

>If ya don't wanna capture forms data (like forget the contact page)
and ya don't wanna bother with a blog  (like kill the blog and posts stuff)
and instead, a wanna create a portfolio-ish 'static' site...
then maybe start with this boiler plate page,  change the nav stuff,
and create a .njk file (and maybe a .md file)  for each nav option.
The .md file has a line for which layout (njk file) it should use.
So, for a portfolio, maybe stick nice html into each .njk file.

>I guess I'll try this with an addition Nav option, called SwordFish.
Build a web page all about Sword Fishing, and show it when he Navs there.


>don't forget, all the css is in file:
eleventy-netlify-boilerplate/_includes/assets/css/inline.css

well, i commented out inline.css and replaced it with bulma.css


> Hey, get with the program:
.ntk files are html templates (no content)
.md files are content
ok, .md examples have html shorthand too. 

 
> what about .css ?
is it bad manners to tie a css class to a portion of md words?
at least, if i did that, I would do no formatting in the md,
instead, i would rely on the class to do the layout & formatting.
like classes in bulma.

{:.selzClass1 } hello from class selzClass1
I added a plug in so that I could put CSS classes in a .md file.  Maybe not a good technique.

There is also a HACK to work with images in the includes/ images / static folder (or some crazy path like that).
i am using a relative path when defining anchor and href img-src, for the bulma menu logo.
but the relative path changes when the Url gets into sub-folders.
so, the nav .njk snippet has a HACK to find the right folder--   ./  or ../    (geez.)
Maybe solve this with a base tag instead, or a njk var set from the base url,
then use the njk var in the anchor href img-src.


