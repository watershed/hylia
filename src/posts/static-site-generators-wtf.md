---
layout: layouts/post.njk
title: 'Static site generators: WTF?'
date: 2019-07-02T16:02:09.995Z
tags:
  - Publishing
  - WebDev
---
Warning, you have entered the world of web tech, so frequent use of acronyms lurk below (and one sweary one above).

This site uses [Eleventy](https://www.11ty.io) as a static site generator, but what the hell is one of those? 

**Static site generator**, or SSG for short, is an awful, unclear term for a method of web publishing that nonetheless has important advantages over what has become the norm since the rise of blogging 20 or so years ago.

## Where we have been

For most of this century, blogging engines have tended to be  software frameworks that talk to: 

* Publishers, using private pages to enter content
* Databases, where content is stored
* Templates, which generate pages
* Visitors, viewing public published pages

We’ll use WordPress as an example here.

Frameworks like WordPress have tended to use PHP as the software language that does the talking to what is typically a MySQL database. And those kind of Content Management Systems (CMS) do so _on-demand_ much of the time.

Like this: 

1. You visit a web page
2. The web server routes the request to WordPress
3. WordPress looks to see if the content of the page requested has been saved in a place called **cache**: 
    * If the page is cached, the page HTML* is grabbed from there
    * If not, perhaps because content has recently changed, WordPress looks up the right template, has the template make the necessary requests of the database (there are usually many), and compile the results into HTML*
4. The server returns the page to you

(*HTML is the underlying software language of web pages.)

Computers are quick, but this can take quite a bit of time. If the website is eking out resources on a server share with many other third parties, it can take many seconds – and you, the visitor, perceive the site to be sluggish.

Frameworks like this are **dynamic** in the sense that they rely upon highly contingent processes every time a page is requested.

## The snappier SSG alternative

By contrast, SSGs save every web page as an HTML file, ready to be served straightaway. The net result is that: 

* Steps 2 and 3 above become redundant, and so too does the database
* Pages are returned to the visitor _much_ quicker – and reliably so because it is the same process running every time
* The system is not vulnerable to potential flaws in the processes running at steps 2  and 3 – there is a lot less to ‘hack’.

SSGs are **static** only in the sense that there are fewer  processes interjecting to serve a web page. 

To confuse things further, the content in the pages themselves doesn’t have to be static. It can exploit all the bells and whistles of modern web code to deliver animation, transitions, video and audio just like any other web page coming out of a ‘dynamic’ publishing system.

Which is why ‘Static Site Generator’ is a terrible term for a very good idea.
