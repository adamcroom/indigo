---
layout: post
title: "The LMS has landed."
date: 2016-07-26 11:07:23
projects: true
headerImage: false
tag:
    - indie-edtech
    - music
category: project
permalink: /2016/07/the-lms-has-landed
author: adamcroom
published: true
---

It was [announced](http://www.ou.edu/content/cte/initiatives/canvas-transition.html) in late Spring that OU was moving from Design2Learn to Canvas as its primary learning management system. Since then, all forces in our Center have been pointed towards all things LMS. Being that Canvas is a much bigger, nastier beast than our sweet, innocent Domain of One's Own initiative that I've been working on for the last couple of years, the reserves have been brought in.

Given that the Digital Learning has been a bit nimble and creative in [making sure OU Create students felt supported](http://backup.adamcroom.com/2016/02/integrated-customer-support-and-slack/) and [honored](http://backup.adamcroom.com/2016/04/recapping-the-ou-creaties/) for their work, I was asked to lead the student side of Canvas as well. I was also asked to design the landing page for the Canvas portal which is now live at [canvas.ou.edu](http://canvas.ou.edu).

![flatcanvasresponsive.jpg](http://backup.adamcroom.com/wp-content/uploads/2016/07/flatcanvasresponsive.jpg)

This gave me an opportunity to infiltrate some of my "domain knowledge" (get it?!) into Canvas, which I appreciated. So I created my own little personal challenge set out to build my own sort of a [SPLOT](http://splot.ca) (Smallest Possible L___ O___ T___). Behold! The Smallest Possible Landing Page! Also known as SPLP to those who like to spit.

There were a few reasons for wanting to attack from this direction: 1.) I wanted it to be pure HTML so it would be super small, fast, and could run on any server since it didn't require a database 2.) I was told this thing would basically only exist for a year so it didn't make sense to build out much more than a page or two and 3.) it's in many ways a metaphor for how I feel about domains versus LMSs. One is portable and light and accessible and the other is big, bulky, scary, and behind a login page. Why not give people one last small bite of pizazz, color (and hope) before they enter the santizied white walls of Canvas. Seriously, Canvas is _nice_ and clean but an accent wall here or there wouldn't hurt anybody! Sometimes I feel a bit like I'm stuck in [the Construct](https://www.youtube.com/watch?v=AGZiLMGdCE0) from the Matrix.

![31g6rA.gif](http://backup.adamcroom.com/wp-content/uploads/2016/07/31g6rA.gif)

Back in March, [Alan Levine](http://twitter.com/cogdog) had posted a link to some HTML5 templates on our little IndieEdTech Slack Channel which you can check out at [html5up.net](https://html5up.net). I landed on one titled Alpha:

![Screen Shot 2016-07-26 at 9.46.44 AM.png](http://backup.adamcroom.com/wp-content/uploads/2016/07/Screen-Shot-2016-07-26-at-9.46.44-AM.png)

This template would actually likely work for a fully functioning website as they have some subpage templates including a contact page but I opted to simply use the front page. A side note: although it's been released on HTML5, it was built by a a couple, Cherry and AJ, who have released over 800 HTML5 templates under a CC license on [their own website](https://templated.co). Kudos to them for sharing such a vast resource for folks like me!

Anyways, my main goal was get users to the login at [oklahoma.instructure.com](http://oklahoma.instructure.com) as quickly as possible while also sharing a bit of helpful hints on where to find resources and help. I placed two logins above the fold and a big ol' link to the [CTE resource site](http://www.ou.edu/content/cte/initiatives/canvas-transition.html) to learn more about the initiative. Again, knowing that this site would be nuked in a year I didn't want to build out a lot of native content and opted to rather push users out the content in which other teams have already built out on the [Center for Teaching Excellence website](http://www.ou.edu/content/cte/initiatives/canvas-transition.html), which presumably isn't going anywhere for some time.

![Screen Shot 2016-07-26 at 9.54.18 AM.png](http://backup.adamcroom.com/wp-content/uploads/2016/07/Screen-Shot-2016-07-26-at-9.54.18-AM.png)

I gave four call outs to the following: faculty adoption, Canvas video tutorials, the mobile apps, and the Canvas guides. I found a neat little tool called [appurl.io](http://www.appurl.io) which will detect the device and then send the user to the appropriate URL. All desktops will be sent to the iTunes webpage, while Apple devices will be sent directly to the native AppStore and Android devices will be sent to Google Play.

There were a couple places where the content was more text-based. Knowing that Canvas is really good about making the content, such as their guides, CC licensed I poked around their sites for some text that might talk about the platform itself. I was surprised at how focused their page is on decision makers more than anything else. Here's the bullets of their [Higher Ed LMS](https://www.canvaslms.com/higher-education/) page:

*   How to choose an LMS
*   Will it get used?
*   Adoptable
*   Adaptable
*   Reliable
*   The Canvas experience

Not much I can sell there on the top bullets and the Canvas experience simply pointed to a few case studies (there are a few nuggets in the [Research](https://www.canvaslms.com/research-education?higher-education) page though). Even more frustrating was the lack of student experience language. Even their [videos](https://www.youtube.com/user/CanvasLMS) speak more about the instructor experience than the student. As a Canvas newbie, I don't have a lot to go off of on exactly what students will exactly like about Canvas, so I scrapped talking about features and simply went with getting help and the onboarding (logging in, downloading the app, answering questions, etc.).

I spent an extra amount of time really honing in the responsiveness and speed. I blogged a earlier in the summer how I've [became a little obsessed](http://backup.adamcroom.com/2016/05/sticking-a-fork-in-the-lms/) with speed and websites. I really wanted to focus on the user who is coming here on their mobile device with a slower data plan. That meant optimizing images as much as possible, looking at the site from every angle on several devices, and tweaking the CSS little by little.

Last, here's the speed test:

![Screen Shot 2016-07-22 at 12.54.52 PM.png](http://backup.adamcroom.com/wp-content/uploads/2016/07/Screen-Shot-2016-07-22-at-12.54.52-PM.png)

Boom! A 99! And this one doesn't even have grade inflation! I haven't felt this good since freshman year Sociology.

My only point dock was on a couple of Google JS files that I can't fix for them. So I'll take it. It's load time is a little over half a second and is faster than 96% of the other sites.  Very cool stats. One thing that really helped was adding resource caching to the .htaccess so you don't have to reload resources everything you don't them. That code snippet looks like this:

<code>## EXPIRES CACHING ##
<IfModule mod_expires.c>
ExpiresActive On
ExpiresByType image/jpg "access plus 14 days”
ExpiresByType image/jpeg "access plus 14 days”
ExpiresByType image/gif "access plus 14 days”
ExpiresByType image/png "access plus 14 days”
ExpiresByType text/css "access plus 1 day”
ExpiresByType application/pdf "access plus 1 month"
ExpiresByType text/x-javascript "access plus 1 month"
ExpiresByType image/x-icon "access plus 1 year"
ExpiresDefault "access plus 2 days"
</IfModule>
## EXPIRES CACHING ##</code>

As a way to gauge it's performance, I ran it across some other highly trafficked OU websites and this little flat file is 5-10x faster than most anything else. Mission SPLP Accomplished! That's one small site for man that gives you entrance into one GIANT LMS.

I've also released the code in a [Github repository](https://github.com/oudiglearn/canvas_splash) in the event that it is valuable to any other institutions. I would love to hear any feedback on either the site or how others have approached informing students!

<small>Featured image: a [flickr photo](https://flickr.com/photos/projectapolloarchive/21445908434 "AS11-40-5962") shared by [Apollo Image Gallery](https://flickr.com/people/projectapolloarchive) under a [Public Domain Work Mark 1.0 Creative Commons](https://creativecommons.org/publicdomain/mark/1.0/) license</small>
