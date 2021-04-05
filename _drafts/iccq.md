---
layout: post
title: "How We Organized the First ICCQ"
date: 2021-03-15
place: Moscow, Russia
tags: science
description: |
  We organized the first scientific conference this year
  and it was not so easy; here is a summary of our
  experience, which may help you do the same.
keywords:
  - iccq
  - ieee conference
  - conference
  - how to organize conference
  - conference
image: /images/2021/03/
jb_picture:
  caption:
---

First, let me clarify what kind of conference we are talking about. 
There are two types of them:
[professional](https://en.wikipedia.org/wiki/Professional_conference)
and
[academic](https://en.wikipedia.org/wiki/Academic_conference).
The difference is [huge](https://redmonk.com/kfitzpatrick/2019/01/29/tech-industry-events-vs-academic-conferences/).
My understanding is that professional conferences are for _practitioners_, 
while academic ones are for _researchers_.
ICCQ, which we organized this year, is an academic one.
I haven't had any expertise in organizing such things, and had to go through it all for the first time.
Here is a more or less detailed description of the journey.
Feel free to repeat it for yourself and make a similar conference.

<!--more-->

{% jb_picture_body %}

**Idea**<br/>
As I said in [my opening speech](https://www.youtube.com/watch?v=65baOBHeVMI), 
the purpose of a new event was to 
help Russian computer society better connect with their worldwide
colleagues. Besides having a good intention I knew where to get a reliable sponsor.
The rest was just implementation.

**Name**<br/>
There are many options to chose from, but it seemed
that the de-facto standard was a few letters, all-caps, like
[SPLASH](https://conf.researchr.org/series/splash), 
[ICSE](http://www.icse-conferences.org/), 
[PLDI](https://pldi21.sigplan.org/), 
[PLOP](https://www.hillside.net/plop/2020/), 
[etc.](https://www.guide2research.com/topconf/) 
There are expections like [EuroSys](https://2021.eurosys.org/)
or [EuroS&P](https://www.ieee-security.org/TC/EuroSP2021/) but
this naming convention is much less popular.
We picked ICCQ, which was not yet actively used in Google and the website
with `.ru` extension was available. Initially, we aimed for `.org`,
but since the event is supposed to be always Russia-based, `.ru`
seemed to be a perfect choice.

**Subject**<br/>
Many conferences aim at many topics, maybe in order to 
attract more papers. We decided to behave completely differently:
we picked a single topic of _code quality_ and decided to reject all papers, 
which would not be relevant to it.
We didn't even publish the list of topics, like many other
events do. We just said that we are about code quality and 
how to make it better.

**Organizers**<br/>
[Organizers](https://www.iccq.ru/2021.html#organizers) were the people who I needed most of all.
They were not supposed to write papers or make speeches, but without
them I would not be able to make the conference. Not all of them
stayed with us for a whole year, some of them joined and quick, some
moved to the PC later.

**Dates**<br/>
We picked a date of the event about eight months ahead of us
and very soon realized that it was a mistake: too close.
It should have been _at least_ one year ahead of us. We had to re-schedule.
We also set three important dates: 
1) "submission deadline"---four months before the event, 
2) "author notification"---two months after the submission,
3) "camera-ready copies"---one month after author notification.
This timeline seems doable, but pretty tight. Next year we'll give
our PC more time for reviews: two months is definitely not enough
for a bigger event.

**Website**<br/>
We made it on [GitHub Pages](https://pages.github.com/) with [Jekyll](https://jekyllrb.com/):
the sources of our website are [here](https://github.com/yegor256/iccq.github.io).
We knew that most conferences use some hosted site builders, like
[conf.researchr.org](https://conf.researchr.org/), but we decided to swim against the
current and build the site the way we believed was right. No surprise,
we've got many of complaints about that from people who we were trying to 
invite into our team, as partners or co-organizers. They were all starting
the discussion with "You need to do you website right." Nevertheless,
the original design of the website survived. By the way, some of the content
we copied with some modifications from [SPLASH(https://conf.researchr.org/series/splash) website.

**Host**<br/>
We were lucky to have a very famous Russian University on our side
right from the start: [HSE](https://www.hse.ru/). We knew people from there
and they were not against hosting the event and putting their name on our website.

**Venue**<br/>
HSE also were not against hosting the event physically on premise.
The event was not going to be big (up to 100 people attending).
We agreed with HSE that they would give us a big class room on Saturday. 
They didn't mind.

**Partners**<br/>
We figured that in addition to HSE it would be good to have a few other sponsors,
mostly to make us look more serious and reputable (as much as it's possible
for a young conference). We had good contact with a few Russian
education organizations and they all agreed: 
[MIPT](https://mipt.ru/english/), 
[MSU](https://www.msu.ru/), and 
[ISP RAS](https://www.ispras.ru/en/). 
We contacted industry companies, and they also agreed:
[SberCloud](https://sbercloud.ru/),
[Yandex](https://yandex.com/company/),
and
[Kaspersky](https://www.kaspersky.com/).
And we also contacted two biggest non-for-profit Russian media organizations:
[RUSSOFT](https://russoft.org/en/)
and
[SECR](https://2021.secrus.org/?lang=en).
They also agreed.
Of course, it was much harder than it sounds. Some of organizations didn't reply
to us, some of them rejected. It was a long process that took about two months
of negotiations. We even created [this web page](https://www.iccq.ru/partnership.html) 
to explain them why we want them to join us.

**PC**<br/>
This was one of the most challenging parts: how to get together a Program Committee
of people who would review the papers and decide which of them deserve to be
published. First, we invited a few people who we personally knew. Then, we decided to try to keep
the PC as diverse as possible in terms of country of origin. We didn't want to 
see there only people living in Russia. We wanted to build a truly international
PC and also truly professional. Because of this plan, the only option for us was cold calling---we didn't
know so many people from different places. 
We've sent about 400 invitation emails to people who participated in similar conferences worldwide.
As you can see on the website: [30 of them](https://www.iccq.ru/2021.html#pc) 
agreed to join us.

**IEEE**<br/>
This was the biggest challenge: to get a 
[technical sponsorship](https://www.computer.org/conferences/organize-a-conference/sponsorship-options) 
from IEEE.
Our friends from IEEE Russia Section C Chapter helped us, and
[we got it](https://conferences.ieee.org/conferences_events/conferences/conferencedetails/51190).
If you want to know more details about this step, [tg me](https://t.me/yegor256), 
I will try to explain.
It took about three weeks, and they accepted our request.
They gave us their own "Record Number" and ISBN for the Proceedings.

**Keynote**<br/>
We decided that a good conference must have a good keynote speaker---it is someone
who doesn't write a paper and doesn't go through a normal review process.
It must be someone known by the community, in order to make the conference
even more interesting for attendees. We decided to invite Anders Møller. We personally
knew him by [his book](https://cs.au.dk/~amoeller/spa/spa.pdf) recently published online.
We invited and he agreed! [His speech](https://www.youtube.com/watch?v=oDdrzXkInnA) 
was definitely <del>one of</del> the best at the conference.

**Twitter**<br/>
We decided to be present at just one social network, since it is the most 
popular among tech people (proof?) and the easiest to maintain:
[@iccq_ru](https://twitter.com/intent/follow?screen_name=iccq_ru). We
tried to post there what's going on with the preparation of the event, almost
every week. Some of our authors and PC members followed us.

**Registration**<br/>
We thought that the event would be on-site, in the class room of HSE. That's why
we created a page at [Meetup](https://www.meetup.com/iccq-ru/events/273816665/) and
collected over 170 registrations. Unfortunately, due to COVID-19, we had to make the
conference fully online.

**Steering**<br/>
We didn't know what exactly it was for, but we saw other events doing this.
we formed a Steering Committee of two people from two most important partners of ours:
[Zhang Yuxin](https://www.huaweicloud.com/intl/en-us/news/building-a-smart-future-with-full-stack-innovation-for-the-cloud.html), 
the CTO of Huawei Cloud and 
[Yevgeny Kolbin](https://www.sberbank.ru/en/press_center/all/article?newsID=ef3e1c1b-fc7f-4eb5-9d36-db23e2ed42fc&blockID=1539&regionID=77&lang=en&type=NEWS), 
the CEO of SberCloud.

**EasyChair**<br/>
There has to be some website to collect papers from authors. We decided to use
[EasyChair](https://www.easychair.org),
since it's pretty popular and not so expensive as some others.

**CFP**<br/>
When everything was ready, there was a question (the biggest one!): how to 
collect the papers from authors. We had to find a way to promote the conference so that
researchers decide to submit their work results to us. Aside from using our 
own existing Twitter/Facebook/Telegram channels, there were two options: 
call-for-papers (CFP) distribution and paid ads. 
We've made a [PDF](https://latexonline.cc/compile?git=https%3A%2F%2Fgithub.com%2Fyegor256%2Ficcq.github.io&target=cfp%2F2021%2Fcfp.tex&command=pdflatex&trackId=1617526368363) and 
[TXT](https://raw.githubusercontent.com/yegor256/iccq.github.io/master/cfp/2021/cfp.txt) versions 
of it and then posted to a few places: 
[WikiCFP](http://www.wikicfp.com/cfp/servlet/event.showcfp?eventid=112792),
[call4paper](https://www.call4paper.com/detail/event/PGNZHDXH27553174),
[AllConferenceCfpAlerts](https://allconferencecfpalerts.com/cfp/view.php?eno=22113),
[SEWORLD](https://listserv.acm.org/scripts/wa-acmlpx.exe?A2=ind2009&L=SEWORLD&P=R5608),
[types-announce](http://lists.seas.upenn.edu/pipermail/types-announce/2020/009182.html),
and
[DBWORLD](https://research.cs.wisc.edu/dbworld/messages/2020-09/1600852058.html).

**Ads**<br/>
We were lucky enough to have a decent budget for paid ads. We placed
our banners into 
[Communications of the ACM](https://cacm.acm.org/)
and 
[IEEE Computer](https://ieeexplore.ieee.org/document/9187479).

**Waiting**<br/>
We were waiting for a few months with almost no result. Some papers
were coming but their quality was obviously pretty low. We were
very nervous, to say the least. We didn't have any backup plan.
If there would be no good papers, I was prepared to call it all off
and admit failure.

**Extension**<br/>
When the deadline arrived, it was obvious that we didn't manage to
collect enough papers. We decided to give our authors another two weeks:
the deadline was extended till Dec 18.
It was worth it! A few very good papers arrived last and we phew-ed.

**Invited Talk**<br/>
To make the conference even stronger, we decided to invite someone
who we knew and respected. Just like we did with the Keynote talk, 
but this time with a full paper to publish too.
We invited Veselin Raychev, the CTO of [Snyk](https://snyk.io/). He wrote a survey
paper for us and we promised him that it will be fast-track reviewed.
Without such a promise he would probably not submit it to us, since
we are too young and small, but since we guaranteed publication, he agreed.
This is how, I believe, invited talks work.

**Desk Reject**<br/>
We decided to reject six papers before even sending them to the PC
for review. The most popular reason was: out of scope. Some papers
were about something completely irrelevant. One paper was even auto-generated,
with some very funny typos inside.

**Bidding**<br/>
We missed this step, because I didn't know about it. I would actually
skip it again, in the next conference, but most event do the bidding,
as I've been told. They ask all PC members to go through the list of
all submissions and pick those they want to review. Probably, they will
pay attention to the subject, maybe to the quality of paper. In the end,
the distribution of papers among PC members will not be randomized.
I don't like this.

**Reviews**<br/>
I went to EasyChair dashboard and clicked "assign papers to reviewers
automatically" and the system did it for me. We've had 17 papers and
30 reviewers. I configured EasyChair to assign at least three reviewers
for each paper. Do the math: most reviewers got two papers, while some of them
just one. However, only about ten reviewers provided their reviews more or
less instantly. Others were not giving us anything and about ten of them
were not even answering my email reminders. We had just seven weeks between
the submission deadline (remember, we extended it by two weeks) and the
day of the final decision. We were not sure that we would be able 
to collect all necessary reviews and that's why we started asking most active reviewers
to review more than just two papers. Surprisingly, most of them agreed to help
us. The bottom line, we managed to collect at least three reviews per
paper, while some papers got five reviews. Because most reviewers performed
their duties on time. Only three reviewers never provided us anything,
without any explanation. 10%. Is is how it should be?

**Accept**<br/>
This was a very tough moment: all papers are ranked and we had to pick some number
of them for the final publication. The question was: how many out of total 17?
Having a conference with a small number of articles is probably not a good
indicator of our work result. On the other hand, publishing something that
was explicitly rejected by reviewers would be at least unfair to other
authors and to reviewers. We had a very intense discussion inside and decided
to accept just six papers. Why six? Because the average rank of each of them
was positive. All papers with negative ranks were rejected.

**Copyright Transfer**<br/>
In order to publish our papers in IEEE Xplore, which is very important for
all authors, we had to transfer the ownership of all texts to IEEE: this is 
the requirement of IEEE. We build a small online form for that and asked
all accepted authors to fill it up. They did.

**YouTube**<br/>
I created a new YouTube channel, verified it, and created a new live
stream.

**Agenda**<br/>
We put all talks on the timeline and published conference agenda.
Then I created Google Calendar events for all sessions and invited
all speakers to their events. I also scheduled a Zoom meeting
for the day of the event and shared the link via all Google Calendar
events.

**Welcome Notes**<br/>
We asked our Steering Committee Chair and Program Committee Chair 
to write short one page welcome notes. They did. I also wrote mine,
on behalf of Organizers.

**Final PDFs**<br/>
We asked all accepted authors to send us so-called "camera-ready copies,"
which were basically their original papers, but formatted exactly 
according to our requirements. Lucky for us, all authors were using
LaTeX we just gave them a few configuration lines for the sources
and all papers look very similar, formatting wise.

**Proceedings**<br/>
Then, we had to design the book, binding together all welcome notes
and papers. I did it myself this time and you can see the sources here.

**Xplore**<br/>
Then, we packaged the entire ZIP archive and 
[uploaded](https://mft.ieee.org/conferences_events/ConfPubFileUploadUI/)
to IEEE. We didn't get any response back. Just crossed fingers
and started waiting.

{% badge https://www.iccq.ru/images/2021/proceedings.png 150 %}

**Prints**<br/>
We found a printing company here in Moscow and ordered them to print
us 100 copies of the proceedings, 
in B5 format (100g/m paper, mate cover). We paid around $10 per a copy
and it took about a week. By the way, we were explicitly told by
IEEE that we are not allowed to sell our Proceedings anyhow or even 
give them away for free, unless it only for PC members, authors,
and people closely related to the organization of the event. That's
why we printed such a limited number of copies.

**Zoom**<br/>
On the day of the event, we started our planned Zoom meeting and
connected it to YouTube live stream. I clicked "Record" and in six hours
there was a 2Gb video file with all presentations.

**Video Publishing**<br/>
I asked a friend of mine to edit this large video file, cutting it into 11
pieces: three short welcome speeches, one 45-minutes keynote, one invited talk,
and six half-hour sessions. Then, I published 
[all 11 files](https://www.youtube.com/playlist?list=PLsFvzjUuF8yr-2nCkuw_4lRrBv9mReznb) 
to YouTube. 
I also had to create their front images and some text descriptions.

**Gifts**<br/>
We packaged our Proceedings in customly made boxes together with
small chocolate bars, ICCQ stickers, and tourist books about Moscow.
We sent them to each author, each PC member, and each partner (about 60 boxes). 
What's left will be used during the year as promotional materials
to advertise our future events and invite new PC members and authors.

Done.

