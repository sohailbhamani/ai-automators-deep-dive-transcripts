---
title: "How to Automate Social Media for All Your Brands in One Place!"
video_id: "om6KpSzTTlc"
youtube_url: "https://www.youtube.com/watch?v=om6KpSzTTlc"
publish_date: "2024-12-13"
duration: "4:57"
duration_seconds: 297
view_count: 670
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_social_media_multiple_brands
  
  Our original social media blueprint: https://www.youtube.com/watch?v=00qppWuIW-g
  
  Let’s say you’re working with an automation such our social media blueprint, but you want the scenario to work for multiple brands.
  
  The issue is that these modules are connected to a single social media account. How do we get around that? Cloning the scenario and adding filters to your starting Airtable trigger is the easiest approach to this.
  
  In this video, we’ll walk you through how to adapt our social media automation system to work with multiple brands and their respective social media accounts, all within one Airtable base. Follow along as I break down the process step by step!

yt_tags:
  []


# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "General"
entities:
  companies:
    - "Apple"
    - "Slack"
    - "Twitter"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "# How to Automate Social Media for All Your Brands in One Place"
keywords:
  - "ai-agents"
  - "ai-news"
  - "apple"
  - "frameworks"
  - "make"
  - "meta"
  - "slack"
  - "tutorials"
  - "twitter"
  - "workflows"
---

# How to Automate Social Media for All Your Brands in One Place!

in this video I'm going to explain how to create a social media system that can handle multiple Brands and the social media accounts of each of those respective brands in this automation we're going to be using the social media blueprint that we have on our main channel in this case it's listening out for messages on a private slack Channel where you can just pass in interest in news items and blog pulse and this automation then scrapes that and then comes up with relevant pulse for each of the social networks all of that information then goes into an air table base including the updates and a generated image which you can then edit or replace depending on what you want and then when it's ready you click ready to publish and when this automation runs it'll pulse those to the relevant social networks that all works well and good but the problem is if you have a client or if you are managing multiple social media accounts so multiple Brands and each of the brands has a bunch of social media accounts then you need to adapt this process to suit that but the good news is it's actually quite easy to do so so for the moment I've just added in some example URLs just to illustrate this concept a bit and I'm going to move all of those to ready to publish we have not yet set up this multi-brand process but I need to explain a little bit just before I do that which is that we have this URL status and date set up here we do not actually have the Facebook pulse and text populated in all cases here but this is just for test data just is just to explain how you do this so at the moment the second and fourth rows here are marked as to be published today so this is today's date 4th of December at the start start of this scenario the trigger here it's looking out for statuses that are marked as ready to publish and where the date is before tomorrow so this will only pick up relevant ones it will ignore anything in the future so let's just test this out what happens if we click run ones and it comes up with this best Apple TV shows which is the second one so that's working as expected now let's say that we want to make this multibrand what we do is we insert left and we can then create a single select and we're going to call this brand and I'm going to add some options let's just call this brand one and brand 2 then for each of the polls that you create you need to make sure that you've actually selected a brand brand one and brand two and then you clone this scenario but before you do that we need to add a new filter to the formula so this will be the first brand so the scenario of the first brand and each of the modules the Facebook Twitter Instagram each of these modules will be connected to the accounts relevant to that brand only and then within this formula we just add in a new section which is let's go back here this is called brand so where brand is equal to is equal to Brand one and we'll press okay we'll copy that and we press okay we'll press okay now L what happens if we press run one oh I realized I included this within the brackets here it should be after this okay that should work press okay now what happens if we click run once okay nothing has come back and that's because if you look at the dates here the only stories that are scheduled to be posted today is for brand 2 what happens if we changes to we change this one to Brand one and if we run that then perfect it picks up that relevant one that means that when that's picked up it will go to this scenario and then at the very end here it will mark this as published and then that will not be picked up again so then you just go through this create the connections relevant for each of the social networks so we'll go back to the scenarios and then I'm going to just click clone on the right and then I'm going to change this to Brand two click save perfect and then the only difference between here is to go back into this and then change that formula whoops I'll change that formula to Brand two press save and from there I'll run that and see what shows up which is this one perfect so I'll go back to my first scenario and change that back to Brand one again so there we go we have the brand two scenario here and that's down as brand two perfect and brand one formula of brand one in this case we're we're already filtering by these other fields if you were just filtering by the brand field by itself you just get rid of all of those and just filter by that and then from there you can then schedule each of these scenarios to run at whatever time you want you could schedule them to run multiple times per day you know certain days of the week you could run at regular intervals every few hours for example so you can run this get this to run every 3 hours between a certain time of day on certain days of the week so that's how you configure the timing for exactly when you want these to run and very importantly if you only want it to pick up one record at a time make sure that this is set as limit to one because if you set this as limit to 10 then it could pull 10 stories to each of these social networks at once which would be quite spammy of course when you're ready to go you link these modules back together and then configure each of the social networks as you want and if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where you can get access to all of our automation blueprints as well as courses and weekly workshops
