---
title: The Joy and Sorrow of Markdown  
date: 2017-02-03T00:00:00.000Z
author: Nobody Cares
summary: I am taking over fourthpost .md   to write some handy tips about markdown.  Yes, this is opinioned.  Yes, I am grouchy today. A goal--  learn enough about markdown, to see if I could adopt an approach to web pages, where I use markdown files for the content (mostly text), and rely on the web page programming to do the layout and format.
tags:
  - environment
  - politics
  - programming
---

markdown file naming:
This file is called fourthpost .md but maybe the name is unimportant?
like, I could create another post called legCramp .md and stick it on github in the right folder,
and it would be added to this blog?

OK, so what should I type in this markdown file?  My words and wisdom, of course, but should I be concerned about format?

in the top section of this .md file,  (Front Matter) I stuck in an extra colon.  Bad move.
summary: I am taking over fourthpost .md   to write some handy tips about markdown.  A goal: bla bla 
This causes a failure when 11ty or netlify (or some pre-processor) tries to blend this markdown into the web pages.
<br>
Chris Coyier is a smart guy.  Here he talks about markdown and blogs:
https://css-tricks.com/probably-blog-markdown/

<br><br><br>

BULMA AND MARKDOWN INCOMPATIBILITY
When sticking markdown characters in my .md file, like
greater than sign, pound sign, equal sign, line break slash  
The markdown gets transformed to html, but then
Bulma takes liberties with the generated html tags.
Bulma over-rides the classes and psudo classes of the tags,
like h1 no longer appear bold.
when markdown gets iffy, I hackishly insert some old fashioned html.  Here are three br tags:

<br><br><br>

A guy created some css to hack past the bulma/markdown mismatch.
The idea is you override some bulma styles with old fashioned styles
for h1 blockquote  (etc).  Maybe just borrow a couple of styles here,
and insert them into the top of my custom bulma.css file that is in the
includes / css folder of this githup repo.
https://gist.github.com/joallard/06f113b690d5553d90187a53bc38cb15

<br><br><br>
line break experiments go here ...

I am hitting enter as I type, to put in line breaks.
Like this.
And this.

Ready for some blank lines?  here are three of them:



OK, those three blanks did not appear on the web page.  now try three 'blank line's with a greater than sign in front:
>
>
>
inserting blank lines in markdown.... Not sure how., without that br hack. 
<br><br><br>

another line break test here:  poundsign + blank:
# 

paragraph testing folows:
<br><br><br>
If I just type on and on, and on and on,  and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, and on and on, then what?

> So, here I am trying to do old school Markdown. I stuck a greater than sign on the front of this.  I am just typing away, as if I was a real author.  I don't worry about line breaks.  I am just typing like I am inside a word processor.  Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way. Everything is beautiful, in its own way.  Now I am at the end of the paragraph.

Now I am starting a new paragraph.  And all the joy that comes with it.  Let me repeat that:  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  all the joy that comes with it.  Now I am at the end of the joyful paragraph.


This page has some examples of how confusing the content vs layout can be.
I am typing inside a file called fourthpost.md
Notice markdown or 11ty transforms text with a .md  to a nonsense link.
Notice markdown does not transform text like this --> blewMyNoseTooHard.txt

So, now as I type, I have to be aware of Markdown rules.
Like, where line breaks come in.
and whether I can stick a greater than sign on the front of text, like this:
> hello I am text with a greater than sign in front.

here is my attempt at three blank lines, by putting a slash on the line:
/
/
/
here is my attempt at theree blank lines, by putting space space slash on the line:
  /
  /
  /  
  

ok, equal sign below this line makes this line transform to bold, but only in the markdown editor.  sheesh.
=

^^^ trying three carats for a divider
^^^
Markdown creates h1 stuff when you stick a pound sign on the front of text, like this:
# hello I am a header.  This line has a poundsign on the front.
 
For pound sign header, the text appears bold in the markdown editor, but that is probably cuz the github editor is taking liberties.
I see the generated html has the h1 tag, but BULMA overwrites it with bulma.css
^^^
If I was to create .md files outside of github, then upload those .md files, then maybe I would be happier.
^^^




here is markdown for a sample image, escaped with three quotes on the front and back:
'''![A sample inlined image](https://source.unsplash.com/random/600x400)'''
here is markdown with a sample image:
![A sample inlined image](https://source.unsplash.com/random/600x400)

So, now I know how to stick images in this markdown, instead of images in the html.
When do images belong in html ? (or in an njk file in this case) 
What images belong in the .md file?   (maybe blog-ish images?)
When is the blogger a different person than the web page programmer?
What does a blogger have to know about that damn web page programming?

As a blogger, I guess I have to follow rules when creating .md files:
a) stick some front loader stuff in the top of the .md file 
a) the web page programming uses bulma, so dont type pound sign and other characters in the line starting character.
b) inserting image 'reference' is OK, but this reference means a link to somewhere, so the image is NOT stored with the .md file.


