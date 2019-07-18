---
layout: post
title: "Three Flavors of Networked Blogging with Wordpress"
date: 2015-12-15 08:12:41
projects: true
headerImage: false
tag:
    - domains
category: project
permalink: /2015/12/three-flavors-of-networked-blogging-with-wordpress
author: adamcroom
published: true
---

---
layout: post
title: Three Flavors of Networked Blogging with Wordpress
published: true
author: admin
comments: true
date: 2015-12-15 08:12:41
tags:
    - Alan Levine
    - Amy Collier
    - DS106
    - FeedWordPress
    - Middlebury
    - wordpress
    - Wordpress MU
categories:
    - domains
    - wordpress
permalink: /2015/12/three-flavors-of-networked-blogging-with-wordpress
image:
    feature: A63C409DD4.jpg
---
I&#8217;ve been helping with the launch of [MiddCreate][1], a domains project at [Middlebury][2], led by [Amy Collier][3]. One of their faculty members was interested in a multisite setup for her class, and while that&#8217;s a great approach, I wanted to offer the Middlebury folks a broader look at options for networked blogging with a particular focus on different models that WordPress affords.

## Networked, distributed sites

This is the approach that I use for my [PR Pubs][4] course, which was popularized by [Alan Levine][5]&nbsp;/&nbsp;[DS106][6]. Essentially, faculty set up a course site and utilized it&#8217;s blog function to syndicate student work. This is arguably the broadest approach and lends itself well to student agency. This is because the model depends on student&#8217;s sites to have RSS feeds to process the syndication, so, technically, students are able to use any platform that produces an RSS feed. That said, it is also more arduous to manage at both a student and faculty level (though I would argue this may be a good thing depending on your objectives). If you are taking a portfolio building approach to your class, I highly recommend this model.

The how: If you are at an institution that has a [Domain of One&#8217;s Own][7] initiative (we have [OU Create][8]) and gives students access to tools like CPanel and Installatron, students have multiple applications that they can choose from (such as [WordPress][9] and [Known][10]). I have setup a WordPress instance to run the course site and installed [FeedWordPress][11] which is the real engine of the tool. I won&#8217;t go into this method too in-depth because Alan [wrote a series in 2014][12] which is arguably the most comprehensive tutorial of the plugin (HIGHLY recommended). But for those new to the game,&nbsp;[FeedWordPress][11] allows you to subscribe to any of the Atom and RSS feeds that a site generates. If the student is using WordPress (as well as [Blogger][13]), you will see multiple options for RSS feeds pop up. That&#8217;s because there are feeds for the blogs as well as the comments (which can be beneficial if you want to track comments as well).



Once you have subscribed to the RSS, you can look under the &#8220;Feeds & Updates&#8221; menu item and you can decide whether you want the course site to manually check for updates (known as a cron job) or automatically check for updates. I have mine set to check for updates automatically once an hour. One other feature that you might want to take a look at is where the permalinks point. You can either have it point to your local copy or to the students website. I prefer to point to the students site to really promote the idea of these networked, distributed sites, but occasionally a student site disappears and I appreciate the ability to point to the local copy.

There is also an [Feedwordpress Advanced Filters plugin][14] that can be handy. I use it to locally store the images that syndicate. That way, in the event that the student site goes down, I have a local copy cached.



When you&#8217;ve finally subscribed to all of the student sites, your FeedWordPress dashboard will look something like this, showing the feeds, their address, and the last time the site was scanned for new posts:



## WordPress Multi-Site

So this is&nbsp;a new approach&nbsp;that I&#8217;m playing with. Tim Owens [wrote a great series][15] on WordPress multi-site and the advantages it brings. Multi-site is pretty self explanatory: One WordPress user is a super admin to multi sites. Most campus-wide blog solutions are, indeed, simply one installation of a WordPress multi-site. Users can sign up to create a WordPress website but do not manage the installation or its features. This means that all updates to WordPress, themes, and plugins happen at a Super Admin level.

What I wanted to look at was can you use WordPress Multi-Site to replicate the same functionality as distributed site syndication, but lowering the bar to&nbsp;entry for creating and maintaining the site itself. For some, becoming a full sysadmin of their own domain might not be desired and they are looking for an approach that mirrors a hosted solution (such as WordPress.com or Blogger). What would this look like?

I setup  and installed WordPress Multi-Site. The next thing you need to do is go to your Network settings and enable registration for both sites and user accounts.



Then install both FeedWordPress and [Inpsyde Multisite Feed][16] (make sure to Network Activate FWP). Multisite Feed is a great little plugin that I found which allows you to create one RSS feed for posts across the entire the network, which means you are no longer managing the RSS feed of all students, but, rather, one MEGA&nbsp;feed.



Next you&#8217;ll leave the Network admin site and go into the Dashboard of whichever site you want to use as your course hub and then add the feed to FeedWordPress. The feed is simply %siteurl%/multifeed (this URL is also customizable in the Multisite Feed settings).



And, voila, I now have a syndication hub where students can just signup for a WordPress instance and will automatically be syndicating. I can even add a link to &#8220;Create a Site&#8221; by adding %site-url%/wp-signup.php to the menu.



Now to just sit back and relax:



As students signup for an individual site, you&#8217;ll receive email notifications as well as find them on your Network Admin Dashboard under Sites:



So when is this model appropriate? If students are producing a lot of course-specific work but is not necessarily towards a portfolio, you might take this approach. For example, say I&#8217;m teaching a U.S. Media History course, and I make an assignment that requires students to build sites in groups. My class has 24 students and I break them up into groups six groups of four. I then assign them decades (1910s, 1920s, 1930s, 1940s, 1950s, and 1960s) and tell them that I want them to build a resource site for each decade. And suppose I want a consistent look and feel. And let&#8217;s make one last assumption that future classes will either do past or future decades OR revise previous students work. Rather than having to manage several installation instances, you can allow students to fire it up themselves, and then you can manage all the updating and maintenance and you&#8217;ll still have a syndication hub of all student work.

It&#8217;s important to note that students are still technically admins meaning they can export content and then import it into their specific portfolio website if they want.

## Group Blog

So the last model I want to look at is the good ol&#8217;, tried and true group blog. I have to admit, group blog has never been my bag. I&#8217;ve always found it a little suppressing when there&#8217;s not a huge barrier to having students create their own site. But this semester I actually had a use case where it came in really handy so I wanted to show how I set it up. We have a faculty member&nbsp;who liked the idea of blogging but teaches a large lecture class called &#8220;[Architecture for Non-Majors][17]&#8221; which is a general education course generally taken during freshman year and hovers around 100 students. He didn&#8217;t want to (or felt capable of) teaching domains at that scale. That said, he wanted a public facing space where students could write about and comment on various posts about architecture.

Enter the group blog.

The challenge for this was 1.) making it easy for students to sign up and 2.) making it easy for the faculty member to manage. This gave me an opportunity to play with BuddyPress for the first time in-depth. After installing WordPress, you want to install the [BuddyPress plugin][18], one of the most popular WP plugins out there, which focuses on creating a social network on your site. BuddyPress has several popular features that you can enable including Activity Streams and Notifications:



