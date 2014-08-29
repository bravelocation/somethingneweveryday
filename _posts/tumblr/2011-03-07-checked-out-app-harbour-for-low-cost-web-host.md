---
layout: post
title: Checked out App Harbour for low cost web hosting (66/365)
date: '2011-03-07T12:00:00+00:00'
tags:
- computing
tumblr_url: http://www.somethingnew365.com/post/44289172584/checked-out-app-harbour-for-low-cost-web-host
---
I’ve been running a few of my small websites/apps on Google App Engine recently, mainly because the price point is really good (i.e. free). It’s not been a bad thing as it means I’ve been learning more about Python, but it’s really a shame WIndows Azure doesn’t have a free entry point.
Thanks to my friend @saqibs yesterday I checked out App Harbour, a web site that almost solves the problem. It runs on top of Amazon Web Services, and allows single instances of Visual Studio web solutions to be hosted for free - with a scaleable solution for when you need more.
This looks really promising, but the coolest thing is the release process. You can just do a push to their server via Git (or even better Mercurial coming soon) and it will automatically build and deploy your code. What a great idea.
Even better, if you add unit tests it will also automatically run them before deployment, and only go ahead if the all pass. Genius.
I don’t have anything to deploy there right now, but it’s definitely an option for future projects where ASP.Net and C# are the preferred options.
Update: Mercurial is now available accoprding to http://support.appharbor.com/kb/getting-started/using-mercurial-on-appharbor
