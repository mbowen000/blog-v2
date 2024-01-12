---
title: 'A signshop website'
description: 'Chronicles my adventures with building a website for my parents small business'
pubDate: 'Jan 08 2024'
heroImage: '/blog-placeholder-3.jpg'
---

## Simple is always better - Building a Small Business Website

### Intro
Over the years, I've always been seen as the "tech guru" around my family. Making websites became a passion when I picked up a PHP web development book
from Barnes and Noble in 8th grade, and when my parents sign shop needed a website, I was happy to take on the job. What resulted was a great exploration into writing my own CMS, frontend for displaying images in a lightbox, and a navigation structure that was very early 2000s.

This site is still hosted on the same server as this blog, at <a href="http://plainfieldsigns.net">plainfieldsigns.net</a>. I designed the (very dated) template, and built a PHP backend for the site using codeignitor that allows my parents to upload content. So basically I wrote my own mini "CMS" for photo uploads. Here's a screenshot:

![A signshop website](/plainfieldsigns-old.jpg)

Looking at this 15 years later is painful and we're in a different place with technology:

* This homegrown CMS "app" for photo uploads is terrible.
* I used JQuery and lightbox code to display the images.
* The taxonomy and navigation is hardcoded
* I don't think my parents have uploaded any content in 10+ years.

(Todo in the future: Do a breakdown / analysis of this existing software and explore how I built it and what I could have done better as a young grasshopper!)

It's time to do this the modern way and make this useful again. Hopefully a thing that I can do that will connect my parents and I even though we live ~1000 mi apart. (And not annoy them or me in the process) 😊 

## New And Improved

The goal should be to make a refreshed design for this site that allows easy content manipulation, shows basic contact information.

**Requirements**

* Powered by a CMS (Headless for fun) - Posts should just be sign images with optional text content. (Could be fun for mom and dad to write some details about the job or the process of making the sign)
* Static content should be easily hosted
* Template could be : https://astro-strata.vercel.app/
* CMS Could be Sanity / but should consider others that are even easier. https://www.sanity.io/guides/sanity-astro-blog


**Next steps:**

* Outline the structure ✅
* list changes that are needed to the chosen template ✅
* POC and hook up CMS with Astro ✅
* Verify that its a) easy to use b) easy to maintain and deploy ✅
* Build the thing and port some content locally ✅
* Deploy it! ✅
* Show my folks how to use the thing to add content


### Update 1/12/2024

I've made some progress. After getting some input from Mom, I decided to build my own template from scratch using Tailwind CSS components. The design is still mostly boilerplate tailwind but we'll spruce that up soon. As of now, I would consider the POC complete that demonstrates:

* Content can be managed in Sanity Studio by my Mom and Dad. I have that running on Sanity production.
* The Frontend application is deployed to a free app service on Digital Ocean, my typical hosting platform. The bonus here is that I can move these static apps to free tier apps and then sunset my droplet / VM and save like $10 per month! 
* Deploying content on Sanity publishes a webhook that automatically rebuilds the frontend app, updating the content from Sanity (any new sign photos will be pushed). **This could potentially be a separate blog article on how to set up.**

```
<script>Script Source</script>
```

Here's a screenshot of what it looks like now (notice the photos I used are just random family photo uploads):

![Plainfield Signs New Site](/plainfieldsigns-new-draft.jpg)

### Summary and other challenges

I have learned some things about static sites, Astro, headless CMS and other new technologies by getting hands on here. It's been tricky to wrap my head around the limitations of using a static site. For example, with a static site I have to rebuild the site in order for new content published in the CMS to appear. 

Another challenge is dynamic behavior. I would like to have a contact form on the site that sends an email (via a service like sendgrid) to my parents gmail address. However, as a static site hosted without a backend, this is proving difficult. I am able to create a serverless function with Digital Ocean, however I cannot find a way to authenticate to that service from the static site. I do not want to expose a function that sends emails to my parents without some kind of security / obfuscation, as I planned on having a captcha on the form, but leaving the function exposed to the internet generally would be a no-go. 

This has really turned into a "serverless" adventure and it's pushed me to learn and and utilize a new set of technology and tools. Its definitely a mind-shift to think about accomplishing things without a full webserver backed "app". 

**Next Steps**

* Finalize the template
  * Finalize the design of the main content - hopefully make it look a little more bespoke and not so templated.
* Port over existing content
  * Determine if there are ways to bulk create posts in Sanity for each of the existing images (there has to be!)
* Get some new photos taken for the main splash and featured gallery images.
* Implement the contact form - potentially just using some 3rd party integration that uses iframe or something.
* Add other basic pages
* Switch over the DNS to the new site
* (From Above) - Train the users (mom and dad).