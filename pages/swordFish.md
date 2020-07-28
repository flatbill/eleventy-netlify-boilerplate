---
layout: layouts/swordFish.njk
title: swordFish
date: 2017-01-01T00:00:00.000Z
permalink: /swordFish/index.html
eleventyNavigation:
  key: swordFish
  order: 5
---
hello from swordFish file: eleventy-netlify-boilerplate/pages/swordfish.md

> ya gotta stuff pics in folder: static/img/  
>eleventy.js has some passthrough logic to upload those images to netlify. 

>here is imbedded html in the markdown file:
 
<img src="../static/img/img_girl.jpg" alt="Girl in a jacket" width="250" height="300">

>now lets try inserting the image with markdown instead of imbedded html:

![GirlieJacket](/static/img/img_girl.jpg){: width=50% height=50% }

