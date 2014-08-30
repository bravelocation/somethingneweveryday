---
layout: post
title: Fixed bug using App Hub stack traces (221/365)
date: '2011-08-09T20:14:00+01:00'
categories:
- coding
- phone
tumblr_url: http://www.somethingnew365.com/post/44061575973/fixed-bug-using-app-hub-stack-traces-221365
---
Technical post: I wanted to check how my Bedside Clock app downloads were doing (tailing off but up to 4,700+), but found out that the [App Hub](http://create.msdn.com/) website has been updated to show stack traces of crashes users have the phone have experienced.

This is a great feature, and I easily fixed the code up to handle more gracefully if some malformed XML is returned from a web service I’m calling.
New version out as soon as I can release my newly Mangofied app.
