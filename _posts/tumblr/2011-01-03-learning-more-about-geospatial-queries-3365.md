---
layout: post
title: Learning more about geospatial queries (3/365)
date: '2011-01-03T15:15:00+00:00'
categories:
- coding
- location
tumblr_url: http://www.somethingnew365.com/post/44289266273/learning-more-about-geospatial-queries-3365
---
It’s the last day before I’m back at work (and in London) tomorrow, so obviously I wanted to make the most of the day and spend it on my computer :-) This means today’s post is quite a technical one, so iff you’re not a software engineer, you may want to look away now.

What I’ve been looking into is efficient geospatial queries i.e. how to find a set of points that are close to a specific point. I’ve got some ideas for some projects for both work and personal use which need this, which in a crappy “it sounds more interesting than it is if it’s secret” way, I can’t really talk about right now.

First off was to understand how to calculate distance between two latitude/longitude points. This is a reasonably well-known algorithm which I have used in the past, and this page gives a good explanation and code examples in C# and JavaScript: [http://pietschsoft.com/post/2008/02/Calculate-Distance-Between-Geocodes-in-C-and-JavaScript.aspx](http://pietschsoft.com/post/2008/02/Calculate-Distance-Between-Geocodes-in-C-and-JavaScript.aspx)

Now this is useful in general purpose queries, but I’m using Google App Engine for hosting some of my personal projects (not the work ones for obvious reasons). I’m doing this mainly learning new skills - Python in particular - and also having a free entry point for low-usage sites makes it massively more attractive than Windows Azure when you’re just playing about. I’ve no idea why Microsoft don’t offer this option :-(

Anyway, one of the drawbacks of using simple entity stores like the App Engine Datastore is that they don’t offer complex “WHERE” clauses in the native query languages. You could implement a query using the algorithm explained above at runtime, but clearly this wouldn’t be very efficient as you’d be doing a lat/long comparison on every entity in the datastore rather than using the native processes of the datastore itself.

A bit of research found a very interesting article at http://code.google.com/apis/maps/articles/geospatial.html - which explains one rather clever approach to exactly this problem. The article explains it in full, but in essence it simply:

* Breaks the lat/long two dimensional space into a grid of referenced squares
* The larger parent squares have a shorter label than the squares contained within it

For example, the grid square labelled “a7c52b” has a larger parent square of “a7c52”, which also has a parent square of “a7c5” …

This means you can use a StringListProperty type in the App Engine datastore to hold the set of any lat/long point’s parent squares, and hence with a bit of care you can do a simple “WHERE” query at the appropriate accuracy level. Very clever!

Other options discovered include:

* Geodatastore - http://code.google.com/p/geodatastore/wiki/HowItWorks
* Google Fusion tables http://www.google.com/fusiontables/public/tour/index.html
* Geohashing - http://en.wikipedia.org/wiki/Geohash

In summary, I definitely learnt a new algorithm for efficiently storing lat/long points in an entity store in an easily queryable way, so it both passed a fun couple of hours and meant I could keep my #new365 streak going :-)
