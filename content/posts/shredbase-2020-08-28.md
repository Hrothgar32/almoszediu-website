+++
title = "Shredbase (2020-08-28)"
date = 2020-08-28
lastmod = 2020-09-06T19:31:28+03:00
categories = ["development"]
draft = false
weight = 2001
featuredImage = "/images/metal.jpg"
+++

It's not the first day that I began to work on this project, but this day I felt
like I began to see my effort being worthwhile.

Shredbase is going to be a sort of metal band recommending site, which will base
it's recommendation on the r/metal subreddit.


## Challenges {#challenges}


### Natural language processing {#natural-language-processing}

Since my recommendations will be based on Reddit comments and posts, I need to
find a way to extract this information from the many English text and organize
it into links, pictures, names and numerical information.

Fortunately, the language of my choice for the backend is Python, which has many
libraries which can help me. I chose [spaCy](https://spacy.io/), since it's open source, has great
documentation and it's intuitive to use. Another advantage for it is it's great
[interactive tutorial](https://course.spacy.io/en/), which teaches me to use it from zero to hero.
The only other NLP solution that I've used was [Wit.ai](https://wit.ai), but that company has been
aquired by Facebook and it's not a library, but an API which brings in the
danger of data mining by a third party, and I'm not a fan of that.

I will probably try to achive something similar to it's **intent-entity** system,
but the exact implications will be in the future.


### Database caching {#database-caching}

It would be quite tedious to run the NLP program every time a user wants to find
similar metal bands to say, Metallica, so I plan to save the results in an SQL
Database. I'll probably use MariaDB and the effectiveness of the whole operation
will depend on the demand of the website.


### Getting the data {#getting-the-data}

Python to the rescue! Some really cool people have already written a wrapper for
the Reddit API called [PRAW](https://praw.readthedocs.io/en/latest/), which will help me tremendously. This wonderful tool
can extract comments, posts, upvotes, and everything you would need to get
Reddit data. Since I won't give away the gathered data to third parties, I think
I won't violate any Reddit guidelines.


### Frontend {#frontend}

I'm more of a backend guy, and a terminal-lover but to a certain extent only. I
myself like nicely written, accessible UI-s with a good experience, so I will
try my best to write something enjoyable to use.

I will use React.JS as my frontend-framework, since I've worked with it before
(the [Media Server Project.](https://movie.almoszediu.com)), and work with it is an enjoyable and intuitive
experience. I'll probably use some free heavy metal font for logo, and animate
some simple flames around it.

The background will be black of course.


## Progress (so far, and today) {#progress--so-far-and-today}


### API {#api}

I've outlined the skeleton of my API based on the first two functions of my
website:

-   Recommend bands through a similar band.
-   Recommend bands through a subgenre.
    Not particularly elegant, but it helps to keep the scope of the project
    manageable. Sometimes remote procedure call is all you need.


### UI {#ui}

I'm relearning React.js because the last time I've used it was some 2 years ago,
and many things have changed since. So... I shouldn't use Redux, Hooks are not a
buzzword anymore, and screw classes? I guess that's how we roll now.


### NLP {#nlp}

I'm learning the spaCy library with their online interactive course, which is
quite good, but I'm also documenting my progress in an org file. The good thing
about Org mode is that you can execute code and view the results just like in
Jupiter Notebooks.
This way I'm gonna make myself a cookbook which will help me out if I'll forget
something along the development process. And believe me, I most certainly will
forget stuff.


## Future {#future}

I've got some things on my plate right know, since I might begin some additional
projects very soon (some of them for clients), but I'm confident in my abilities
to realize this fun utility website. I hope it will be of great use to me, and
other metalheads as well.
