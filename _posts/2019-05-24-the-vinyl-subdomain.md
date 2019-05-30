---
layout: post
title: "The Vinyl Subdomain"
date: 2016-03-28 03:03:54
projects: true
headerImage: false
tag:
    - indie-edtech
    - music
category: project
permalink: /2016/03/the-vinyl-subdomain
author: adamcroom
published: true
---

Let me just start by saying we live in a really cool time in history. 🙂 I published [a blog post][1] on Saturday evening about how I noticed that [Discogs.com][2] had an API and how COOL it would be to have a site that pulled in all the data. I keep an [online record of my vinyl collection][3] there so it seemed like a half-decent idea to see if my data could be pulled into a site that I control. Well, I&#8217;m proud to say that not even 48 hours later and it exists (head over to [Let me just start by saying we live in a really cool time in history. 🙂 I published [a blog post][1] on Saturday evening about how I noticed that [Discogs.com][2] had an API and how COOL it would be to have a site that pulled in all the data. I keep an [online record of my vinyl collection][3] there so it seemed like a half-decent idea to see if my data could be pulled into a site that I control. Well, I&#8217;m proud to say that not even 48 hours later and it exists (head over to][4] if you would like to see it) thanks MOSTLY to [Tom Woodward][5] who shall be given any vinyl he&#8217;s ever wanted.

For the majority of the technical specs, I recommend that you read Tom&#8217;s blog [where he brilliantly details][6] how he parsed the API into a Google Spreadsheet and then turned it into a WordPress Custom Post Type. He&#8217;s shared both the [script][7] and the [plugin][8].

What this means for poor little me who knows nothing about anything APIs is that I do what Tom tells me to do and then magically this happens in my WordPress instance:



It also looks like Tom has added all the details that are attached to the record as Custom Fields within the Custom Post Type:



So there you have it. I&#8217;ve officially reclaimed my vinyl data. Raise your glasses to Tom, everyone. Let&#8217;s have a party.



I had to do a couple of different quick edits to my template to get the posts to show up on the home page. By default, WordPress doesn&#8217;t have custom post types in &#8220;the loop&#8221; so I added them in by adding this bit of code to functions.php:

add_filter( 'pre_get_posts', 'my_get_posts' );
function my_get_posts( $query ) {
if ( is_home() && false == $query-&gt;query_vars['suppress_filters'] )
$query-&gt;set( 'post_type', array(
'YOUR_CUSTOM_POST_TYPE_HERE' ) );
    return $query;
 }

I also wanted to pull the Custom Fields into the post itself so that information was publicly exposed. Right under the_content();?  portion of my single.php file I dropped in this:

&lt;?php the_meta(); ?&gt;

Simple enough.

Next, I wanted to build out a way to explore the collection based on the custom fields so you could not only look by purchase date but also by artist, release year, or record label. I came across a WordPress plugin called [Filter Custom Fields & Taxonomies Light][9]. I have to say I was quite impressed with how simple the UI was. I was able to quickly whip up a query page:



After adding some CSS style customizations to it, I went ahead and made a second version of the tool that could function as a widget on a single post so folks could surf around the site a bit quicker.



Last, I went in and manually grabbed images of the records to put in place to get a nice store front look to the site:



On another note, my colleague [John Stewart][10] and I were having some conversations this morning about what _other _APIs could be beneficial to the project. One idea was to see how we could link the collection to information from other sources. For instance, what if we pulled in the Spotify playlist for each record and embedded it directly within the post? Or what if we could pull the album images from the Amazon API? It&#8217;s a fun world once you started realizing how you can start to hook up the plumbing that&#8217;s been put out there for us on the web.

I can&#8217;t thank Tom enough for the help or Kin for the inspiration. Speaking of that [API Evangelist][11], he gave a [rather inspiring answer][12] to his own question of how to move the needle on APIs. He notes that it won&#8217;t be e-commerce, the big companies of today, legacies of yesteryear, governments, or even (sadly) the evangelists. According to Kin:

> It will be the API literate individual, who understands that they can get access to their own data, and information from any website, system, application, connected device, company, and institution, using APIs. It will be people who understand that they can make their education, career, and the web into what they want, using APIs. That the web is programmable. A digitally aware individual who assumes full control over their online self, taken it back from the tech giants, understanding that they own all the exhaust from their online (and increasingly offline) personal, and professional life.

And I think that sums up a lot of my currently feelings (in a much more articulate manner). And this is an area where I see a lot of opportunity for education. The value of our institutions is our ability to shape a literate and aware citizenry. But, first, [music][4]. 🙂

 [1]: https://backup.adamcroom.com/2016/03/a-vinyl-api-of-ones-own/
 [2]: http://discogs.com
 [3]: https://www.discogs.com/user/acroom/collection
 [4]: http://vinyl.adamcroom.com
 [5]: http://twitter.com/twoodwar
 [6]: http://bionicteaching.com/discography-to-wordpress/
 [7]: https://gist.github.com/woodwardtw/2f5d898442d55e06a17d
 [8]: https://gist.github.com/woodwardtw/fb22ee592019d1cb870f
 [9]: https://wordpress.org/plugins/filter-custom-fields-taxonomies-light/
 [10]: http://twitter.com/jstew511
 [11]: http://apievangelist.com
 [12]: http://apievangelist.com/2016/03/27/this-is-how-apis-will-deliver-the-change-we-need/
