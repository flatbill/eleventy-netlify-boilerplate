---
title: Smart People Talk
date: 2029-08-20T00:00:00.000Z
author: Nobody Cares
summary: Smart People Talk about technology
tags:
  - technology
---


##### Aug 20 focus on people who promote the STACK vs the old MONOLITH

jamstack loblaw dev ops netlify
https://www.netlify.com/customers/loblaw/

jamstack contentful guy talks about components and a speed based architecture
https://www.youtube.com/watch?v=HSSLI0jcMm0&feature=emb_rel_pause

Monica Dinculescu is smart and fun and builds web stuff, static sites.
Monica says a static site is a superbadass site where you don't have to care about infrastructure.
https://www.youtube.com/watch?v=f5QYSdpMs6Y

Monica recommends learning about serverless functions:
https://github.com/anaibol/awesome-serverless

example netlify cms
https://www.elpassion.com/blog/jam-stack-your-old-cms-into-the-closet


###### netlify calling aws
Director of Support .... might be useful someday, but right now i seem to have partial success with netlify + faunaDb
Oct '19
You could use our (reverse) proxying feature to connect us to it; that’s a pretty common pattern and avoids CORS problems too:
https://docs.netlify.com/routing/redirects/rewrites-proxies/#proxy-to-another-service 21
(and, it’s how our own functions implementation routes to AWS under the hood without setting pesky custom hostnames or worrying about SSL certificates ourselves - AWS has one that covers THEIR hostnames already!)
