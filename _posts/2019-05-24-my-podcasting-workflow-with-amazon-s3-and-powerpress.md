---
title: "My Podcasting Workflow with Amazon S3 and PowerPress"
layout: post
date: 2018-05-11 09:05:24
image: /assets/images/markdown.jpg
headerImage: false
tag:
- markdown
- components
- extra
category: blog
author: jamesfoster
description: Markdown summary with different options
---


---
layout: post
title: "My Podcasting Workflow with Amazon S3 and PowerPress"
author: admin
comments: true
date: 2018-05-11 09:05:24
headerImage: false
permalink: >
    /2018/05/my-podcasting-workflow-with-amazon-s3-and-powerpress
---


I just hit the publish button on the season finale of [Media and the End of the World][1]. I have to say, it&#8217;s been a lot of fun to experiment with the medium from both a media and technical perspective. One thing you learn being on both sides of the production is your ticks. For instance, I&#8217;ve learned I say &#8220;you know&#8221; and &#8220;I&#8217;d be curious to hear&#8221; quite frequently.

Ralph and I will be consecutively teaching abroad this summer so rather than putting the show on temporary hiatus without notice, we decided to &#8220;wrap the season,&#8221; and then we&#8217;ll come back as soon as we possibly can without feeling rushed. For the uninitiated, in most episodes of MATEOTW, we make a futile attempt to either cover the media or interview a media professional. And I have to say we&#8217;ve gotten pretty good at creating some semblance of a professional and entertaining production if I do say so myself. For the season finale, we decided to use it as an opportunity to reflect on the podcast itself, what our main takeaways were, as well as discuss some of my our top moments. This post isn&#8217;t about that, but  do feel free to listen to it!



Instead I wanted to give some background information into how I record, edit, host, and publicize the podcast. I&#8217;m putting a summary at the top with my entire workflow:

  * Record podcasts with mics, board, and [Adobe Audition][2].
  * Mix, master, and bounce files with Adobe Audition.
  * Upload audio files to [AWS Amazon S3][3] bucket.
  * Write a blog post in an self-hosted instance of [WordPress][4] and added power of the [PowerPress][5] plugin.
  * Create a social media card using [Adobe Photoshop][6].
  * Track podcasting analytics using [PodTrac][7].

This sounds like a lot, but it&#8217;s become a really quick process for me. In fact it&#8217;s worth noting that my process when we started was much simpler. I edited and bounced everything with GarageBand (I even did it once on the free, open-source editor Audacity) and then just stuck it on Soundcloud. This is _really_ all youneed&#8211;even for iTunes&#8211;but as I explain further down, this process also has its limits/costs. Yes, the process is now much more complex, but I&#8217;m _really_, really happy with it. The piece I usually spend the most time on is (obviously) recording followed by editing, but I&#8217;ve learned that if I can willingly accept my imperfections such as my &#8220;um&#8217;s&#8221; then my editing time is dramatically cut down. Nearly all our shows are now just straight one-takes with very, very minor edits. Okay, now for some more in-depth information.

### Recording and Editing

In Gaylord Hall, David Candy, our in-house broadcast engineer, was nice enough to spin up a podcasting studio for us out of unused microphones and boards we had in the building. By all accounts, it is more than we would ever need, so I&#8217;m incredibly grateful to be able to utilize it on the reg.



The board has 64 channels. At most, I&#8217;ve used six of the them. And for the most part, I don&#8217;t know what I&#8217;m doing. I know _just_ enough to be dangerous. David was smart and created a &#8220;rails&#8221; experience for us with several different board scene presets which activate the necessary channels for both recording and playback. At OU, we have a site-wide license for Adobe Creative Suite for all faculty, staff, and computer labs, so we are using Adobe Audition. Similar to the David&#8217;s board presets, he created a template Audition files with all the necessary tracks and proper board routing.

This makes the whole room less scary. Before this podcast, I had no previous experience with Audition and was a bit intimidated by the software, as most are with anything new from Adobe. Luckily, Audition works very similarly to other DAWS editors like Audacity, Logic, etc. which I have utilized, though one noticeable difference is that it doesn&#8217;t support virtualized instruments in the same way, say, ProTools, GarageBand, or Logic does. So it&#8217;s really best for a recording and editing interface.

It does have some nice mastering capabilities though. Over the season, I tweaked and re-tweaked the track effects rack to sweeten our vocals. I started with a preset called DeEss and Limit Mail Voice Over but it gave a harshness to my voice which is a higher frequency that Ralph&#8217;s. Now, I almost exclusively use my own modified preset that I based off a preset titled &#8220;Podcast Voice&#8221; which seems to work just fine for both Ralph&#8217;s and my track.



Next, I throw in a 30-second intro track, which is a mashup of a public domain audio from the (in)famous radio show Orson Wells&#8217; [The War of the Worlds][8] and (mostly as pure comedic contrast) a track I purchased via [AudioJungle][9] titled &#8220;[Epic Trailer Intro.][10]&#8221; I also tag the end of each episode with the last 10 seconds of the intro which fades out.

