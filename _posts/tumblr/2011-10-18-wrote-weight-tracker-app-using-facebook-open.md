---
layout: post
title: Wrote Weight Tracker App using Facebook Open Graph (291/365)
date: '2011-10-18T18:23:00+01:00'
tags:
- coding
- facebook
tumblr_url: http://www.somethingnew365.com/post/43670341296/wrote-weight-tracker-app-using-facebook-open
---
I had a load of fun yesterday hacking out a website/app that uses the new Facebook Open Graph.
If you’ve been following closely I’ve been pretty obsessed over the last few weeks with both dieting and tracking my weight online. I’ve been looking for something to integrate into the new Facebook Ticker and the Timeline, so I wrote a Weight Tracker App to do just that.
Following the Open Graph tutorial I managed to get my actions and objects set up reasonably quickly, and from there it wasn’t too much effort to be able to post weights on given dates into both the ticker and my timeline. Hurrah!
Next I wanted to pull the data back from Facebook and show on a graph. The FB API call was easy enough, and I decided to use the Google Graph API for the graphical part. What took the longest time was getting two asynchronous Javascript APIs to work together reliably, and I think that now works OK.
I’ve submitted my app to Facebook for approval, but they said that won’t happen until the Timeline comes out of beta. What that means is I don’t think you can use the app yet so you’ll have to take my word for it - although I think I might be able to add people as testers etc. if you really want to try it.
