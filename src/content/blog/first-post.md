---
title: 'First post'
description: 'Lets get it started'
pubDate: 'Jan 08 2024'
heroImage: '/blog-placeholder-3.jpg'
---

# Creating my new net home

Start Stream of conciousness - I'm not going to slow down here, just go:

I've recently been swimming in a sea of distraction, borderline depression, and I've got a spark to start fresh. I am fired up and want to 
engage with the world around me a little bit more. Doing so on the internet is not a solution, but I think this is more of an attempt to stop 
blocking myself from engagement, and start a channel of some sort.

Typically - my workflow looks like this:

* Get inspired and super excited about an idea
* Do some prototyping or start writing code, and then realize I jumped the ship. The idea is not good, or maybe I need to design it first.
* Go start designing, creating a backlog, or making design concepts.
* Lose steam, stop working on it.

So, instead I want to start small. 
I want to get my blog running first, as a place to hold this journey. So its 8:47 AM on a Monday now, and I have some time to kill before my next meeting.
How long will it actually take to get this published to the web? Let's see...

## Things to do

* Get Astro setup locally w/ a template
* Make only critical modifications to make "work" for me.
* Add this post as first post.
* Get hosted on existing DigitalOcean server on root domain.
* Put existing content at old.mikescottbowen.com or something similar.

From there I can tweak, enhance, and start my journey.
 
## Future Things to do

* Talk about xbiking and building my commuter bike
* Talk about Longmont
* Talk about Salesforce Architecture and Development
* Talk about side projects

## Large Goals

* Engage with my community more
* Read more books
* Write and express more (and actually complete small things)

Ahh, what a nice post, sort of a brain dump to kick this off. Happy 2024! 

Mike

# Appendix / Progress Update

## Update 9:09 AM

* Ok, I've got Astro installed, stripped minimal boilerplate, and now its got my first blog post in it.
* Let's get logged into (and dust off) my webserver.

## Update 9:58 AM - We're Live!

* Succesfully logged into my VM on digital ocean
* Pushed everything to git
* Pulled the repo to my local webserver
* Did some googling to remember where my Apache2 configurations are stored, and modified the virtual host config
* Restarted Apache
* Now we're live!

So lets go onward to better things.

* Update server to not be on Ubuntu 12.04. This will involve re-deploying mikescottbowen.com and plainfieldsignsinc.com (my parents business website)
* Make sure we have a CI pipeline that is easy to use, ideally pushing to git will just auto pull changes and run builds on the server
* Update the blog to look more "me"
* Keep writing content!
