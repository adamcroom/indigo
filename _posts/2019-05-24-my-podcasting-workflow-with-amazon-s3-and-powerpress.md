---
title: "My Podcasting Workflow with Amazon S3 and PowerPress"
layout: post
date: 2018-05-11 09:05:24
image: /assets/images/markdown.jpg
headerImage: false
projects: true
tag:
- podcasting
- wordpress
- aws
category: project
author: adamcroom
description: Markdown summary with different options
permalink: /2018/05/my-podcasting-workflow-with-amazon-s3-and-powerpress/
---

I just hit the publish button on the season finale of [Media and the End of the World](http://mediaandtheendoftheworld.com). I have to say, it's been a lot of fun to experiment with the medium from both a media and technical perspective. One thing you learn being on both sides of the production is your ticks. For instance, I've learned I say "you know" and "I'd be curious to hear" quite frequently.

Ralph and I will be consecutively teaching abroad this summer so rather than putting the show on temporary hiatus without notice, we decided to "wrap the season," and then we'll come back as soon as we possibly can without feeling rushed. For the uninitiated, in most episodes of MATEOTW, we make a futile attempt to either cover the media or interview a media professional. And I have to say we've gotten pretty good at creating some semblance of a professional and entertaining production if I do say so myself. For the season finale, we decided to use it as an opportunity to reflect on the podcast itself, what our main takeaways were, as well as discuss some of my our top moments. This post isn't about that, but  do feel free to <a href="https://mediaandtheendoftheworld.com/podcasts/022-season-one-finale/">listen to it</a>!

Instead I wanted to give some background information into how I record, edit, host, and publicize the podcast. I'm putting a summary at the top with my entire workflow:

*   Record podcasts with mics, board, and [Adobe Audition](https://www.adobe.com/products/audition.html).
*   Mix, master, and bounce files with Adobe Audition.
*   Upload audio files to [AWS Amazon S3](https://aws.amazon.com/s3/) bucket.
*   Write a blog post in an self-hosted instance of [Wordpress](http://wordpress.org) and added power of the [PowerPress](https://wordpress.org/plugins/powerpress/) plugin.
*   Create a social media card using [Adobe Photoshop](http://adobe.com/photoshop).
*   Track podcasting analytics using [PodTrac](http://podtrac.com).

This sounds like a lot, but it's become a really quick process for me. In fact it's worth noting that my process when we started was much simpler. I edited and bounced everything with GarageBand (I even did it once on the free, open-source editor Audacity) and then just stuck it on Soundcloud. This is _really_ all youneed--even for iTunes--but as I explain further down, this process also has its limits/costs. Yes, the process is now much more complex, but I'm _really_, really happy with it. The piece I usually spend the most time on is (obviously) recording followed by editing, but I've learned that if I can willingly accept my imperfections such as my "um's" then my editing time is dramatically cut down. Nearly all our shows are now just straight one-takes with very, very minor edits. Okay, now for some more in-depth information.

### Recording and Editing

In Gaylord Hall, David Candy, our in-house broadcast engineer, was nice enough to spin up a podcasting studio for us out of unused microphones and boards we had in the building. By all accounts, it is more than we would ever need, so I'm incredibly grateful to be able to utilize it on the reg.

![](http://backup.adamcroom.com/wp-content/uploads/2017/12/IMG_1755-2500x1875.jpg)

The board has 64 channels. At most, I've used six of the them. And for the most part, I don't know what I'm doing. I know _just_ enough to be dangerous. David was smart and created a "rails" experience for us with several different board scene presets which activate the necessary channels for both recording and playback. At OU, we have a site-wide license for Adobe Creative Suite for all faculty, staff, and computer labs, so we are using Adobe Audition. Similar to the David's board presets, he created a template Audition files with all the necessary tracks and proper board routing.

This makes the whole room less scary. Before this podcast, I had no previous experience with Audition and was a bit intimidated by the software, as most are with anything new from Adobe. Luckily, Audition works very similarly to other DAWS editors like Audacity, Logic, etc. which I have utilized, though one noticeable difference is that it doesn't support virtualized instruments in the same way, say, ProTools, GarageBand, or Logic does. So it's really best for a recording and editing interface.

It does have some nice mastering capabilities though. Over the season, I tweaked and re-tweaked the track effects rack to sweeten our vocals. I started with a preset called DeEss and Limit Mail Voice Over but it gave a harshness to my voice which is a higher frequency that Ralph's. Now, I almost exclusively use my own modified preset that I based off a preset titled "Podcast Voice" which seems to work just fine for both Ralph's and my track.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/effectsracksettings.png)

Next, I throw in a 30-second intro track, which is a mashup of a public domain audio from the (in)famous radio show Orson Wells' [The War of the Worlds](http://www.sacred-texts.com/ufo/mars/wow.htm) and (mostly as pure comedic contrast) a track I purchased via [AudioJungle](https://audiojungle.net) titled "[Epic Trailer Intro.](https://audiojungle.net/item/epic-trailer-intro/8322562)" I also tag the end of each episode with the last 10 seconds of the intro which fades out.

The last thing I do is I bounce the tracks down to a single mp3 file (God bless iTunes for keeping mp3's alive). I go to Export > Multitrack Mixdown, and use the following settings which I got from [this YouTube video](https://youtu.be/0PO0NUcS370?t=6m16s):

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/mixdown.png)

This setting makes the file small enough to be easily downloaded on a phone, but still maintain a decent amount of fidelity.

### Audio File Storage

When I [announced the podcast on my blog last year](http://backup.adamcroom.com/2017/11/media-and-the-end-of-the-world-the-podcast/), I noted that I had landed on Soundcloud as the storage service. Part of my reasoning was sound. For instance, Soundcloud and iTunes play quite nicely together, so it's very easy to get a Soundcloud podcast on the iTunes store as Soundcloud produces an RSS feed that iTunes can read.

But I made a big mistake when I chose Soundcloud for my storage service. First, their analytics are terrible if not often down right wrong. Second, I misread "180 upload minutes" as "180 upload minutes _per month_." Big error on my part which lead to me realizing we were out of space after only a few episodes. To really be an effective solution for podcasting, you have to jump into Soundcloud's $15/month Pro Unlimited account. And I am just not up for that.

First, I considered just hosting the content myself on my personal web server and not bothering with Soundcloud, but I'm on a shared web server and didn't want to slow down anything with the big data transfers we see due to our _massive_ audience. And then I seemed to remember that there was a conversation on the Reclaim Hosting Community site once upon a time about hosting podcasts. Sure enough, I rediscovered [a thread](https://community.reclaimhosting.com/t/podcasting-with-reclaim/383) that [Tim Klapdor](http://timklapdor.com) started in September 2016\. In the thread, Tim Owens suggested S3 as a potential hosting solution and Tim replied that he took that approach (coupled with Jekyll on the front end) and that he found this particular [walk through tutorial](https://growthedream.com/host-podcast-files-amazon-s3/) very helpful (Thanks Tim(s)! I, too, found it helpful!)

S3 stands for Simple Storage Service and is one of many offerings that Amazon has for storage. If you've never heard of it, you have likely accessed files on it as it's heavily utilized by some big name players including Netflix. So, if you've ever streamed anything on Netflix, you are are a benefactor of S3\. The story of AWS is pretty great. In short, they had built up an internal team that had both access to many servers and the internal personnel to manage it, so they decided to monetize it.  This is now what fairly common and referred to as cloud computing. One benefit is that Amazon can store your data in multiple physical spaces which creates redundancy and gives you (according to official Amazon stats) 99.99% up-time and 99.999999999% durability.

> Data in Amazon S3 Standard, S3 Standard-IA, and Amazon Glacier storage classes is automatically distributed across a minimum of three physical Availability Zones (AZs) that are typically miles apart within an AWS Region. The Amazon S3 One Zone-IA storage class stores data in a single AZ, and is ideal for customers who want a lower cost option for infrequently accessed data and do not require the availability and resilience of S3 Standard storage. Amazon S3 can also automatically replicate data to any other AWS Region.

Unlike most hosting services where you pay a flat monthly fee, S3 charges you a monthly rate based off of how much data you are storing and how often it's being accessed. Like your electric bill, the more you utilize the more you pay. This makes it really easy to scale web products without having to pay for potential scale upfront. To give you a sense of cost, as of this post, Amazon charges a hair over $.02/month for your first 50TB of storage. Insane, yes? And if two pence is too rich for your blog, they have a free 12-month period called "free tier" which includes 5GB of space on S3\. Season one was 23 mp3 files weighing in at 750MB, so we've got plenty of room for growth there. So we have yet to be charged a single penny.

As I mentioned, AWS also charges for information retrieved, not just stored. That pricing depends on where your physically store it, so here's an example of a server in Northern Virginia.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/nvirginia.png)

As I mentioned, we are still in the "free tier" year, but they also have a handy calculator, and I put in the numbers for April 2018\. I made a calculation based on our usage which including  storing 600MB, 375 put/copy/post/list requests and 700 get requests (this number is equivalent to our monthly listenership total) and it came out to a whopping total of..... wait for it..... four cents. After using it for a decent length of time, I can now confidently say I would highly recommend it as a solution for storing all kinds of data for backup purposes. Photos, audio, video, you name it.

### Podcast Website

Now AWS S3 is JUST for hosting the audio files themselves. I have to also maintain a website as a portal for accessing the podcasts, but even that simple move beats the heck out of Soundcloud's $15/month charge. Now if you factor in a web domain and a storage package (which we offer at OU for $12/yr or is available through [Reclaim Hosting](https://reclaimhosting.com) at $30/yr), you'll quickly see that the price is very reasonable assuming that you are just starting off with your experimentation (I'm excluding software costs as there are free alternatives to Adobe CS such as [Audacity](https://sourceforge.net/projects/audacity/)).

So I moved all of the audio content over to S3 and now needed a way to link this data to our website. For iTunes (or any other podcatcher to "catch" your "pod") your site has to have RSS feed. Soundcloud's RSS feed has all the necessary metadata for iTunes, but while Wordpress does indeed have an RSS feed out of the box, it doesn't contain all the necessary data points iTunes needs. For instance, in addition to titles and descriptions, iTunes needs information on the show itself as well as data points like length, explicit nature of content, etc.

I installed a Wordpress plugin called [PowerPress](https://wordpress.org/plugins/powerpress/) to cover these needs. PowerPress is a plugin that is supported by a company called [BluBrry](https://www.blubrry.com), which is another full fledged podcasting solution. They support this open-source plugin that allows you to integrate your content or BluBrry content into your website. There are premium features available to BluBrry customers, but for my purposes, the plugin works just fine. So what happens is that I fill out some form fields based on information related to the show on an admin panel:

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/Screen-Shot-2018-05-09-at-10.20.17-AM.png)

And then that information is then coded into the RSS feed:

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/podcastfeed.png)

If you look closely, you see specific pieces of data that begin with `<itunes:` . Those are unique data points that iTunes requires.

Similarly, an individual episode post looks like so:

![](http://backup.adamcroom.com/wp-content/uploads/2017/12/Screen-Shot-2017-12-20-at-3.36.28-PM.png)

This looks very similar to a normal Wordpress post. The blog post title doubles as the episode title. The post itself becomes the description (iTunes will read a limited number of HTML tags such as links and basic styling). And then there are some custom fields at the bottom where I plug in in the link from AWS S3\. All files are stored in what AWS refers to as a "bucket." Here is where I would refer you to the blog post Tim Klapdor [referenced](https://www.blubrry.com), (as well as [Wes Fryer](http://www.speedofcreativity.org)'s [blog post](http://www.speedofcreativity.org/2016/02/16/podcasting-costs-with-amazon-s3/) on S3 as a hosting solution) but quickly... After creating a bucket and then uploading the file, you just want to make sure the file is to be publicly read as S3 initially marks all files private.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/d5xF0JyRuf.gif)

I should explicitly say that you can host this file ANYWHERE and AWS is one of thousands of possible solutions (but I do really like the scalability and low cost). I plug that link into the Wordpress post and then add tracking to the frontend of link. I am using a service called [podtrac](http://podtrac.com) which is free. Once you have given Podtrac some basic info about where your podcast lives, all you do is add `https://dts.podtrac.com/redirect.mp3/` to the front of every episode link.

### Promotion

Okay, the _last_ thing that I do is I create a small graphic to accompany the podcast. I do think most for aesthetic purposes for social media. As you are likely aware, Facebook and Twitter will both auto generate thumbnails for links. This is usually either the Featured Image of a Wordpress post or simply the first image found in the post itself. I wanted to control this a little bit more, so I've created a little Photoshop template file that I change out every episode. Our fonts are [Futura Extra Bold](https://www.fonts.com/font/urw/futura/extra-bold) and [Hemogoblin](https://www.dafont.com/hemogoblin.font) (which is a fantastic name by the way). The card contains the episode number, the topic or guest(s), our logo, and necessary links.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/ep015.jpg)

Next, publish your post! I've set up my blog to auto tweet a link to the blog post so that's all automated.

You can also choose on the PowerPress admin page if and where you want audio players on your site. I've set ours up to have the player at the top of every blog post.

### Publishing on iTunes and Google Play

Getting setup on iTunes is actually a pretty easy process, though Apple does approve every podcast. For our podcast, it took two or three days to hear back that it had been approved. You'll actually submit your podcast using i[Tunes Podcast Connect](https://podcastsconnect.apple.com/) which requires an [Apple ID](https://appleid.apple.com). For the approval process, I get the sense that they just want to make sure that the feed is properly working. So to close the loop on publishing the podcast, after I put the information into the PowerPress admin page that populated the RSS Feed, the first thing iTunes does is ask for your feed address. Once you've entered it, click "Validate" and it will tell you whether it was able to pull all the necessary data points. If you get the green button marked "Prepared for Submission" you can now submit the podcast to the store.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/itunes-2500x1293.jpg)

Getting approved for the [Google Play](https://play.google.com/music/podcasts/publish) store is a very similar process to iTunes. In fact, one thing that's nice about Google is that if there isn't specific Google Play data in the RSS feed, it will default to the iTunes metadata and use that instead.

![](http://backup.adamcroom.com/wp-content/uploads/2018/05/googleplay.png)

So there's a glimpse into the technical side of Media and the End of the World. It's always helpful for me to document this information if only for myself (I search my own blog constantly for links I've dropped in here) but I hope it's valuable to others as well. As always, I'm happy to answer questions about any of this in the comments below.

<small>Featured Image: [CC0 licensed image](https://stocksnap.io/photo/2KWC7GFQLV) by [Antonio](https://stocksnap.io/author/kado)</small>
