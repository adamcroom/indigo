---
title: "Annotating EdTech Terms of Service"
layout: post
date: 2018-04-25 10:04:07
image: /assets/images/markdown.jpg
headerImage: false
tag:
- conferences
category: blog
author: adamcroom
---

This is part two in my [wrap up posts from OLC Innovate 2018][1]. My third and final presentation was demoing and gathering feedback on a framework and tool that [Amy Collier][2] and I have been developing over the past few months.

This idea started after a panel presentation that Amy and I were on at [OpenEd 2017][3] ([my notes from my portion of that presentation are here][4]). The idea that was floating around at that specific was that institutions involved in Domain of One&#8217;s Own projects, where ownership of data is given directly to the students via a domain registration process, uniquely positions those institutions to serve as what Amy has coined as a [digital sanctuary][5], much like the recent [rise of sanctuary cities][6] in the United States. I talked about similar ideas. Mostly how, while DoOO has been often framed as the opposite of the LMS, we are now in a time where we can see its value over large public monolithic tools such as Facebook, Slack, Twitter, etc. particularly in relation to data and data privacy.

Shortly after, Amy and I quickly realized our ideas were closely aligned and we wanted to continue thinking about how we can educate publics specifically on the Terms of Service of EdTech tools. As an instructor, I&#8217;ve often given strong preference towards &#8220;real tools&#8221; over the institution-adopted tools, which often feel artificial, clunky, and lack the broader appeal of a openly networked environment. Yet, particularly in the U.S., we are now in the midst of a historical period where technology is outpacing law and the level of trust we have as it relates to a platforms ability to protect individual data is at an all time low.

The [Facebook-Cambridge Analytica scandal][7] that eventually led to Congress testimonies by Mark Zuckerberg highlighted an issue the normal user doesn&#8217;t often consider: something as simple as accessing a quiz which asks to access bits of your digital information in efforts to complete it can lead to unintentional and severe consequences.

This scenario overlaps quite nicely with what happens in a classroom often by good, well-intentioned instructors. I, myself, have done this exact thing. In one specific course I teach, I ask students to signup for account on Canva to design social media pieces. Part of the assignment objective is to learn and productively use the tool and the other objective is to compare and contrast the web-based tool to a desktop graphic design application.

But the truth is that I&#8217;ve never read Canva&#8217;s Terms of Service from the lens of either myself or my students. I couldn&#8217;t tell you if my students retain ownership of the work they create. I couldn&#8217;t tell you if they can permanently delete it should they choose.

There are websites out there, like [tosdr.org][8], that are great for giving you information on _some_ platforms, but only a few have educational use cases. Additionally, none of them seem to connect directly to the ToS themselves through something such as an annotation layer, which can bring full, real-time context into the specific statement, which is important in a time when Terms are often regularly updated.

So this is where Amy and I started to develop our idea. What can we build that would allow people to 1.) annotate terms of service related to tools they adopt in a classroom? and 2.) see an aggregated list of all current annotations. Last, if we were to start critically analyzing EdTech Terms of Service, what questions should we even ask?

### The Framework

