---
layout: page
title: campaign tech
tagline: my work on the warren campaign
description: 
---

I joined the Warren campaign in June 2020 as the first product manager, focusing on organizing technology. Much of what my team built was open sourced after the campaign, and you can find a good summary of that effort on [Wired](https://www.wired.com/story/elizabeth-warren-campaign-open-source-tech/) and [Medium](https://medium.com/@teamwarren/open-source-tools-from-the-warren-for-president-tech-team-f1f27d2c7551).

<br/>

<p align="center">
  <img src="../assets/images/warren.jpeg" alt="Warren Tech Team" width="600"/>
</p>

<br/>

---

### Switchboard: Organize Your Community

Switchboard was a tool for distributed organizing. It's my favorite of all the projects I worked on, and both the [front-end](https://github.com/Elizabeth-Warren/supportal-frontend) and [backend](https://github.com/Elizabeth-Warren/supportal-backend) are open source!

<br/>

<p align="center">
  <div class="responsive-youtube">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/FVrbVGFsK_s" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</p>

<br/>

When I first joined the campaign, I was told that several hundred thousand volunteer prospects had filled out a form online but had not yet heard back from the campaign. This was both urgent and inevitable: it was critical that we connected with supporters as soon as possible, but we didn't have the staff to organize everyone. To solve this, we needed to make everyone an organizer by empowering volunteers to connect with Warren supporters in their communities. Switchboard was our solution to that.

We sent our best volunteers to Switchboard, a web app where they could discover, connect, and keep track of supporters in their area. We replaced the traditional model, where an organizer has to cut lists of prospects for volunteers to call, with a simple algorithm that repeatedly assigned volunteers their ten closest contacts. Volunteers would call or text supporters and if they made a connection, they could sign the supporter up for an event and add them to their list for future contacts. 

The app was beautiful, simple, and easy to use. We made a passwordless login flow (we didn't want to be in the business of doing password resets!), and volunteers could shift supporters into [Mobilize](https://join.mobilize.us/) events directly from the app. I personally used Switchboard daily to recruit for debate watch parties, phone banks, and canvasses in my town. 300+ volunteers used Switchboard, and thousands of supporters got their first outreach from the campaign via Switchboard, and our volunteers loved it!

Collaborators: [@jjandoc](https://github.com/jjandoc), [@goldblatt](https://github.com/goldblatt), [@matteosb](https://github.com/matteosb), [@victoriaadams](https://twitter.com/victoriadams), [@higgycodes](https://twitter.com/higgyCodes), and many many more!

---

### Shifter: Never Miss a Volunteer Shift

Shifter made it possible to capture event signups wherever we wanted. With Shifter, we could collect event signups on our own front-ends and write them to [Mobilize](https://join.mobilize.us/) (our event management tool) using the Mobilize [API](https://github.com/mobilizeamerica/api). We created a mirror of our Mobilize events database that we synced periodically, writing new signups from our front-ends to Mobilize while refreshing our data to have the most recent event info from Mobilize. 

Shifter powered in-app event signups on Switchboard (above), as well as on our website. We built a beautiful personalized signup journey based on Shifter, where visitors could select how they wanted to help and we would recommend events based on their location (and the campaign's priorities in that location). Shifter also acted as a failsafe to capture and cache event signups when Mobilize went down.

<br/>

<p align="center">
  <a href="../assets/images/shifter.png"><img src="../assets/images/shifter.png" alt="Shift Yourself"/></a><br/>
  <i>Shifter on the /volunteer page. This page got 12.5k WAU and was responsible for 12% of all call and 15% of all canvassing signups.</i>
</p>

<br/>

A Shifter widget was integrated directly into the call script in ThruTalk. This meant that a volunteer calling to recruit for an event on the mass-contact calling tool could sign up the supporter they were calling for a Mobilize event directly from the ThruTalk call script. 

This is important because before Shifter, callers would mark the person they were calling as "interested in attending" in a survey question, relying on the supporter to remember to attend the event (!!!). With Shifter, the supporter received email reminders from Mobilize, and the success of our recruitment efforts could be tracked and measured. Shifter helped us capture thousands of volunteer shifts that would otherwise have been lost.

<br/>

<p align="center">
  <a href="../assets/images/shifter2.png"><img src="../assets/images/shifter2.png" alt="Shift Yourself"/></a>
</p>

<br/>

Collaborators:  [@goldblatt](https://github.com/goldblatt), [@jjandoc](https://github.com/jjandoc), [@victoriaadams](https://twitter.com/victoriadams), [@matteosb](https://github.com/matteosb), [@chipbetterley](https://www.linkedin.com/in/cbetterley) and many more.

---

### Iowa Caucus App

<br/>

<p align="center">
  <img src="../assets/images/caucus.png" alt="Caucus App"/>
</p>

<br/>


Our Iowa team wanted a mobile app to help precinct captains (~2500 Warren volunteers) navigate caucus math. The app was for internal campaign use only and had three major requirements: 

1. Get the caucus math right
2. Work offline
3. Send results of calculations back to the campaign

We put together a proposal for a design and a recommendation to try building this as a progressive web app with Vue, with the caveat that the technology was still new and would require the Iowa team to be an active participant in building and testing. This choice had some big benefits - there was no app store review process or separate packages to maintain, volunteers didn't have to remember Apple or Google passwords (a real issue), and once the app was pinned to the home screen, it looked and felt just like a native app. We wrote results to DynamoDB (S3 for pictures of paper caucus worksheets, which proved crucial) and then to a master spreadsheet where analysts compiled results. 

After some initial issues (service workers failed to update the app in certain scenarios, and we had to track down those users to clear their cache), our app and the accompanying support hotline worked well on caucus night, and even won us some delegates!

<br/>
<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr" align="center">Spoke to a Warren precinct captain. She told me at her site there was a mistake in the counting/math at first, but Warren camp has its own delegate math app. So she did math and showed folks in charge, helped save a delegate for Warren.<br><br>This is how these things work I guess! 1/</p>&mdash; Danielle Kurtzleben (@titonka) <a href="https://twitter.com/titonka/status/1224558023974313985?ref_src=twsrc%5Etfw">February 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br/>

<br/>
<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr">The Warren caucus app was the only one in the room that worked, so take from that what you will.</p>&mdash; Amanda C. (@MdmeAlbertine) <a href="https://twitter.com/MdmeAlbertine/status/1224530037489262592?ref_src=twsrc%5Etfw">February 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br/>

Caucuses are a [developer's nightmare](https://www.nytimes.com/2020/02/09/us/politics/iowa-democratic-caucuses.html), with niche requirements and little opportunity to test technology ahead of time. That said, we found our infrastructure held up remarkably well. We gave ourselves a generous timeline (~6mo) for the project, we built on extensive feedback from colleagues who had used apps in previous caucuses, and we incorporated failsafes like the support hotline to help catch and fix issues before the contest. You can browse the source code for our app [here](https://github.com/Elizabeth-Warren/iowa-caucus-app).

We were able to share the raw data we collected with the Iowa Democratic party to speed up results:

<br/>
<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr" align="center">Our campaign collected photos and other raw documentation of the results at hundreds of caucus locations as part of our internal reporting process. Today we will provide what we have to the Iowa Democratic Party to help ensure the integrity of their process.</p>&mdash; Roger Lau 劉煒 (@RogerLau) <a href="https://twitter.com/RogerLau/status/1224712792227401729?ref_src=twsrc%5Etfw">February 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br/>


Collaborators: [@jjandoc](https://github.com/jjandoc), [@goldblatt](https://github.com/goldblatt), [@benweissmann](https://benweissmann.com/), [@victoriaadams](https://twitter.com/victoriadams), [@charlotteeffect](https://twitter.com/charlotteeffect), and many others.

---

### Dialers, Hotlines, and other fun with telephony

I spent a lot of cycles on the campaign learning everything I could about telephony. This included researching the possibility of building our own dialer for massive call campaigns (we eventually decided [ThruTalk](https://www.thrutalk.io/)/Livevox was the most cost-effective option for us), finding ways to improve call connection rate with caller ID and whitelisting, and building call and text flows for various initiatives. Thanks to some clever ideas from [@benweissmann](https://benweissmann.com/) and a Twilio developer account, I once found myself "in charge" of a small army of Verizon phones that would all ring at the same time. I have zero regrets about the whole thing.

---

### More...

Our campaign tech team was a phenomenal group of individuals. To hear their stories, check out [this episode of DevTalk podcast](https://kerry.lothrop.de/devtalk-41/) we recorded with my friend Kerry Lothrop after the campaign, and [this wonderful post](https://medium.com/@susangoldblatt/tech-on-a-presidential-campaign-an-overview-9679d69b2109) by one of our engineers. You can find other campaign projects on the Team Warren [Github](https://github.com/Elizabeth-Warren).

<br/>
<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr">Several times during the campaign, the <a href="https://twitter.com/TeamWarren?ref_src=twsrc%5Etfw">@TeamWarren</a> tech team approached our NH team to ask: “How can I make your work easier? How can I simplify this process? What’s a pain point, and how can we help?” Whenever and wherever they could, they were there to help.</p>&mdash; Elice Rojas-Cruz (@elicejosselyn) <a href="https://twitter.com/elicejosselyn/status/1243560381555052550?ref_src=twsrc%5Etfw">March 27, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br/>
