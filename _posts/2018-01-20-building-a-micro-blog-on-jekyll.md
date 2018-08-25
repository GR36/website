---
title: Building A Micro Blog On Jekyll
date: 2018-01-20 16:14
bigimg: /img/2018-01-20-microblog-howto-featured.jpeg
tags: [howto]
---
After exploring other options to sharing on social media and [using Micro.blog](http://gr36.com/2018-01-20-using-microblog/) I’m stuck. There doesn’t seem to be the perfect option out there to fulfil all of my needs so for now I still to my own blog. 

Now comes the issues with posting lots of updates and where they need to go. Ultimately there are a few things I want to achieve. 
* Keeping content mine as much as possible
* post to other social media platforms
* not clog up longer blog post streams or RSS

Since my blog is already built on Jekyll and hosted on Github I set to work to hit as many of these goals as possible.

## Keep content mine
The main feature of my [micro.blog usage was for Daring Fireball style link posts](https://gr36.micro.blog). Short quotes from other peoples articles (linking back to them) and a few words (sub 150) from my self as a comment. I built a Workflow to do this easily on micro.blog so sharing these shouldn’t be a major issue. 

### Micro Blog Collection
Inside your \_config.yml set up a collection with a name of your choice. Seeing as this will be aimed at micro blog I went for something easy.

```
Collections:
micro:
	  output: true
	  layout: post
	  permalink: /micro/:title
```

This will mean that posts in this collection will not be posted to the main index page and also not in the main RSS feed. Create a folder called \_micro for all the micro posts to go into. 

![]({{ site.baseurl }}/img/2018-01-20-github-screenshot.png)

### Micro Blog Index
In the main repo create a file called micro.html and set the YAML with a permalink as /micro/index.html. Example below:

```
---
layout: page
permalink: permalink: /link/index.html
title: Link Posts
---
```

Then it’s time to get all of your posts listed, this is pretty easy to do and will ultimately be dictated by what info you will want to see on an index page, the below is the contents of mine. This page will then be found at /micro/. 

```
{ % for item in site.micro reversed % }
<article class="post-preview">
  { % if item.link % }
	  <a href="{{ item.link }}">
  <h2>{{ item.title }}</h2>
  </a>
  { % else %} 
  <h2>{{ item.title }}</h2>
	  { % endif % }
  <p>{{ item.content }}</p>
</article>
{ % endfor % }
```

I have chosen to only show the title and then all of the content as these will only be small posts. The If item.link is unique to my use case and means that if I set a link in my YMAL front matter the title will link to this URL in a similar vein to Daring Fireball. 

The <article\> tag is set in my CSS and simply adds in the same formatting as my blog and separates the posts neatly. 

If in doubt copy the content from your index.html and add in `{ % for item in site.micro reversed % }`. 

### Micro Blog RSS Feed
This might come as a shock but if you’ve got a regular blog people won’t want to read a barrage of micro updates. So a collection and separate RSS feed is a must. This is the easiest part of the set up. Simply create a file called micro.xml and add the following:

```
---
layout: null
---
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
  <channel>
	<title>{{ site.title | xml_escape }}</title>
	<description>{{ site.description | xml_escape }}</description>
	<link>{{ site.url }}</link>
	<atom:link href="{{ site.url }}/micro.xml" rel="self" type="application/rss+xml" />
	{ % for post in site.micro reversed % }
	  <item>
		<title>{{ post.title }}</title>
		<description>
		  {{ post.content }}
		</description>
		<pubDate>{{ post.date | date: "%a, %d %b %Y %H:%M:%S %z" }}</pubDate>
		<link>{{ site.url }}{{ post.url }}</link>
		<guid isPermaLink="true">{{ site.url }}{{ post.url }}</guid>
	  </item>
	{ % endfor % }
  </channel>
</rss>
```

All of your posts in the Micro collection will now be delivered through this separate RSS feed. So you can set this to post to social media through IFTTT or many other places as you desire however there are limitations. 

![]({{ site.baseurl }}/img/2018-01-20-socialmedia-links.png)

## Cross Posting
This is where I fall down. I haven’t found a way to share full posts that are below 280 characters straight to twitter and longer ones as links. I am pretty sure this is achievable however I stopped short when realising almost every one of my posts was way past this limit. 

I believe there may be a way to do this with a limited RSS \<description\> of 280 characters. However in practice this hasn’t worked for me to auto post through IFTTT. If this is a major issue for you then micro.blog is the place for you! 

Hopefully this helps with improving your Jekyll site and can be modified to your use cases for collections. I am currently adapting this to add in a few collections so the possibilities are endless. 

