---
title: Ulysses Automation Tip - When Inspiration Hits
date: 2016-12-27
tags: howto, automation
---
I have been writing in Markdown for a few years now, using a variety of apps to create and publish posts to my personal blog, Coolsmartphone and a few other Wordpress blogs. Having recently switched all of my work to the Ulysses app I’ve been trying to automate as much of my workflow as possible: and heres a nifty trick to jot some notes when you get an idea.

I take no credit for this, the whole idea and process came from the Ulysses team themselves, they have some [great ideas on their blog][1] if you want to delve in deep. First things first, the Ulysses app might [seem very expensive][2], but if you’re serious about writing, previewing and publishing direct from your devices then seriously think about the investment.

![][image-1]
￼
## x-callback-url
The Ulysses app supports x-callback-url which will allow some apps apps to trigger actions inside Ulysses. So going to the ulysses://x-callback-url/ and adding on an action, with the Ulysses app installed will automate several things that may require several taps. The following actions are supported.
•	new-sheet to create a new sheet
•	insert to add text to an existing sheet
•	attach to create a note attachment for an existing sheet
•	new-group to create a new group
•	open to open a particular sheet or group
•	open-group to open a group with a particular name
•	open-all to open the All section of your library
•	open-recent to open Last 7 Days
•	open-favorites to open your Ulysses Favourites

So in this example I am going to use a url to open a new sheet in an ideas tab, so you can jot down ideas as soon as inspiration strikes. I often jot down things in the notes app, or try and remember things, but this workflow has allowed me to take a few notes of ideas straight in the app. I can then finish them on which ever device is easiest. The URL to create a new note is:

`ulysses://x-callback-url/new-sheet?group=Ideas`

So what App to use? Well my personal taste is the Workflow app. It can be used for all sorts of iOS automation, and I’ve published quite a few ideas for you to try out already. Workflow will cost [you a grand total of £2.29 from the App Store][3], and will come in handy more times than you think.

![][image-2]
￼
Can I presume you have the apps already? If you want to cheat, just go [here and download the workflow][4] I have set up for you. Just tap ‘get workflow’ and you can save it straight into the app, but if you want to learn and set it up yourself. Follow the instructions below [courtesy of the Ulysses team][5].

•	Open Workflow.
•	Tap the Plus button top right to add a new workflow.
•	Tap “Actions” bottom left to select the actions that belong to the workflow.
•	From the list of actions, select “URL” and swipe right to add it to your workflow.
•	Insert the x-callback-url in the designated field.
•	Go back to Actions, select “Open URLs” and also add it to your workflow via swiping right.
•	Now tap the gear to name the new workflow and give it a proper icon.
￼
![][image-3]

You can also do the same thing is other apps such as [Launch Centre Pro][6], which is another great app for automating things that otherwise might take several seconds. Even at the slightly more expensive £3.99 app like these are well worth the investment if you’re serious about making things easier.
Let me know how you get on.

[1]:	https://ulyssesapp.com/blog/category/tips-tricks "some great ideas on their blog"
[2]:	https://ulyssesapp.com/#top "Ulysses app might seem very expensive"
[3]:	https://itunes.apple.com/gb/app/workflow-powerful-automation/id915249334?mt=8&ign-mpt=uo%3D4 "you a grand total of £2.29 from the App Store"
[4]:	https://workflow.is/workflows/aed4f6fbc4e94e13b5f28105f6722929 "here and download the workflow"
[5]:	https://ulyssesapp.com/blog/2016/04/introduction-x-callback-support/ "courtesy of the Ulysses team"
[6]:	https://contrast.co/launch-center-pro/ "Launch Centre Pro"

[image-1]:	https://cdn-images-1.medium.com/max/800/1*gQhbgpAUzRsfP3ODZhpqEA.jpeg
[image-2]:	https://cdn-images-1.medium.com/max/800/1*yNYP-Wg-ErgwTkeKO0FI1Q.png
[image-3]:	https://cdn-images-1.medium.com/max/800/1*prc7oyZCAkRNxYkxej5jEA.png