The last question is where we started. Below are sixteen yes/no questions that make up the framework that we currently still under development. The framework has been informally developed by surveying what others have said (such as ToS;DR and [Audrey Watters][9]&#8216; [Audrey Test][10]) as well as integrating current institutional practices at specific European institutions, which we argue are ahead of the curve with respect to this issue. The questions:

  * Are the terms easy to read?
  * Can you terminate your account?
  * Does the service track you on other websites?
  * Do you grant a copyright license?
  * Is information shared with third parties?
  * Can they stop providing you a service to you at any time?
  * Can you download an archive?
  * Are users notified of changes before they are made to ToS or if information is transferred in the event of a merger/aquisition?
  * How much and what information is necessary to sign up for account? Are pseudonyms allowed?
  * What personal information is stored?
  * Are archives of terms available?
  * Does the service use cookies or third-party cookies? If so, can you opt-out?
  * Can the service sell or share your data without additional consent?
  * Can your data be used without additional consent for the purposes of research or marketing?
  * Will there be collection of special categories of personal or sensitive data? (Ex: racial/ethnic origin, finances, health).
  * Will there be consolidation, interlinking, cross-referencing or matching of personal data from multiple sources?

These questions are still being developed, vetted, and consolidated as necessary. A portion of our presentation was gathering feedback on the framework. **I&#8217;m openly requesting that you comment or annotate on this post or reach out directly if you have ideas/comments/questions.**

### The Tool

The second portion of the tool is the tool itself. We wanted to build something that would allow anybody to add to the collective analysis, building upon Mike Caulfield&#8217;s concept of [Choral Explanations][11], as we recognize that their often isn&#8217;t one definitive interpretation of a document. I built a simple form that asks the user to define the tool itself, the question they are seeking to answer, the answer itself, as well as some annotation metadata such as the specific URL and the text from the Terms of Service.



Once a &#8220;find&#8221; is submitted, that piece of data is then aggregated to a homepage which is organized by the tool.



There is much left to be desired as it relates to future development. For instance, once you see the process, you can see how this would integrate nicely into a tool such as [hypothes.is][12], or perhaps more specific, the hypothes.is annotation toolkit, in a similar manner to which Jon Udell has [written about][13] and demonstrated in projects such as the [Digital Polarization Initiative][14], a student-run project which allows students to investigate questions of truth and authority and publish their results, as well as [Science in the Classroom][15], which are annotated research papers and accompanying teaching materials.

We received really positive feedback in the session, which was a very encouraging way to end the conference. Faculty said they would like to use this in their course as an activity as well as a resource, which was great to hear. We also quickly were able to uncover some interesting answers. For instance, did you know that TurnItIn claims fair use?

> A U.S. District Court judge ruled that archiving student papers to assess originality of newly-submitted papers constitutes a fair use under the U.S. Copyright Act, provides “a substantial public benefit” and helps protect the papers from being exploited by others. Read the summary judgement.

In it&#8217;s current state, the tool isn&#8217;t quite ready for primetime. I&#8217;ll end with a request to those who are interested in exploring the tool more, whether its on the collection or development side, **reach out to either myself or Amy (Twitter: [@acroom][16] and [@amcollier][17])** as we believe are inching closer to a phase where we can to soft launch the tool at specific institutions in order to gather further feedback.

Featured image: A CC0 licensed photo from João Silas

 [1]: https://backup.adamcroom.com/2018/04/recapping-and-reflecting-on-olc-innovate-2018/
 [2]: http://redpincushion.us/blog
 [3]: https://openeducation2017.sched.com/event/BXgM/open-practices-digital-sanctuaries-a-trans-institutional-conversation-about-students-risk-and-agency-in-domains-initiatives
 [4]: https://backup.adamcroom.com/2017/10/the-criticality-of-open-platforms-opened17/
 [5]: https://er.educause.edu/articles/2017/8/digital-sanctuary-protection-and-refuge-on-the-web
 [6]: https://newrepublic.com/article/142490/donald-trump-rise-sanctuary-home
 [7]: https://www.nytimes.com/2018/03/17/us/politics/cambridge-analytica-trump-campaign.html
 [8]: https://tosdr.org
 [9]: http://hackeducation.com/
 [10]: http://hackeducation.com/2012/03/17/what-every-techie-should-know-about-education
 [11]: https://hapgood.us/2016/05/13/choral-explanations/
 [12]: http://hypothes.is
 [13]: https://blog.jonudell.net/2017/05/05/weaving-the-annotated-web/
 [14]: https://www.digipo.io/wiki/commons/index.htm
 [15]: http://www.scienceintheclassroom.org/homepage
 [16]: http://twitter.com/acroom
 [17]: http://twitter.com/amcollier
