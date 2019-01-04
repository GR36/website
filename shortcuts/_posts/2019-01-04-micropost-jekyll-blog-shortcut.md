---
title: "Shortcut: Micropost To Jekyll Blog"
date: 2019-01-04 14:14
bigimg:  /img/2019-01-04-coding-MacBook.jpeg
tag: shortcuts
---
You may remember me trying to quit Twitter (well in fact I've tried several times) and [start using micro.blog](https://www.gr36.com/2018-05-25-you're-not-cool-enough-for-micro.blog/). This didn't work, for various reasons, so I have resurrected my project to try and [build a version](https://www.gr36.com/2018-01-20-building-a-micro-blog-on-jekyll/) on my own blog.

This is pretty easy to get off the ground but I never got it to a stage I was happy with. So after searching the web, and a bit of inspiration from [Jordan Merrick](https://www.jordanmerrick.com) I set to work on completing the project. The one thing I have always fallen down on is the auto posting to social media, I want text of less than 280 characters to go straight to Twitter, and anything longer to be posted to my blog but the title and link sent to Twitter like a regular blog post.

I'm not proficient enough in coding to write something myself, so after a bit of destitute thinking I fell back to something I do know enough about - Shortcuts. 

![](https://gr36.com/img/2019-01-04-micropost-shortcuts-screenshot.png)
[Download the Shortcut](https://gr36.com/shortcuts/files/Micropost-Jekyll.shortcut)

By using a simple count characters and If statement I can share some text to it and let the magic happen - kind of. It isn’t ideal, I would really like this to work automatically but it is the best I have so far, the rest of the shortcut will add in all the Jekyll front matter and post this to github using their API. No messing around with commits and nothing to sort out, You can customise the front matter to make sure the post is formatted to your specification and also so it is tagged or posted in the correct collection dependant on your blog. 

Mine is built after each commit by Netlify and all my micro posts are displayed on an index found at [gr36.com/micro](https://gr36.com/micro/). I can share some text written in any app, but by far the easiest is [Drafts](https://gr36.com/2018-04-29-finding-use-for-drafts/).
