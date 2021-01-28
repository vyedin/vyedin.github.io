---
layout: page
title: campaigh tech
tagline: my work on the warren campaign
description: 
---

[...]. Much of our tech was open sourced after the campaign, and you can find a good summary of that effort on Wired and [Medium](https://medium.com/@teamwarren/open-source-tools-from-the-warren-for-president-tech-team-f1f27d2c7551).

<br/>

<p align="center">
  <a href="https://twitter.com/elicejosselyn/status/1243560381555052550"><img src="../assets/images/warren.jpeg" alt="Warren Tech Team" width="600"/></a>
</p>

<br/>

Our campaign tech team was a phenomenal group of individuals. To hear their stories, check out [this episode of DevTalk podcast](https://kerry.lothrop.de/devtalk-41/) we recorded with my friend Kerry Lothrop after the campaign, and [this wonderful post](https://medium.com/@susangoldblatt/tech-on-a-presidential-campaign-an-overview-9679d69b2109) by one of our engineers. You can find other campaign projects on the Team Warren [Github](https://github.com/Elizabeth-Warren).

<br/>

<p align="center">
<img src="../assets/images/tweet1.png" alt="Tweet" width="400"/>
</p>

<br/>

---

### Switchboard: Organize Your Community

Switchboard was a tool for distributed organizing. It's my favorite of all the projects I worked on, and both the [front-end](https://github.com/Elizabeth-Warren/supportal-frontend) and [backend](https://github.com/Elizabeth-Warren/supportal-backend) are open source!

<br/>

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/FVrbVGFsK_s" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

<br/>

When I first joined the campaign, I was told we had several hundred thousand volunteer leads who had filled out an interest form online but had not yet heard back from an organizer. This was both urgent and inevitable: it was critical that we connected with supporters as soon as possible and put them to work, but we didn't have the staff we needed in every state to organize everyone. To solve this, we needed to make everyone an organizer by empowering volunteers to connect with other Warren supporters in their communities. Switchboard was our solution to that.

We sent our best and most trusted volunteers to Switchboard, a web app where they could discover, connect, and keep track of prospects in their area. We replaced the traditional model, where an organizer has to cut lists of prospects for volunteers to call, with a simple algorithm that repeatedly assigned volunteers their ten closest contacts. Volunteers would call or text their prospects and if they made a connection, they could sign the prospect up for an event and add them to their list for future contacts. 

The app was beautiful, simple, and easy to use. We used a passwordless login flow (we didn't want to be in the business of doing password resets!), and volunteers could shift their prospects into Mobilize America events directly from the app. I personally used Switchboard almost daily to recruit for debate watch parties, phone banks, and canvasses in my town. Thousands of volunteer prospects got their first outreach from the campaign via Switchboard, and our volunteers loved it!

Collaborators: [@jjandoc](https://github.com/jjandoc), [@goldblatt](https://github.com/goldblatt), [@matteosb](https://github.com/matteosb), [@victoriaadams](https://twitter.com/victoriadams) and many many more!

---

### Shifter: Never Miss a Volunteer Shift



<br/>

<p align="center">

</p>

<br/>

Collaborators: 

---

### Iowa Caucus App

<br/>

<p align="center">
<img src="../assets/images/caucus1.png" alt="Caucus App"/><img src="../assets/images/caucus2.png" alt="Caucus App"/>
</p>

<br/>


Our Iowa team wanted a mobile app to help precinct captains (~2500 Warren volunteers) navigate caucus math. The app was for internal campaign use only and had three major requirements: 

1. Get the caucus math right
2. Work offline
3. Send results of calculations back to the campaign

We put together a proposal for a design and a recommendation to try building this as a progressive web app, with the caveat that the technology was still new and would require the Iowa team to be an active participant in building and testing. This choice had some big benefits - there was no app store review process or separate packages to maintain, volunteers didn't have to remember Apple or Google passwords (a real issue), and once the app was pinned to the home screen, it looked and felt just like a native app. We wrote results to DynamoDB (S3 for pictures of paper caucus worksheets, which proved crucial) and then to a master spreadsheet where analysts compiled results. 

After some initial issues (service workers failed to update the app in certain scenarios, and we had to track down those users to clear their cache), our app and the accompanying support hotline worked well on caucus night, and even won us some delegates!

<br/>

<p align="center">
<a href="https://twitter.com/RogerLau/status/1224712792227401729"><img src="../assets/images/tweet3.png" alt="Tweet" width="400"/></a> 
</p>

<br/>

Caucuses are a developer's nightmare, with niche requirements and little opportunity to test technology ahead of time (as we saw with the official Iowa caucus reporting app). That said, we found our infrastructure held up remarkably well. We gave ourselves a generous timeline (~6mo) for the project, we built on extensive feedback from colleagues who had used apps in previous caucuses, and we incorporated failsafes like the support hotline to help catch and fix issues before the contest.

In the end, we were able to share our raw data with the Iowa Democratic party to speed up results:

<br/>

<p align="center">
  <a href="https://twitter.com/titonka/status/1224558023974313985"><img src="../assets/images/tweet2.png" alt="Tweet" width="400"/></a>
</p>

<br/>

Collaborators: 

---

### Dialers, Hotlines, and other fun with telephony



<br/>

<p align="center">

</p>

<br/>

Collaborators: 

