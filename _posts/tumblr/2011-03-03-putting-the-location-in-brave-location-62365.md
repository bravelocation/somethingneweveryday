---
layout: post
title: Putting the location in Brave Location (62/365)
date: '2011-03-03T12:00:00+00:00'
tags:
- coding
- location
tumblr_url: http://www.somethingnew365.com/post/44289173809/putting-the-location-in-brave-location-62365
---
Despite really just making it for myself, my Bedside Clock Windows Phone 7 app has now passed 1000 downloads and rising steadily about 50 a day. Very surprising.
The relative success means I’m thinking about doing a version 2, and one of the feature requests was to add in location awareness so it will tell you where you currently are. Obviously if you don’t know where you’re sleeping you’ve probably got bigger problems than a clock can solve, but I do love location aware features so why not?
On the train home on Thursday I managed to get an initial version working, and being in transit was quite useful for testing if it actually worked!
I won’t share the actual code here as it’s not production quality yet - and is a bit dull to be honest - but in outline I did the following:
Used the pattern outlined at http://msdn.microsoft.com/en-us/library/ff431782(v=VS.92).aspx to get the current latitude and longitude
Registered at http://www.geonames.org/ to use their free reverse geocoding service
Used the WebClient code outlined in http://weblogs.asp.net/scottgu/archive/2010/03/18/building-a-windows-phone-7-twitter-application-using-silverlight.aspx to fetch XML from GeoNames using the current location and hence displaying on the screen
It worked reasonably well, although some of the names returned while on the train were a little weird (not really a good use case for a bedside clock though!). The man thing I learnt was the slightly restricted way you make web service calls in Silverlight/WP7
Now I’ve thought about it more, for the next version I’ll probably go with SimpleGeo for the location services, as they offer much richer functionality although it will take a little more programming.
