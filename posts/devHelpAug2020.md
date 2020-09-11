---
title: dev Help Aug2020 
date: 2020-08-25T00:00:00.000Z
author: Nobody Cares
summary:  links and notes about doing web development in Aug2020.  projects like questool5.
tags:
  - programming
---


##### Favicon.   lotsa work to put a crummy icon on the browser tab.
 
draw an icon on this page:
https://brunoportfolio.com/online_tools/iconpaint/index.php
then download it, and rename it to favicon.ico  (try the download folder).
move favicon.ico to the source code folder. (try github repo or local angular folder).

You still might see an old favicon.ico after ya generate the app again, then build > deploy > publish, and refresh.
Go local, and delete a chrome folder.  oh but first ya gotta shut down chrome.
C:\Users\asp0363\AppData\Local\Google\Chrome\User Data\Default\Favicons


fonts .... cool, or excessive madness?   ibm plex
https://www.1001fonts.com/ibm-plex-mono-font.html

###### angular on netlify Aug 2020
https://scotch.io/tutorials/deploying-an-angular-app-to-netlify#toc-tldr-how-do-we-deploy-an-angular-app-to-netlify-


###### netlify redirects
https://docs.netlify.com/configure-builds/file-based-configuration/#redirects
what the heck is a splat?
some ruby-ish word that means we dont know yet how many arguments to pass in.
so, somehow redirects (or lack of them) use something splat-ish to route 'bad' request like myApp/foonookoo to a catch all 404.
https://docs.netlify.com/routing/redirects/redirect-options/#custom-404-page-handling
who cares about the wanky name on some user typed in on the URL ???
instead, we might want to redirect requests like myApp/foonookoo to a main SPA page.  
this seems like a better idea when the app is an angular SPA.


###### colors
https://www.sessions.edu/color-calculator/

###### javascript functions
https://www.freecodecamp.org/news/constant-confusion-why-i-still-use-javascript-function-statements-984ece0b72fd/ 
8:54:49 AM: Different functions path detected, going to use the one specified in the Netlify configuration file: 'functions' versus '' in the Netlify UI

1. Create new function in netlify-faunadb-example2/functions/ folder   !! make sure you name it with .js on the end !!
2. add function definition & export to: netlify-faunadb-example2/src/utils/   (func define. export at the bottom) 
3. change the web app to call the new function.  (example React.   App.js)
```
<button  data-id={id} onClick={this.readTodoAndLogIt} > readTodoAndLogIt </button>
... elsewhere, write this funny func.  This is inside app.js, not the netlify external lambda function...
 ////////////////////////////////////////////////////////////////
  readTodoAndLogIt = (e) => {
    const todoId = e.target.dataset.id
    // Make API request 
    api.readTodo2(todoId).then(() => {
      console.log(`read todo id ${todoId}`)     
    }).catch((e) => {
      console.log(`There was an error reading ${todoId}`, e)
    })
  }
  /////////////////////////////////////////////////////////////////
```

Note on logging the function calls ...
inside the /functions/ folder, where we create Netlify Lambda functions --- console.log command writes to the netlify logs.
but in .js files that run in the browser --- console.log command writes to the browser console (visibl e in chrome dev tools).

faunadb crud:
https://docs.fauna.com/fauna/current/tutorials/crud.html?lang=javascript
``` Let’s use a Map function to create several posts at once```

Wes Bos talks about async.  Nice error handling. function yolo()  vs function (safeYolo) 9:15 into the video.
async await is cool, but error handling is hard.  Wes's solution:  a high order function that wraps a function with error handling.
This is not used by the netlify fauna example, but maybe it's a good approach to use in questool.
https://www.youtube.com/watch?v=9YkUCxvaLEk


async await in faunadb  client.query ... probably not exactly what I want ?
https://fauna.com/blog/getting-started-with-fql-faunadbs-native-query-language-part-5

Consider Dave's technique in the his netlify example.
Dave writes a catch block in every function.  it's reasonably short.  Is it good enough?
 ``` Dave's approach```  exports.handler = (event, context) => {           
>vs 
``` possible other approach```  exports.handler = async (event, context) => {     

Dave's approach hints that exports.handler is promise based?
Maybe Dave's approach is good enuff.  we want to avoid callbacks.  I guess it's ok if we use promises with .then
hey, wait a minute.... Dave also has  exports.handler = async (event, context) => { 
in function: todos-create.js and others.
``` for libraries that return a promise, you can return that promise directly to the runtime.```  
https://docs.aws.amazon.com/lambda/latest/dg/nodejs-handler.html

fauna db docs & promises:
https://docs.fauna.com/fauna/current/drivers/javascript.html
>All methods on faunadb.Client return ES6 Promises


Someday, maybe I'll understand exports.handler
http://cloudway.io/post/local-lambda-nodejs-development-environment/

ideas on 'best practices' for fat arrow functions.  look at hint #5 nesting, to make it more readable:
https://dmitripavlutin.com/javascript-arrow-functions-best-practices/

fun swedish guy on javascript functions and automatic tests with jest:
https://www.youtube.com/watch?v=Eu35xM76kKY

Dave uses function literals to compose faunaDb queries. 
``` return client.query(q.Get(q.Ref(`classes/todos/${id}`))) ```
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals 
 
 
###### javascript session management
https://stackoverflow.com/questions/105034/how-to-create-guid-uuid
first, create a UUID for the current user session:
```
function uuidv4() {
  return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
    var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
    return v.toString(16);
  });
}

console.log(uuidv4());
```
store the session UUID somewhere. Maybe a cookie.
when a user does something on drEd5, store the cookie, store the same info in faunaDb.
when a user does something on drEd5, read the info on FaunaDb.
What else should we store about the user session?
 -- faunaDb info, like pagination.

###### angular 
https://stackblitz.com/edit/angular-submit-if-valid?file=app%2Fsubmit-if-valid.directive.ts

###### questionnaire
http://quizbucket.org/what-is-the-default-scope-in-nodejs-application-1429


##### misc
surge to host a site: https://surge.sh/
