+++
title = "Beginning this whole Hugo thing"
date = 2020-05-14
lastmod = 2020-05-14T22:40:49+03:00
tags = ["hugo", "org"]
categories = ["announcements"]
draft = false
weight = 2001
featuredImage = "/images/beginning.jpg"
+++

## What's this blog all about {#what-s-this-blog-all-about}

To share the love for the one and only OS, Emacs of course. Well, not entirely.
It will contain random snippets of thought, both professional and
unprofessional, so it will reflect my thoughts on the current state of certain
software projects which I discover. In the beginning this going to be a bit
self-centered, as it will also be a kind of "self-documentation" I suppose, but
this could change easily.


### Implementation {#implementation}

I'm writing this whole website inside of Emacs, taking advantage of a couple
of wonderful things, built by wonderful people:

-   [Hugo](https://gohugo.io) is a static site generator written inside of Go. You can use various
    formats to edit the content of your website, but the most sensible choice is
    Markdown, because that's what Hugo is really optimized for. The advantages of
    this approach as opposed to a non-static website is that the only HTTP request
    happens when the user loads in the page, making databases unneccesary, and
    making the whole website a lot faster.
-   Markdown might be amazing, but every citizen of the Emacs realm knows, that
    org-mode is the shit. But how can you use org mode
    for your website, when you have to use markdown? [ox-hugo](https://ox-hugo.scripter.co) to the rescue! This
    wonderful Emacs package not only enables you to convert your org thoughts to
    Markdown, but also has the ability to export a single subtree into it's own
    post, making possible to write all of your blogposts in a single place, taking
    advantage of various org-mode tricks (**or so am I told, I actually still don't
    know very much about them**). See for yourselves:

    {{< figure src="/images/org-mode-big-brain.png" >}}

    Amazing isn't it? Well, I have to learn much more about this org thing, to
    take advantage of it, but it's sure easier updating the Github page
    of the website, when it's only one measly file.
-   [Doom Emacs](https://github.com/hlissner/doom-emacs). Well of course we cannot forgot the star of this evening, the
    whole reason I'm going far and beyond in my static website setup. But it is
    totally worth it. In the near future, there will be posts about my workflow,
    and all the pain and suffering which came because of it, but it's all possible
    thanks to hlissner's efforts. If you're still using Vim, Spacemacs or use
    Emacs, but you're not sure how to configure it yourself, give this distro a
    spin, I'm sure you'll get something out of it.

    {{< figure src="/images/doom-emacs.png" >}}


### Future {#future}

I'm planning to write a Spotify frontend for Emacs, because I'm too lazy to
switch workspaces to do such a trivial task, so yeah, instead of relying on some
wonderfully written programs, like [spotify-tui](https://github.com/Rigelutte/spotify-tui), I'm wondering of a wild path,
and write my first Emacs Lisp package. This thing is one of the reasons I
started this blog, because I thought it would be fun to document the whole
process, maybe some fortunate soul will learn from my mistakes.
