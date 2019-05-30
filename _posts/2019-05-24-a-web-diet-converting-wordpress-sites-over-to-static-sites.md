---
layout: post
title: 'A Web Diet: Converting Wordpress Sites Over to Static Sites'
published: true
author: admin
comments: true
date: 2017-08-07 01:08:42
tags: [ ]
categories:
    - bits-and-bytes
    - domains
    - jmc
    - wordpress
permalink: >
    /2017/08/a-web-diet-converting-wordpress-sites-over-to-static-sites
image:
    feature: 32698135126_af7d516591_z.jpg
---
Over the years, my main course web project, PR Pubs, has became one sprawling beast. For the most part, people know [prpubs.us][1] as the homepage for the course, but I haven&#8217;t actively used that space for a few semesters. Thus, in May I made it one of my summer goals to rework prpubs.us in such a way that both narrates and preserves the history of the course and the space. The story of Pubs is an epic one with many twists and turns. Once upon a time, it started as a blog feed, morphed into a full open course, vacationed for a summer on the Jekyll CMS, and is now more integrated with Canvas, our LMS. Nothing really captures this story well and for good reason: I&#8217;ve tried counting and I believe it&#8217;s existed in eight separate places since 2014. In fact, out of all the spaces, my own personal blog is probably the best representation of the evolution:

  * [Follow Along With My Students&#8217; Work This Semester &#8211; January 27, 2014][2]
  * [PR Pubs Goes Online &#8211; January 13, 2015][3]
  * [Sticking a Fork in the LMS &#8211; May 16, 2016][4]
  * [The LMS has landed. &#8211; July 26, 2016][5]
  * [A Page For Courses &#8211; August 9, 2016][6]

I got interested in archiving a bit more [while visiting Middlebury College][7] last Fall where they&#8217;ve started a project out of their library to preserve student web work at the request of students. I should also mention that Kin Lane has been [a major inspiration][8] in helping me see the benefit of static sites. The point being that I&#8217;ve known good and well that no CMS is in for the long term. I&#8217;m a data pack rat so I&#8217;m always thinking about the long term.

At the heart of every course site has been the blog feed powered by the FeedWordPress plugin. Students are writing between 250-500 total blog posts per class per semester. I&#8217;ve systematized the process of preparing for the next batch of PR Pubsters. Every semester, I clone a clean version of my syndication hub which is already preloaded with theme, plugins, and custom code that I need to make it work. Over the past couple years, I&#8217;ve probably done this a dozen or so times across various courses and thus end up with a ton of WordPress instances.



Eventually, the semester ends and these 250-500mb spaces of content become dormant. There are tasks that I&#8217;ve done in the past to close a course site which basically involves unsubscribing to student feeds. But recently I&#8217;ve decided that for better preservation purposes, I would rather have a fully static HTML version of each course site. In a lot of ways, it feels like I&#8217;m putting it sites on a diet. &#8220;Why consume all of those data-dense databases?! Stick your macronutrients: HTML, CSS, and JS! Get rid of your addiction to Cigawordpress!&#8221;

### What are the upsides to doing this?

  1. You know no longer need WordPress or any other CMS to be the engine of the site. The biggest benefit is that you are less vulnerable to becoming infected through an out-of-date theme or plugin. If you aren&#8217;t actively updating the site, you are making yourself susceptible to a lot of mean people on the web.
  2. You can host it on any type of web server.
  3. You can even just keep it locally on your computer and access it via your web browser.
  4. Because of it&#8217;s portability, it&#8217;s much easier to share a static site as an open education resource (OER). You could even host them on Github allowing people to create forks of the site if they so choose.

Jim Groom turned me on to a tool called SiteSucker [a few months back][9] because that guy is always thinking a step ahead of me&#8230; SiteSucker does exactly what I laid out earlier. And Jim lays out a strong argument:

> I don’t pay for that many applications, but this is one that was very much worth the $5 for me. I can see more than a few uses for my own sites, not to mention the many others I help support. And to reinforce that point, right after I finished sucking this site, a faculty member submitted a support ticket asking the best way to archive a specific moment of a site so that they could compare it with future iterations. One option is cloning a site in Installatron on Reclaim Hosting, but that requires a dynamic database for a static copy, why not just _suck that site_? And while cloning a site using Installatron is cheaper and easier given it’s built into Reclaim offerings, it’s not all that sustainable for us or them. All those database driven sites need to be updated, maintained, and protected from hackers and spam.

Side note: Isn&#8217;t it always a let down when you are trying to write a blog post and you realize that someone has already made your argument and in a much more succinct fashion I might add? That Groom! But, nevertheless, I&#8217;ll continue on in hopes of imparting a little bit more wisdom&#8230;

[Sitesucker][10] grabs your site contents and converts it into HTML, CSS, and JS. You can also set how many links deep you want to pull content. For me, I wanted to grab all my students blog posts, but I didn&#8217;t necessarily want the links they were referencing in their blog posts, so I went three levels deep (front page, pages, blog posts).

### What are the downsides?

  1. Because it is a _static_ site, it can no longer make _dynamic_ calls. Dynamic calls are when pieces of the web resource are being constructed when the URL is first called. This includes comments, searches, and other organization features like categories and tags that are native to WordPress. Now SiteSucker will generate a copy of these dynamic calls and turn them into static, but after that they will cease to function. None of the content disappears but it can&#8217;t be regenerated, so no new comments. This isn&#8217;t a big deal for me considering the sites are completely dormant, but it does sting a bit to lose search functionality.
  2. You need to understand basic HTML and CSS to make any significant edits to the site after it&#8217;s in it&#8217;s static state. Remember, you longer have access to the nifty WordPress WYSIWIG editor. This is where the OER argument gets tricky. Yes, it&#8217;s more portable, but potentially less editable depending on the user&#8217;s knowledge.

[John Stewart][11] was kind enough to test it for me with prpubs.us and it worked like a charm. I then went and grabbed static versions of the other course sites followed by hitting that scary &#8220;delete&#8221; button in Installatron which made the WordPress instances go away.

Last, I redesigned the prpubs.us front page to better tell the historical narrative of the course. There you can find images of past versions, full information on the technologies that powered each, and links to the archived versions.

[device link=&#8221;prpubs.us&#8221; type=&#8221;imac&#8221; color=&#8221;&#8221; orientation=&#8221;portrait&#8221; hide=&#8221;&#8221; width=&#8221;&#8221; scroll=&#8221;true&#8221;][/device]

Hopefully this is a much more helpful resource for visitors and student alike. Either way, I feel like the state of the health PR Pubs is at an all-time high. Here&#8217;s to surviving.

 [1]: http://prpubs.us
 [2]: https://backup.adamcroom.com/2014/01/follow-along-with-my-students-work-this-semester/
 [3]: https://backup.adamcroom.com/2015/01/pr-pubs-goes-online/
 [4]: https://backup.adamcroom.com/2016/05/sticking-a-fork-in-the-lms/
 [5]: https://backup.adamcroom.com/2016/07/the-lms-has-landed/
 [6]: https://backup.adamcroom.com/2016/08/a-page-for-courses/
 [7]: https://backup.adamcroom.com/2016/09/its-the-middleburys/
 [8]: http://kinlane.com/2016/09/06/keeping-things-static-with-my-public-presence-to-reduce-security-friction/
 [9]: http://bavatuesdays.com/get-sitesucker-sucker/
 [10]: http://ricks-apps.com/osx/sitesucker/
 [11]: http://johnastewart.org