Additionally, it generates several custom pages which you can activate very quickly such as Register. This makes it very easy for students to register for the site&#8217;s main page.



You&#8217;ll also want to make sure you&#8217;ve enabled registration within your WordPress settings under Settings > General. You&#8217;ll also want to make sure you&#8217;ve set new users to be &#8220;Authors.&#8221;



One thing I really appreciate about BuddyPress is user management. You can easily see how many users you have as well as who has not completed signup, and by that I mean they haven&#8217;t clicked the verification link from their email. This can happen for a number of reasons including Spam filters. But, anyways, it allows you at an administrator level to resend the verification email (even in bulk!).



So which model is right for you? Well, of course, that really depends on what you are trying to do and I&#8217;d suggest looking at several factors: your objective, disk space capacity, class literacy, personal vs collaborative, etc. While one could argue the merit or purity of a specific method, it&#8217;s hard to deny the flexibility of the mighty little WordPress.

&nbsp;

 [1]: http://middcreate.net
 [2]: http://www.middlebury.edu
 [3]: https://twitter.com/amcollier
 [4]: http://prpubs.us
 [5]: https://twitter.com/cogdog
 [6]: http://ds106.us
 [7]: https://reclaimhosting.com/domain-of-ones-own/
 [8]: https://create.ou.edu
 [9]: https://wordpress.org
 [10]: https://withknown.com
 [11]: https://wordpress.org/plugins/feedwordpress/
 [12]: http://cogdogblog.com/2014/07/14/feed-wordpress-101/
 [13]: https://www.blogger.com/home
 [14]: https://wordpress.org/plugins/faf/
 [15]: https://blog.timowens.io/getting-started-with-multisite-part-1-why-multisite/
 [16]: https://wordpress.org/plugins/wp-multisite-feed/
 [17]: http://thedude.oucreate.com
 [18]: https://wordpress.org/plugins/buddypress/