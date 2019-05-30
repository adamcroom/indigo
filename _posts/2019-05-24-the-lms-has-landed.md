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

It was [announced][1] in late Spring that OU was moving from Design2Learn to Canvas as its primary learning management system. Since then, all forces in our Center have been pointed towards all things LMS. Being that Canvas is a much bigger, nastier beast than our sweet, innocent Domain of One&#8217;s Own initiative that I&#8217;ve been working on for the last couple of years, the reserves have been brought in.

Given that the Digital Learning has been a bit nimble and creative in [making sure OU Create students felt supported][2] and [honored][3] for their work, I was asked to lead the student side of Canvas as well. I was also asked to design the landing page for the Canvas portal which is now live at [canvas.ou.edu][4].



This gave me an opportunity to infiltrate some of my &#8220;domain knowledge&#8221; (get it?!) into Canvas, which I appreciated. So I created my own little personal challenge set out to build my own sort of a [SPLOT][5] (Smallest Possible L\___ O\___ T\___). Behold! The Smallest Possible Landing Page! Also known as SPLP to those who like to spit.

There were a few reasons for wanting to attack from this direction: 1.) I wanted it to be pure HTML so it would be super small, fast, and could run on any server since it didn&#8217;t require a database 2.) I was told this thing would basically only exist for a year so it didn&#8217;t make sense to build out much more than a page or two and 3.) it&#8217;s in many ways a metaphor for how I feel about domains versus LMSs. One is portable and light and accessible and the other is big, bulky, scary, and behind a login page. Why not give people one last small bite of pizazz, color (and hope) before they enter the santizied white walls of Canvas. Seriously, Canvas is _nice_ and clean but an accent wall here or there wouldn&#8217;t hurt anybody! Sometimes I feel a bit like I&#8217;m stuck in [the Construct][6] from the Matrix.



Back in March, [Alan Levine][7] had posted a link to some HTML5 templates on our little IndieEdTech Slack Channel which you can check out at [html5up.net][8]. I landed on one titled Alpha:



This template would actually likely work for a fully functioning website as they have some subpage templates including a contact page but I opted to simply use the front page. A side note: although it&#8217;s been released on HTML5, it was built by a a couple, Cherry and AJ, who have released over 800 HTML5 templates under a CC license on [their own website][9]. Kudos to them for sharing such a vast resource for folks like me!

Anyways, my main goal was get users to the login at [oklahoma.instructure.com][10] as quickly as possible while also sharing a bit of helpful hints on where to find resources and help. I placed two logins above the fold and a big ol&#8217; link to the [CTE resource site][1] to learn more about the initiative. Again, knowing that this site would be nuked in a year I didn&#8217;t want to build out a lot of native content and opted to rather push users out the content in which other teams have already built out on the [Center for Teaching Excellence website][1], which presumably isn&#8217;t going anywhere for some time.



I gave four call outs to the following: faculty adoption, Canvas video tutorials, the mobile apps, and the Canvas guides. I found a neat little tool called [appurl.io][11] which will detect the device and then send the user to the appropriate URL. All desktops will be sent to the iTunes webpage, while Apple devices will be sent directly to the native AppStore and Android devices will be sent to Google Play.

There were a couple places where the content was more text-based. Knowing that Canvas is really good about making the content, such as their guides, CC licensed I poked around their sites for some text that might talk about the platform itself. I was surprised at how focused their page is on decision makers more than anything else. Here&#8217;s the bullets of their [Higher Ed LMS][12] page:

  * How to choose an LMS
  * Will it get used?
  * Adoptable
  * Adaptable
  * Reliable
  * The Canvas experience

Not much I can sell there on the top bullets and the Canvas experience simply pointed to a few case studies (there are a few nuggets in the [Research][13] page though). Even more frustrating was the lack of student experience language. Even their [videos][14] speak more about the instructor experience than the student. As a Canvas newbie, I don&#8217;t have a lot to go off of on exactly what students will exactly like about Canvas, so I scrapped talking about features and simply went with getting help and the onboarding (logging in, downloading the app, answering questions, etc.).

I spent an extra amount of time really honing in the responsiveness and speed. I blogged a earlier in the summer how I&#8217;ve [became a little obsessed][15] with speed and websites. I really wanted to focus on the user who is coming here on their mobile device with a slower data plan. That meant optimizing images as much as possible, looking at the site from every angle on several devices, and tweaking the CSS little by little.

Last, here&#8217;s the speed test:



Boom! A 99! And this one doesn&#8217;t even have grade inflation! I haven&#8217;t felt this good since freshman year Sociology.

My only point dock was on a couple of Google JS files that I can&#8217;t fix for them. So I&#8217;ll take it. It&#8217;s load time is a little over half a second and is faster than 96% of the other sites.  Very cool stats. One thing that really helped was adding resource caching to the .htaccess so you don&#8217;t have to reload resources everything you don&#8217;t them. That code snippet looks like this:

## EXPIRES CACHING ##
&lt;IfModule mod_expires.c&gt;
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
&lt;/IfModule&gt;
## EXPIRES CACHING ##

As a way to gauge it&#8217;s performance, I ran it across some other highly trafficked OU websites and this little flat file is 5-10x faster than most anything else. Mission SPLP Accomplished! That&#8217;s one small site for man that gives you entrance into one GIANT LMS.

I&#8217;ve also released the code in a [Github repository][16] in the event that it is valuable to any other institutions. I would love to hear any feedback on either the site or how others have approached informing students!

Featured image: a flickr photo shared by Apollo Image Gallery under a Public Domain Work Mark 1.0 Creative Commons license 

 [1]: http://www.ou.edu/content/cte/initiatives/canvas-transition.html
 [2]: https://backup.adamcroom.com/2016/02/integrated-customer-support-and-slack/
 [3]: https://backup.adamcroom.com/2016/04/recapping-the-ou-creaties/
 [4]: http://canvas.ou.edu
 [5]: http://splot.ca
 [6]: https://www.youtube.com/watch?v=AGZiLMGdCE0
 [7]: http://twitter.com/cogdog
 [8]: https://html5up.net
 [9]: https://templated.co
 [10]: http://oklahoma.instructure.com
 [11]: http://www.appurl.io
 [12]: https://www.canvaslms.com/higher-education/
 [13]: https://www.canvaslms.com/research-education?higher-education
 [14]: https://www.youtube.com/user/CanvasLMS
 [15]: https://backup.adamcroom.com/2016/05/sticking-a-fork-in-the-lms/
 [16]: https://github.com/oudiglearn/canvas_splash
