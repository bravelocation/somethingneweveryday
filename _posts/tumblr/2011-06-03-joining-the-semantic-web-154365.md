---
layout: post
title: Joining the semantic web (154/365)
date: '2011-06-03T18:43:00+01:00'
tags:
- coding
tumblr_url: http://www.somethingnew365.com/post/44286008031/joining-the-semantic-web-154365
---
Following the announcement on the big 3 (2?) search engines about trying to standardise structured data in web pages via http://schema.org/, I thought I’d join the party and add some data to Josie’s website.
One of the standard schemas is for a painting, so it was pretty easy to add the appropriate markup to each page on the website that shows an image.
For example, the HTML for the image page of William Blake/Johnny Depp was amended to add a few extra attributes:
<span itemscope itemtype=”http://schema.org/Painting”>
  <div class=”imageContainer”>
    <a href=”/gallery/image.aspx/icons/Juno” id=”ctl00_MainContent_imageLink”><img src=”/gallery/images/current/WilliamBlake.jpg” id=”ctl00_MainContent_mainImage” itemprop=”image”   alt=”William Blake” /></a>
…
    <h1 class=”imageTitle” itemprop=”name”>William Blake</h1
   <div class=”imageDescription” itemprop=”description”>37 x 66cm oil on canvas 2010</div>
   <div class=”imageAuthor” itemprop=”author”>Josie McCoy</div>
… 
</span>

It will be very interesting to see if the initiative takes hold any more than the existing structured data formats that already exist. I guess if there are clear benefits in terms of search rankings, they almost certainly will.
