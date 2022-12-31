---
title: "2022 Holidays Open Chess Tournament"
date: 2022-12-30T20:49:35-08:00
draft: true
author: "Victor Zheng"
categories: ["chess-club"]
tags: ["events", "chess", "organizing"]
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: ""
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "https://raw.githubusercontent.com/victor-zheng-codes/Personal-Blog/main/content/posts/post-files/holidays-open/HHCC%202022%20Holidays%20Open.jpg" # image path/url
    alt: "The 2022 Hart House Holidays Open" # alt text
    caption: "The 2022 Hart House Holidays Open in the Great Hall of Hart House" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/victor-zheng-codes/Personal-Blog/tree/main/content/posts"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

The Hart House Holidays Open hosted by the historic Hart House Chess Club (HHCC) returned for the first time since the pandemic. This holiday season tradition had been sidelined since Dec. 2019 thanks to the COVID-19 pandemic and the gathering restrictions stemmed from it. I had the privilege (or responsibility as a HHCC Exec) of joining the tournament organizing team as one of the lead organizers for the event. 

<hr>

### The Event Recap
212 participants descended on the Great Hall of Hart House at the University of Toronto from Dec. 9-11, 2022, for a weekend full of chess. 5-rounds, split in 6 rating-divided sections, with a $8000+ prize fund, resulted in possibly the biggest chess tournament in Toronto at Hart House since the 1970s, and perhaps the biggest in Toronto in the last decade. The winner of the Crown (highest section) was Max Chen, a high-school student who had attended every Hart House Holiday Open tournament since his first in 2014.  

