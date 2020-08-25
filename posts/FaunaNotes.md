---
title: FaunaDb Notes  
date: 2020-08-05T00:00:00.000Z
author: Nobody Cares
summary:  tips and gotcha's about FaunaDb
tags:
  - programming
---

###### FaunaDb Aug 2020

https://docs.fauna.com/fauna/current/cookbook/index.html?lang=javascript

https://docs.fauna.com/fauna/current/security/?lang=javascript


user gmail account
so far, only the todo database in that account

###### chris coyier and david.  

Build your backend with serverless functions.
todo app. faunaDb sample.
Netlify duznt have a database, but lets build some functions that crud faunaDb.

https://www.youtube.com/watch?v=iZrzuUwm-9Y&list=RDCMUCADyUOnhyEoQqrw_RrsGleA&index=19


we could hit the api's from the browser, but that is not secure enough.
instead, lets hit serverless functions that protect that api.

lets do CRUD stuff, interfacing (not with the api's in the browser) but instead, run node javascript on the server.


steps (see if I remember right)
fork the netlify-faunadb-example repo.  created netlify-faunadb-example2 on flatbill github.
delete old todo on fauna db via the fauna console.
in my example2 repo, there is a readme.md file, created by dave.
dave build a deploy-to-netlify button.  lotsa complex stuff happens when you click it.
next thing ya know, i'm auto-jumped to a netlify site, tying my netlify account (or maybe site) to the github account (maybe the repo).
so, every time i change the github source, it auto deploys a site: https://sharp-leavitt-971c15.netlify.app/
which is a react site.  very skinny and elegant react app.
there are also some step-by-step instructions in dave's readme.md file,
where you go into fauna db, create a netlify database, and generate a KEY and a SECRET.
Never mind the instructions that say: Set your database access secret in your terminal environment <-- i didnt do this
instead, I followed the video instructions to go into netlify and configure a KEY and SECRET in the environment settings.
Settings for sharp-leavitt-971c15 > Environment Variables > FAUNADB_SERVER_SECRET fnAD0HCiMIACEg9sJMnvzNnHtCD22..
This environment KEY and SECRET gets read by the javascript functions, where each function references: 
secret: process.env.FAUNADB_SERVER_SECRET
!!! This magically ties the javascript functions to the Fauna database !!!!

? how to explain the CRUD functions ??
so, there are functions like todos-read.js
and these functions get built somehow as 'netlify functions' which seem similar to AWS lambda function.
At the top menu in my netlify account, the functions are listed: 6 Lambda functions actively running in production.
I'm just not sure how the functions got there.  Nor am I sure how the react app magically got there.
Probably something to do with the build settings.  

 
 
 
SECRET is pasted in from fauna db (where I generated a secret)



