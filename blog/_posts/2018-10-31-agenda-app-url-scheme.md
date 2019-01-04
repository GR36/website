---
title: "Agenda App URL Scheme"
date: 2018-10-31 10:57
bigimg: /img/2018-10-30-agenda-hero.png
tags: Automation, How To
---
The opinions on Agenda app range from excitement to confusion but it has caused quite a stir in iOS productivity circles. The developers are constantly improving the app and there are now a bunch of automation options available for Agenda via x-callback URL.

You can use these in Shortcuts or a whole range of automation apps and here is a breakdown of what you can do.  

## Open
On-the-agenda view
`agenda://x-callback-url/on-the-agenda
`

Open the Today overview
`agenda://x-callback-url/today
`

Open a project
`agenda://x-callback-url/open-project?title=\[project title]
`

Open a note
`agenda://x-callback-url/open-note?title=\[note title]
`

## Create
Create a new note
`agenda://x-callback-url/create-note?project-title=\[project name]&title=\[note title]&text=\[note text]
`

Append to existing note
`agenda://x-callback-url/append-to-note?title=\[note title]&text=\[text]
`

![](https://gr36.com/img/2018-10-30-agenda-screenshots.png)

## Optional extras
Add in extras to the end of the url if you need some more control. These are not mandatory.

On the agenda
`&on-the-agenda=\[true or false]
`

Specific date
`&date=\[year]-\[month]-\[day]
`

Start and/or end dates
`&start-date=yesterday&end-date=tomorrow
`

### Example 1
`agenda://x-callback-url/create-note?project-title=My%20Project&title=New%20Note&text=Hello%20World&on-the-agenda=true&date=2018-03-12
`

### Example 2
`agenda://x-callback-url/create-note?project-title=Blogposts&title=New%20Post29&text=Hello%20World&on-the-agenda=false&start-date=yesterday&end-date=tomorrow`