I wrote the [event recap here](https://harthousechess.com/2022/12/13/2022-hart-house-holidays-open-attracts-record-breaking-crowd-of-212-players/) with full details on the tournament and the results. 

|![](https://raw.githubusercontent.com/victor-zheng-codes/Personal-Blog/main/content/posts/post-files/holidays-open/Board-One.jpg)|
| :--: |
| <b>Max Chen and International Master Nikolay Noritsyn played in Rd 3 with Max coming out on top. Max went on to win the tournament.</b>|

### My Role as an Organizer

Although my official title is Co-Communications Director on the HHCC Executive Board, I was involved in a variety of tasks, including:
- **keeping track of the tournament pre-registrations**
    - We historically used in-person payments by cash, but post-COVID, Hart House offers an online payment option. The online system is more secure and robust and was the way that we went. 
    - Hart House sends us volunteers a list of people who paid online, and this list isn't in the correct order / format for chess players. Ratings are not sorted, players input wrong CFC IDs (or are unrated), sometimes parents register their children, players request byes, and there are players who are from other countries and not unrated. 
        - Thus, I designed (alongside Ahmed Khalf, a HHCC Exec) a [system](https://github.com/Hart-House-Chess-Club/cfc-status) to keep track of pre-registrations by parsing through CFC-IDs and taking data from the convenient public API for chess players in Canada. 
    - I also created an [application](https://github.com/Hart-House-Chess-Club/HH-registration-data) to keep track of pre-registration data, since I had to contact Hart House to get the latest data on the registrations weekly. This allowed us to determine registrations and calculate how many people had registered for certain sectisns without waiting for the weekly data.
- **maintaining the tournament webpage**
    - Over the past few months, I have undertaken the responsibility of updating the website for all of our events and activities. For this event, it was no different, and I created the [tournament page](https://harthousechess.com/2022/10/15/hart-house-chess-club-holidays-open-2022/) on our [harthousechess.com](https://harthousechess.com/) website. 
    - In addition, for this event, I decided to embark on another project to create an event specific tournament website. In my opinion, an event specific webpage is the gold standard for most major Canadian tournaments today (The Canadian Open, attracting ~350 players, always has an event webpage.) I think we should celebrate good ideas and an event webpage is grounded in evidence of success. The website that I created involved contacting UofT to prepare a sa.utoronto.ca webpage, resulting in our new website, [harthousechess.sa.utoronto.ca](http://harthousechess.sa.utoronto.ca/). Of course, this website needs to be renewed annually, and so the link may someday die :(. Interestingly, prior to 2015, our Club used to use hhchess.sa.utoronto.ca (that data is now all lost) before changing to harthousechess.com. I can go on a tangent on the sa.utoronto.ca system, but it's just not great for everything. 
    - I also had the privilege of writing the [Event Report](https://harthousechess.com/2022/12/13/2022-hart-house-holidays-open-attracts-record-breaking-crowd-of-212-players/), many thanks goes to John Upper from the Canadian Chess Federation for the amazing photos. 
- **answering tournament emails**
    - running this tournament meant that we had to monitor the tournament email for many questions that participants had. 
        - out of the ~100 or so that we received, some of the ones that stood out were people asking about (1) byes, (2) withdrawals, and (3) Unrated discounts. We're hopefully going to make it clearer for the Reading Week Open come Feb.  
- **preparing/distributing signage and posters**
    - Thanks to the work of my Co-Communications Exec Ahmed Khalf, we were able to make marketing posters and advertisements to the general community. I went out to a local print shop to make sure that we could print the posters - that was a fun trip. 
    - I also designed the [official flyer](https://github.com/victor-zheng-codes/Personal-Blog/blob/main/content/posts/post-files/holidays-open/holidays-open-2022.pdf) for the event, and distributed ~350 paper copies to our Club and local chess clubs in the GTCL. 
- **maintaining inventory**
    - The first task in maintaining inventory was in counting the number of chess sets and materials held by the Club. I did a count and found that we didn't have enough chess sets and clocks to run this tournament. Historically, we ask players to bring their own equipment, but this isn't how major tournaments run. It doesn't make sense for the Club to hold too many chess sets and clocks when our focus is on students. 
    - Annex Chess Club provided a lot of help by loaning out chess sets and clocks for this event. 
    - Other things that I did a full inventory on were scoresheets (both carbon-copy and non carbon-copy), pens (I bought another 360 pens), and board numbers.
        - board numbers in particular were very difficult to do because our previous board numbers only went up to 70. I decided to design board numbers for the Club using Inkscape, and this worked out. We bought some special cardstock holders that enabled the numbers to hold up. I also learned about cardstock and the weight of paper (heavier is better imo)
- **setting-up/taking down the tournament playing hall**
    - arriving early at 1 pm (5.5 hrs before rd 1) on Friday and being the last to leave the tournament hall on Sunday at 11:30 pm 7.5 hrs after rd 5) was fun (even with the CSC236 exam on the next day)
        - setting up the playing hall was a bigger task than I envisioned. Before the tournament, I met with Hart House Events to talk through the event logistics for chairs, tables, and rooms. I decided to book the East Common Room as well, in case we went way over our estimated 200 people. 
        - the biggest hassle for setting up was bringing the DGT boards and equipment that we have in our Club. This equipment takes forever to unpack and is super heavy. 


|![](https://raw.githubusercontent.com/victor-zheng-codes/Personal-Blog/main/content/posts/post-files/holidays-open/Alex-Ferreira.jpg)|
| :--: |
| <b>Alex Ferreira was the Tournament Director and has been the backbone of the tournament since its inception. </b>|


Some other things that I helped set up. 
- **determining budgeting and setting entry fees** (big shoutout to Crystal, our Treasurer for doing a fantastic job)
    - As a non-profit, 100% of our proceeds go to support our student members. In particular, equipment upgrades, in-house tournaments, welcome back events, the Canadian University Championship, and the PanAmerican University Championship.
- **ordering new merchandise**
    - Since I've had to purchase lots of merchandise for both XdHacks and the UofT Tennis Club, I'd like to think that I have a good grasp of where to find the best deal for merch. 
        - in Fall 2022, we were able to purchase custom toques, pens, hoodies, and t-shirts! We'd never been able to do that. 

|![](https://raw.githubusercontent.com/victor-zheng-codes/Personal-Blog/main/content/posts/post-files/holidays-open/my-colleagues.jpg)|
| :--: |
| <b>This was a team effort from the entire Hart House Chess Club Exec Board. Pictured are Tanner and Crystal. Shout out to Bowen and Ahmed as well :) </b>|


### Reflection
Overall, the tournament went really well, and from what I heard, we got a lot of positive feedback. I think there are some improvements to be made for the Reading Week Open in February, but I think overall, this year's holidays open was a great success. The Club's fundraising goals depended on this event, and we reached our goals. I am happy to be given the opportunity and also very happy that I was able to learn a lot from the event about event organizing, planning, and decision making. One of the biggest things I've learned is that a supportive place like Hart House really makes a difference. Having a place to host an event, having people able to help you navigate budgets, room bookings, registrations, and other logistical things makes it easier to let myself and the Chess Club focus on what we do best: running a chess tournament. 

|![](https://raw.githubusercontent.com/victor-zheng-codes/Personal-Blog/main/content/posts/post-files/holidays-open/HartHouse-view.jpg)|
| :--: |
| <b>I've realized the importance and possibilities that a place like Hart House brings. </b>|

Being a part of the event organizing structure has really been a fun ride. I'm looking forward to running more chess tournaments, and shaping the future of chess in Toronto (and Canada).

Photo Credits: John Upper, CFC