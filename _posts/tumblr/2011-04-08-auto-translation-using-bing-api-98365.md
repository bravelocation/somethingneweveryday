---
layout: post
title: Auto translation using Bing API (98/365)
date: '2011-04-08T12:00:00+01:00'
categories:
- coding
tumblr_url: http://www.somethingnew365.com/post/44289145765/auto-translation-using-bing-api-98365
---
One of the more surprising things about the success of my Bedside Clock app is how it’s used in over 15 different countries in the world. So for version 2 I thought I’d make it better for them by translating the few bits of text in there into many languages.
Luckily I found a brilliant tool from Microsoft Consulting in the UK that can automatically translate resource files using the Bing Translation API. This worked really well, and after following the slightly cryptic instructions at http://msdn.microsoft.com/en-us/library/ff637520(v=VS.92).aspx I managed to get it working in French, German, Italian, Spanish and Dutch.
One slightly painful thing was the apparent lack of support for language only resource files, so I had to make one per market, but overall I’m very happy with the results.
