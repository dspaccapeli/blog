---
title: "Hello World!"
date: 2023-01-03
layout: post
---

I made this website. And it is something special.

It has been a while I wanted to create my space online and wasn't satisfied with the alternatives. WordPress is more expensive than I'd like to without hosting without headaches. To do simple stuff you need to fight with the system and if you want to customize it you still need get your hands quite dirty. Other alternatives were also not satisfactory for multiple reasons. I want something simple.

But truth to be told, the most important part is that I wanted to train my builder muscles.

![Watercolor image of a hammer and stone in front of a monitor]({{ '/assets/images/230103-1.png' | relative_url }})

So, I started with simplicity and an idea in mind. A website should have the fewest moving parts as possible from the user’s point of view. I wanted to remove things.

First, let’s get rid of online text editors embedded in the blog. We have already plenty good text editors: LibreOffice, Microsoft Word, Google Docs, etc. Why should we reinvent the wheel? Have the website and the editor experience be separate. The website should be a simple, easy to maintain host of content and leave the editor to think about the typesetting, corrections, colors, image embeds and so on.

I went even beyond, by removing a login panel. I wanted the user to go as fast as possible from having their document ready on their computer to live on the blog. Let the user (me) drag and drop a file on the website (after authenticating, which is instant after the first time) and let me upload it to the server. This is achieved in one sweep by using the IndexedDB API (a lot of cool things can be done with underused/not-so-new APIs). The server then would take care of converting the website to HTML, extract the media, meta data and updating the database.

Here is a demo:

<iframe width="560" height="315" src="https://www.youtube.com/embed/47ADnXnrrc0" frameborder="0" allowfullscreen></iframe>

I find it pretty cool!

For the more curious, this is the high-level architecture of the thing. As you can see, I use a relatively simple and straightforward stack. Some may say outdated and unscalable: SQLite, PHP, shell scripts. But it is simple and most importantly... works.

![Diagram of the website architecture]({{ '/assets/images/230103-2.png' | relative_url }})

**Update:** This blog has since been moved to GitHub Pages to reduce costs and simplify hosting while maintaining the same goals of simplicity.

