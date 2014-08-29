---
layout: post
title: Hacked together a near realtime RSS->Twitter solution (50/365)
date: '2011-02-19T12:00:00+00:00'
tags:
- coding
tumblr_url: http://www.somethingnew365.com/post/44289181959/hacked-together-a-near-realtime-rss-twitter-s
---
Day 50. Is that all? Seems like I’ve been desperately casting around for something new to do each day for years :-(
A technical post today.
For a while the Yeltz Forum - a discussion board that I help out on as “technical adviser” every so often - was locked down so only registered users could see the posts. If you’ve been following the recent history of Halesowen Town Football Club, you’ll know things have been pretty contentious over the past couple of years, with administration, court cases, cigarette smuggling and all sorts of fun, so we wanted the site locked down so we knew who was viewing it. However things have settled down a bit now recently (in a bad way as we’re terrible on the pitch right now) so now anyone can see what’s on the site.
What this means is that we can now get the posts from the site on Twitter. This is reasonably useful, as the “Match Updates” section is the only good way of getting near real-time reports of live games, which makes it the perfect candidate for putting on Twitter.
There are several RSS->Twitter sites out there, and I decided to go with Google’s Feedburner which offers lots of functionality as well as the Twitter integration
The key problem I had to solve was the default update speed is every 30 minutes, which is fine for most of the time but when the match is being played I’d like updates in as near real-time as possible.
Luckily Feedburner has a Ping feature in which you can hit a URL and it will refresh the RSS feed - and hence the Twitter feed if something has changed. With a bit of simple Python programming I got a cron job running on my AppEngine site calling the Ping server every minute during game time, and we were in business.
You can see the results on Twitter at @yeltzforum - but don’t look too closely as you’ll see evidence of yet another drubbing in yesterday’s game :-(