The last thing I do is I bounce the tracks down to a single mp3 file (God bless iTunes for keeping mp3&#8217;s alive). I go to Export > Multitrack Mixdown, and use the following settings which I got from [this YouTube video][11]:



This setting makes the file small enough to be easily downloaded on a phone, but still maintain a decent amount of fidelity.

### Audio File Storage

When I [announced the podcast on my blog last year][12], I noted that I had landed on Soundcloud as the storage service. Part of my reasoning was sound. For instance, Soundcloud and iTunes play quite nicely together, so it&#8217;s very easy to get a Soundcloud podcast on the iTunes store as Soundcloud produces an RSS feed that iTunes can read.

But I made a big mistake when I chose Soundcloud for my storage service. First, their analytics are terrible if not often down right wrong. Second, I misread &#8220;180 upload minutes&#8221; as &#8220;180 upload minutes _per month_.&#8221; Big error on my part which lead to me realizing we were out of space after only a few episodes. To really be an effective solution for podcasting, you have to jump into Soundcloud&#8217;s $15/month Pro Unlimited account. And I am just not up for that.

First, I considered just hosting the content myself on my personal web server and not bothering with Soundcloud, but I&#8217;m on a shared web server and didn&#8217;t want to slow down anything with the big data transfers we see due to our _massive_ audience. And then I seemed to remember that there was a conversation on the Reclaim Hosting Community site once upon a time about hosting podcasts. Sure enough, I rediscovered [a thread][13] that [Tim Klapdor][14] started in September 2016. In the thread, Tim Owens suggested S3 as a potential hosting solution and Tim replied that he took that approach (coupled with Jekyll on the front end) and that he found this particular [walk through tutorial][15] very helpful (Thanks Tim(s)! I, too, found it helpful!)

S3 stands for Simple Storage Service and is one of many offerings that Amazon has for storage. If you&#8217;ve never heard of it, you have likely accessed files on it as it&#8217;s heavily utilized by some big name players including Netflix. So, if you&#8217;ve ever streamed anything on Netflix, you are are a benefactor of S3. The story of AWS is pretty great. In short, they had built up an internal team that had both access to many servers and the internal personnel to manage it, so they decided to monetize it.  This is now what fairly common and referred to as cloud computing. One benefit is that Amazon can store your data in multiple physical spaces which creates redundancy and gives you (according to official Amazon stats) 99.99% up-time and 99.999999999% durability.

> Data in Amazon S3 Standard, S3 Standard-IA, and Amazon Glacier storage classes is automatically distributed across a minimum of three physical Availability Zones (AZs) that are typically miles apart within an AWS Region. The Amazon S3 One Zone-IA storage class stores data in a single AZ, and is ideal for customers who want a lower cost option for infrequently accessed data and do not require the availability and resilience of S3 Standard storage. Amazon S3 can also automatically replicate data to any other AWS Region.

Unlike most hosting services where you pay a flat monthly fee, S3 charges you a monthly rate based off of how much data you are storing and how often it&#8217;s being accessed. Like your electric bill, the more you utilize the more you pay. This makes it really easy to scale web products without having to pay for potential scale upfront. To give you a sense of cost, as of this post, Amazon charges a hair over $.02/month for your first 50TB of storage. Insane, yes? And if two pence is too rich for your blog, they have a free 12-month period called &#8220;free tier&#8221; which includes 5GB of space on S3. Season one was 23 mp3 files weighing in at 750MB, so we&#8217;ve got plenty of room for growth there. So we have yet to be charged a single penny.

As I mentioned, AWS also charges for information retrieved, not just stored. That pricing depends on where your physically store it, so here&#8217;s an example of a server in Northern Virginia.



As I mentioned, we are still in the &#8220;free tier&#8221; year, but they also have a handy calculator, and I put in the numbers for April 2018. I made a calculation based on our usage which including  storing 600MB, 375 put/copy/post/list requests and 700 get requests (this number is equivalent to our monthly listenership total) and it came out to a whopping total of&#8230;.. wait for it&#8230;.. four cents. After using it for a decent length of time, I can now confidently say I would highly recommend it as a solution for storing all kinds of data for backup purposes. Photos, audio, video, you name it.

### Podcast Website

Now AWS S3 is JUST for hosting the audio files themselves. I have to also maintain a website as a portal for accessing the podcasts, but even that simple move beats the heck out of Soundcloud&#8217;s $15/month charge. Now if you factor in a web domain and a storage package (which we offer at OU for $12/yr or is available through [Reclaim Hosting][16] at $30/yr), you&#8217;ll quickly see that the price is very reasonable assuming that you are just starting off with your experimentation (I&#8217;m excluding software costs as there are free alternatives to Adobe CS such as [Audacity][17]).

So I moved all of the audio content over to S3 and now needed a way to link this data to our website. For iTunes (or any other podcatcher to &#8220;catch&#8221; your &#8220;pod&#8221;) your site has to have RSS feed. Soundcloud&#8217;s RSS feed has all the necessary metadata for iTunes, but while WordPress does indeed have an RSS feed out of the box, it doesn&#8217;t contain all the necessary data points iTunes needs. For instance, in addition to titles and descriptions, iTunes needs information on the show itself as well as data points like length, explicit nature of content, etc.

I installed a WordPress plugin called [PowerPress][5] to cover these needs. PowerPress is a plugin that is supported by a company called [BluBrry][18], which is another full fledged podcasting solution. They support this open-source plugin that allows you to integrate your content or BluBrry content into your website. There are premium features available to BluBrry customers, but for my purposes, the plugin works just fine. So what happens is that I fill out some form fields based on information related to the show on an admin panel:



And then that information is then coded into the RSS feed:



If you look closely, you see specific pieces of data that begin with `
