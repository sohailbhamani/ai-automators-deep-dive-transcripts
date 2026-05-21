---
title: "How to Connect a Telegram Bot to Make.com (Beginner Guide)"
video_id: "8TMKfSDORAc"
youtube_url: "https://www.youtube.com/watch?v=8TMKfSDORAc"
publish_date: "2025-01-20"
duration: "5:22"
duration_seconds: 322
view_count: 46226
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_telegram_bot_connection
  
  How to create an AI agent with Telegram + Make.com: https://www.youtube.com/watch?v=juiWBu5m-Jg
  
  Chapters:
  0:00 - Introduction
  0:36 - Creating a Telegram Bot
  1:09 - Connecting the Bot to Make.com
  1:45 - Testing the Bot with a Channel
  3:08 - Testing the Bot with a Group
  4:39 - Troubleshooting and Next Steps
  
  In this tutorial, you'll learn how to create a Telegram bot and connect it to Make.com for instant automation. We'll guide you through the setup process, from creating a bot in Telegram and obtaining the necessary API token, to integrating it with Make.com to automate your workflows. You'll also discover how to configure an authorization filter to restrict access to specific channels or groups.
  
  By the end of the video, you'll understand how to:
  
  - Create a bot using Telegram's BotFather.
  - Integrate the bot with Make.com to trigger workflows automatically.
  - Set up and test the bot in both channels and groups.
  - Add custom authorization filters for enhanced control.
  - Troubleshoot common issues, such as using bots across multiple scenarios.

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Beginner"
audience:
  - "General"
entities:
  companies:
    []
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "com (Beginner Guide)

in this video I'm going to show you how to create a telegram bot in Telegram and then connect it to me"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "coding"
  - "make"
  - "tutorials"
  - "workflows"
---

# How to Connect a Telegram Bot to Make.com (Beginner Guide)

in this video I'm going to show you how to create a telegram bot in Telegram and then connect it to me.com via these instant triggers so every time you send a message to a Channel with this bot then it will automatically pick this up within me.com instantly and I'm going to show you how to set up this simple authorization filter so that only channels that you want will have access to your automations once you understand how to set up the connection with telegram then you can check out the AI agent video on our main channel so you can set up an AI assistant that has access to external tools such as research tools image tools and lots more so I've gone to telegram I'm going to go to contacts and you have to type in bot F then from there type new bot sorry I'll move this up a bit create new bot what are you going to call it just going to call this test make integration bot not very inventive after that you have to choose your username I'm just going to copy and paste in the exact same thing oh that's already taken test make integration to bot right okay that's done now you'll see that we have this HTTP a access token which you should store safely and securely and not give that to anybody else I will be deleting this pot after this video so what to do is then go into your make.com account type telegram go to show more and go all the way down to watch updates now select add on the right hand side you can add a new connection so copy and paste in this API token into here press save and then you just wait for that to run okay looks good press save I'll press okay now I'm going to click run once and just try and test the connection or sorry before I do that I need to add this to a Channel or add it to a group it's slightly different on the make.com site depending on which one you do so I'm going to start with a channel just going to call this channel testing make integration going to make it a private Channel at the top right go to view Channel info go to administrator and click add administrator then copy and paste in the bot name to that click okay and click save now we'll click run once I will wait for new data now I'll type test message and perfect it showed up fine now if that did not work for you one thing you can try is to go and add a new connection click add again and then try again this may be required if you have multiple scenarios that's using the same connection or is using the same web hook now next up what I'm going to do is every time I get a message I'm just going to respond to that same telegram chat with a response method just to acknowledge it this is just a test so I'm going to send a test message the chat ID here is channel post sender chat and ID so let's go to that all the way to channel post sender chat and ID then text just going to type in message received and click okay perfect press run once type test message again now it's responded with message received now let's go back here to this sender chat copy out this ID and what we're going to do is add in this authorization filter typed in authorized so if the channel post sender chat and ID is equal to that so here we're hardcoding in the ID from this particular Channel if somebody else adds this spot to another channel it's going to get blocked here I'll press okay now I'm going to select run ones perfect so we see what the result of that is the cender chat was that so it worked the data we get from telegram is slightly different if it's in channels compared to if it's in groups so now I'm going to create a group within Telegram and then update this scenario to work for a group I'm now going to create a group I'm going to call that testing make integration group not being very inventive I'm going to go to view group info add member I've searched this bot I've added in the name of this bot I'm going to press add so I'll press add I'll press run once click run once and wait for new data and now nothing is happening within this bot and that is because I have not added this bot as as an admin for this account so I'll go to manage group add administrators and then select that bot then click save and close now I'll go again click run once and test five perfect so we got a response we have message chat now the difference here is that it's a slightly different data structure when you're messaging in a group you have the data within this message as opposed to within the channel post so in the authorized filter instead of send or chat ID you'll go to message Chat ID and then the chat ID will be that message Chat ID and then when you're sending a message back to telegram you have this message Chat ID from there okay we'll just run this so that it now runs immediately as the data arrives so we're not waiting to press run once every time for this so right test six and now we have a response message received there may be some shortcomings with the telegram integration if you're having issues such as if you're using the same bot across multiple chats and you want to trigger multiple scenarios if you're having issues with that then just try to create a separate bot and create a new connection within Telegram in your different scenario if you're having issues with your connection go to add and then click add again add in your token that you got from that bot F chat and then try to run the connection again now that you have a telegram bot set up now you can actually do something with it such as bring AI into the Mi so check out the link in the description to our AI agent video using me.com and open AI assistance if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
