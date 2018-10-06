---
title: "In iOS11 Apple Attempts to Make Messages Even More Secure"
bigimg: /img/2017-10-28-ios11-iMessage.jpeg
date: 2017-06-12
---

Since 2012, for many iOS users iMessage or Messages is the glue that keeps them using the platform. Apple’s messaging platform makes sending and receiving messages on any of your devices a breeze. It may have stickers, and now Apple Pay payments, but encryption has always been one of its biggest selling points. Starting with iOS11 Messages.app is going to be a whole lot more secure thanks to iCloud.

iMessage has always featured “secure end-to-end encryption” that in theory stops anyone reading your messages bar the parties involved in the discussion. That may indeed be the case, but unfortunately if iCloud is enabled on your device this means Apple. or security authorise that force Apple, [have access to your device back ups][1]. Thankfully that is all about to change with iOS11.

During the WWDC keynote, Craig Federighi outlined that, starting with iOS11, iCloud will have the facility to sync all of your messages to all of your devices. The option issuer optional and was very much posed as an improvement to the user experience. However this small improvement runs much deeper, and will in fact improve security considerably. 

[https://vimeo.com/220770851][2]

Whilst speaking at John Gruber’s Daring Fireball live at WWDC, Federighi unveiled Apple have developed a way to sync encryption keys to all of your devices without Apple involvement. Meaning Apple does not have access to your messages at any point in the process, so no more compromised iCloud backups. 

> "And so, even if they store information in the cloud, it's encrypted with keys that Apple doesn't have. And so [users] can put things in the cloud, they can pull stuff down from the cloud, so the cloud still serves as a conduit—and even ultimately kind of a backup for them—but only they can read it." - Craig Federighi

It must be said that no one is entirely sure how Apple has managed to pull off such a feat. Cryptography [researcher Kenn White is on of those scratching his head][3]. He posed the question that “If recovery from a forgotten iCloud password is possible *without access* to keys on a device's Secure Enclave, it's not truly e2e”. So should iCloud recovery be possible Apple still have access to your encryption keys in some way.

In that instance Message threads would still remain encrypted, but would be decryptable by other parties other than those involved in the conversation. Apple have not released any further information at present so things are a little up the air, and may change as iOS11 develops. Without further info it is impossible to say if iCloud syncing is the saving grace that privacy conscious individuals have been waiting for. It appears to be a massive step in the right direction though. 

[1]:	https://motherboard.vice.com/en_us/article/psa-apple-can-still-see-your-imessages-if-you-enable-icloud
[2]:	https://vimeo.com/220770851
[3]:	https://motherboard.vice.com/en_us/article/apple-is-trying-to-make-your-imessages-even-more-private