---
layout: layouts/swordFish.njk
title: swordFish
date: 2017-01-01T00:00:00.000Z
eleventyNavigation:
  key: swordFish
  order: 5
---
hello from swordFish file: eleventy-netlify-boilerplate/pages/swordfish.md

> ya gotta stuff pics in folder: static/img/  
>eleventy.js has some passthrough logic to upload those images to netlify. 

>here is imbedded html in the markdown file:
 
<img src="../static/img/img_girl.jpg" alt="Girl in a jacket" width="250" height="300">

>I tried inserting the image with markdown instead of imbedded html,
but the image cant be resized.  this duznt work right:
 ``    ![GirlieJacket](/static/img/img_girl.jpg){width=50% height=50% } ``
this works, but who cares?  ``    ![GirlieJacket](/static/img/img_girl.jpg) ``
> what a hassle.  

> some 11ty lover recommend adding a markdown plugin: https://www.npmjs.com/package/markdown-it-attrs
https://www.11ty.io/docs/languages/markdown/#add-your-own-plugins
only somebody that loves markdown would go thru all this pain.


> elventy has a cute possum balloon thing.  Here's my take on it:
<img src="../static/img/possumBalloonRoadside.jpg" alt="PossumBalloon" width="250" height="300">
