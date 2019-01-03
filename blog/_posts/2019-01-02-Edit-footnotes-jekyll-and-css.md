---
title: "Working With Footnotes In Jekyll And CSS"
date: 2019-01-02 13:55
bigimg: /img/2019-01-02-css-footnotes-featured.jpeg
tag: How To
---
Whilst spending far too long redesigning this blog, I've come to the conclusion that it look fine the way it is and I couldn't be bothered with a huge change. So instead I've been looking into changing some of the small things. Many of these were pretty easy, but my biggest one was the styling of footnotes.

Whilst trying to get to the bottom of exactly how I change the styling, there wasn't a great deal of help out there to help. Information on the CSS related to Footnotes is quite confusing. Much of it was out dated and didn't really apply when using a Jekyll blog. I managed to find a few bits of info and do a bit of testing and it turns out it’s pretty easy to do.

## Jekyll Stuff
The easiest way to do this is to default to the markdown variation Kramdown. This already has footnotes built into it and displays them at the end of the article content. The vast majority of Jekyll blogs out there already use Kramdown, so you might not have to do anything, to check just have a look for `markdown: kramdown` in your `_config.ymal` file.

## The CSS Stuff
This is where most of the information falls down, many resources will tell you to mess around and create a class for your footnotes so you can style this in CSS. That might be the case using Wordpress or HTML but Kramdown presents it all neatly in HTML for you to style. There are two different parts you are able to change if desired.

* The initial footnote that appears in the article contents, in your sites CSS this is the `.footnote`.
* The text showing information at the bottom is a serrate entity. This is what most people refer to as the citation, and this is styled using `.footnotes`.

It is pretty easy to get these confused but dead simple to style them both individually. All of the links and notes adopt the formatting of your regular content, but I wanted the footnotes to appear closer together and also in slightly smaller fonts as they do in academic papers. I also chose to add in some brackets around the footnote (a la Wikipedia) to highlight them a little more. My CSS snippet is as follows.

```
footnotes {
  font-size: 14px;
  margin: -10px 20px;
}

.footnotes p {
  margin: 10px;
}

a.footnote:before {
 content: "[";
}

a.footnote:after {
    content: "]";
}
```

You can of course customise until your heart is content. This might seem pretty obvious to those in the the know, but I struggled to find any conclusive information easily. Hopefully this helps a little, I am still learning myself so wanted to put some information out there to try to help others.
