---
layout: post
title: Programming using the iCalendar data format (9/365)
date: '2011-01-09T16:35:00+00:00'
categories:
- calendar
- coding
tumblr_url: http://www.somethingnew365.com/post/44289261050/programming-using-the-icalendar-data-format-9
---
As you may know I ran an unofficial website for Halesowen Town for many a year back in the day. I stopped doing it a few seasons back after I got sick of all the moaning and bitching, but I still maintain my records of all the team’s matches on there.
I was thinking about our upcoming fixtures, and how I used to add them at the start of each season to my calendar by hand, when I had an idea - a pretty obvious one now - I should use the database on the site to create an iCalendar feed so I can automatically have the fixtures in my calendar.
The iCalendar format is pretty old school, in that it’s a text-based format rather than anything more modern like XML or JSON. I couldn’t find many examples on the protocol usage, but as usual Wikipedia came up trumps with a basic outline to get me started.
After all that research, it didn’t take long to adapt an existing ASPX page that showed fixtures and results to return the data in the correct format, and hence I could add it to my Google calendar. The feed is at http://www.yeltzland.net/anorak/calendar.aspx if you have any interest in HTFC’s upcoming games :-)
The data format has some interesting features I didn’t know about, including pretty good support for events, to-dos, journal entries and a lot of the things you’d want in a PIM. Definitely could be useful in some future projects I’m planning.
