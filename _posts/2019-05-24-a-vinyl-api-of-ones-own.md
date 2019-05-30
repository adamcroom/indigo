---
layout: post
title: "A Vinyl API of One's Own"
date: 2016-03-26 07:03:58
projects: true
headerImage: false
tag:
    - indie-edtech
    - music
category: project
permalink: /2016/03/a-vinyl-api-of-ones-own
author: adamcroom
published: true
---

I&#8217;ve been on a vinyl kick as of late. It happens that a lot of the records I listened to&nbsp;when I was&nbsp;[most emotionally vulnerable to trite love songs][1] are hitting their ten or fifteen year anniversary and being released/re-released on vinyl.

For instance, I recently grabbed a copy of the Little Miss Sunshine soundtrack&nbsp;[Guestroom Records][2], Norman&#8217;s local independent record store. Guestroom holds a special place in my heart.&nbsp;When I got engaged to my wife, we were lucky enough to be allowed to photograph are engagement pictures inside of there:









Little Miss Sunshine is a really interesting case study. The first time I saw it in theaters was during the&nbsp;[Austin City Limits 2006][3]&nbsp;Music Festival in this ran down (what I think was)&nbsp;independent movie theater located in a local strip mall in Austin, Texas. My friend and I had decided to skip the morning lineup and check out downtown Austin. The movie&nbsp;arguably lands on the list of one of the movies most propelled after Sundance as it was picked up by Fox Searchlight and ended up right north of $100mm at the box office despite having an $8mm budget (I&#8217;m learning all of this via the [Wikipedia page][4]). Even still, this movie was &#8220;too indie&#8221; for the Oklahoma theaters, so it was a real treat to actually in a theater.

Anyways, the vinyl was a great snag. I actually remember buying the record at Borders bookstore ([RIP][5]). Looking back, I totally forgot how much bookstores upcharged CDs. Whatever you could find your regular neighborhood shopping store for $12.99 was always $18.99 at a bookstore, so I apparently was really jonesing to have a copy of this bad boy.

When I picked up the record (in the used bin of all places), I noticed a printed metallic number in the lower left hand corner of the jacket.

flickr photo shared by adam.croom under a Creative Commons ( BY ) licenseIt&#8217;s also a &#8220;clear with pink and yellow swirl&#8221; printing which looks absolutely gorgeous.

[flickr photo][6] shared by [adam.croom][7] under a [Creative Commons ( BY ) license][8]So I knew this was an absolute steal. When I was checking out, I chatted with the manager&nbsp;about the record as well as the upcoming [Record Store Day][9]&nbsp;releases. He&nbsp;gave me some interesting insight into why&nbsp;the record was a really good find. He said it had&nbsp;just came in and that it was originally released as a Black Friday special. This seemed like a really good deal of knowledge; the kind you would [expect to get from your local record store][10].

As I slowly build up a modest collection, I have found myself on the&nbsp;hunt for more info online. I landed on [Discogs.com][11], which is the largest wealth of album release information I&#8217;ve ever landed on. It is a must for anyone looking for the small, record store like, information about every release. And I really mean the smallest detail. Check out this description of a [Motion City Soundtrack / Limbeck 7&#8243; Split][12] I&#8217;ve been trying to score for some time:

> 
>   001-002 = Blue w/ White, Grey, Black; gold metallic number 003-100 = Clear w/ Grey, White, Black; gold metallic number 101-200 = Clear w/ Grey, White, Black; silver metallic number 201-248 = Clear w/ Grey, White, Black; pink metallic number 249 = Clear w/ Grey, White, Orange; pink metallic number 250-299 = Clear w/ Grey, White, Black, pink metallic number 300 = Clear w/ Grey, White, Black, black number 301-310 = Blue w/ Blue, White, Orange, green number 311-323 = Clear w/ Grey, White, Orange, green number 324-330 = Clear w/ Grey, White, Orange, purple number 331-511 = Clear w/ Grey, White, Orange, black number 512-600 = Blue w/ Blue, White, Orange, black number 601-634 = Clear w/ Grey, White, Black, purple metallic number 635 = Blue w/ Blue, White, Black, purple metallic number 636-638 = Clear w/ Grey, White, Black, purple metallic number 639 = Clear w/ Grey, White, Black, black number 640-655 = Clear w/ Grey, White, Black, purple metallic number 656 = Blue w/ Blue, White, Black, purple metallic number 657-665 = Clear w/ Grey, White, Black, purple metallic number 666 = Clear w/ Grey, White, Black, black number 667-687 = Clear w/ Grey, White, Black, purple metallic number 688 = Blue w/ Blue, White, Black, purple metallic number 689-700 = Clear w/ Grey, White, Black, purple metallic marker 701-800 = Clear w/ Grey, White, Black, green metallic number 801-824 = Blue w/ Grey, White, Lavender, blue metallic number 825-900 = Blue w/ Blue, White, Lavender, blue metallic number 901-1000 = Blue w/ Blue, White, Lavender, pink metallic number
> 


  How&nbsp;fascinating is this? The split was only released in 1,000 copies and has 28 (!) variations. And they are incredibly random. Some runs&nbsp;are 99 copies, other 12, 11, two, one (#666 was a single press in clear with grey/white/black). The amount of work that went into 28 different silk screening variations is mind-numbing but also&nbsp;highly&nbsp;valuable to me as a collector/potential customer (Did I mention how its also a marketplace?). The album has only two songs but they mean something to me as 1.) they both were two of the most influencial bands in my formative years and 2.) I distinctly remember talking to Patrick Carrie of Limbeck before a show in Oklahoma City and asking him if they would be performing Perfect Teeth (the cut they did for this specific release). Ah, the way I used to try to find ways to let people know of my insider knowledge :wink:.



  Discogs had good info on the Little Miss Sunshine Record as well. It doesn&#8217;t note the Black Friday release fact (though a user had indeed embedded a German video that reviews it), but I verified it via the labels Facebook page and the Record Store Day website and have added that to the Notes section of the article.








  
    
      
        Record Store Day selected Little Miss Sunshine Movie Soundtrack Limited Edition Vinyl for its #BlackFriday event! To&#8230;
      
      
      
        Posted by Lakeshore Records on&nbsp;Friday, December 5, 2014
      
    
  


&nbsp;


  Anyways, a lot of talk at the Indie EdTech Data Summit,&nbsp;thanks to Kin Lane, percolated around not only how we create APIs but leverage the APIs around us. Given that Discogs has so many data points around vinyl, I was interested in if there was an API that existed around the service, and, indeed, there&#8217;s a REST API built around the service.


[discogs.com/developers/][13]


  One nice thing about the API is barcode integration. Discogs has a very slick iOS app&nbsp;(sorry Android users) that allows me to scan albums in the store and pull up info on it. This allowed me to quickly put my collection online by scanning in all of my vinyl barcodes and then adding them to my &#8220;Collection&#8221; (I&#8217;m still working on the albums that are pre and early 1980s which obviously don&#8217;t have barcodes).



  I asked Kin if he had looked into the Discogs API and, as it turns out, he is aware of every API in existence (he had heard of it) but does not know enough to be thoroughly knowledgeable of ALL of them&#8230; API Evangel-what?! The humanity&#8230;



  Anyways,&nbsp;I&#8217;ve been thinking about how I can leverage the Discog API to &#8220;reclaim&#8221; my record collection on my domain. I would love to utilize&nbsp;vinyl.adamcroom.com as a space to show off my recent grabs. I&#8217;m thinking of a WordPress instance with a card-based theme that allows you to surf my collection. It does look like someone has done some a really nice initial work at integrating the Discogs API with WordPress for something called RecordPress:





  The API doesn&#8217;t pull images, but I assume that&#8217;s because most are user submitted and they maintain the copyright. That doesn&#8217;t bother me too much as it would give me a good excuse to take more photos.



  Unfortunately, the work on RecordPress appears to have been abandoned for over a year, and even though they promised to put up their work on Github, I can&#8217;t seem to locate it. This is one reason I&#8217;m interested in promoting an open-source approach to development. It really helps to allow collaborators to pick up a project, particularly if you tend to get distracted (I never get distrac..)



  So I look forward to seeing if this ever comes out, but if it doesn&#8217;t come soon, I&#8217;m going to start seeing how I can refine my chops enough to hook the two up (currently recruiting Tom Woodward :smile:)


In my attempt to tie my entire world around #IndieEdTech, I&#8217;ll leave with the thought that this kind of project is what gets me excited about learning more with APIs. There are arguably very few people that would be interested in a WordPress-powered, card-based theme that shows their Discogs.com collection (though there does [seem to be interest][14] around a WordPress widget). It&#8217;s quite niche. But that&#8217;s sort of the point. This type of work allows me to build out technology in ways that deeply reflect who I am. Technology to reflect the user instead of the other way around. This current distraction stint in vinyl is merely a vessel for me to reconnect with myself and an identity. Many tools, many&nbsp;needs. And that, to me, is always an endeavor worth pursuing.

 [1]: http://www.smbc-comics.com/?db=comics&id=2253#comic
 [2]: http://www.guestroomrecords.com
 [3]: https://en.wikipedia.org/wiki/Austin_City_Limits_Music_Festival#2006
 [4]: https://en.wikipedia.org/wiki/Little_Miss_Sunshine
 [5]: http://www.wsj.com/articles/SB10001424052702303661904576454353768550280
 [6]: https://flickr.com/photos/acroom/26030738016 "Little Miss Sunshine Vinyl"
 [7]: https://flickr.com/people/acroom
 [8]: https://creativecommons.org/licenses/by/2.0/
 [9]: http://recordstoreday.com
 [10]: http://bavatuesdays.com/reclaim-records/
 [11]: https://www.discogs.com/
 [12]: https://www.discogs.com/Motion-City-Soundtrack-Limbeck-LimbeckMotion-City-Soundtrack-Split/release/3574412
 [13]: https://www.discogs.com/developers/
 [14]: https://www.discogs.com/forum/thread/401847
