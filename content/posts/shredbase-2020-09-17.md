+++
title = "Shredbase (2020-09-17)"
date = 2020-09-17
lastmod = 2020-09-17T11:56:36+03:00
tags = ["shredbase", "webdev"]
categories = ["development"]
draft = false
weight = 2002
featuredImage = "/images/metal.jpg"
+++

Well, much has happened since my last dev diary (I have to somehow make more
updates about my projects.), and the plans with Shredbase changed quite a bit.


## No to AI {#no-to-ai}

Natural language processing seemed like a prime candidate for analyzing
comments, but looking at how redditors structure their comments, I had to give
up on this idea. Very few of them formulate complete sentences when they're
recommending bands to listen to, mostly posting a YouTube link, or writing a
short comment with the **Band Name - Song Name** structure. Luckily, I've found
easier ways to extract band recommendations.


## The recommendation section {#the-recommendation-section}

The way things are now, I simply search for the inputted band name in the
recommendation tab, extracting YouTube links from the responses using RegEx. The
only problem right now is that there are too many bands in existence, so I
haven't made a central database with their name yet, right now every search
query is made from the ground up.
This impacts performance right know, and it takes about 5 to 6 seconds to return
the results. I'm planning to introduce every search query in the database, so
the same search query will return the results instantly at the second time when
the band is searched.
Another problem with this approach is that I simply search for the band name in
the top level comments, so a comment like "I don't really like Metallica, could
you guys recommend me something else?" would also return results when the user
searches for Metallica.
Since I only extract the YouTube links from the answers, the number of results
is low when users are searching for not so well known bands. I have to figure
out an approach to include text-only recommendations as well.


## The What Have You Been Listening To section {#the-what-have-you-been-listening-to-section}

The second feature of my website is much more successful right now. Since r/metal
users are encouraged to explain why they like the band they're talking about, I
can include this explanation next to the video, which makes a much more familiar
and interesting experience.
I parse the comments with the BeatifulSoup library, first searching for words
which are emphasized in bold, because usually that is how users emphasize their
listened band and/or songs. Roughly 70-75% of comments are useful, but this
approach isn't without faults, since sometimes somebody begins their paragraph
with **Not Metal** and the YouTube video I return is, well... about plastics and
non-metal elements of the periodic table. If I would have the necessary knowledge and
computing power to do intelligent text-analyzing, I could filter these comments,
but I think it's a funny **feature** so to speak.
Right now, the most recent 100 WHYBLT submissions have been parsed and
introduced into the database with over 6000 comments, and I have discovered many
cool underground bands with my own website, which I see as an absolute win!


## Plans going forward {#plans-going-forward}


### Recommendation section {#recommendation-section}

I might polish the recommendation section a little bit further, so it includes
more responses, and I have to make database tables for the bands and
recommendation to cache frequent queries.


### WHYBLT section {#whyblt-section}

I'm going to write a scheduled Python script which parses every sunday that
weeks WHYBLT submission, so that Shredbase would keep up to date with the weekly
metal experience.


### Hosting {#hosting}

The current plans for now are that I will host my website on my personal
media-server, based in Germany. Right now, I don't think I will get much traffic
for the website, but if this were to change, I might invest in a dedicated VPS
for it.
