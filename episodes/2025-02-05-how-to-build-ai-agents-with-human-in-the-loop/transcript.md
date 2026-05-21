---
title: "How to Build AI Agents with Human-In-The-Loop"
video_id: "vyuenkJQpX8"
youtube_url: "https://www.youtube.com/watch?v=vyuenkJQpX8"
publish_date: "2025-02-05"
duration: "7:22"
duration_seconds: 442
view_count: 3034
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our templates, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_agent_human_in_the_loop_safeguard
  
  https://www.youtube.com/watch?v=juiWBu5m-Jg
  https://www.youtube.com/watch?v=8TMKfSDORAc
  
  Chapters:
  0:00 - Introduction
  1:10 - Demonstration
  2:38 - Safeguard Workflow Explained
  6:15 - When to use this
  
  AI agents are transforming workflows, but they come with risks—like unintended actions or dangerous feedback loops. In this video, I introduce a powerful AI agent human-in-the-loop technique, which we're calling an Agent Safeguard, to ensure human oversight in critical actions, such as publishing to social media or sending emails to client.
  
  We demonstrate how to implement this safeguard using Make.com and OpenAI, interacting with the agent through Telegram. You’ll learn how to enable approval workflows that prevent errors by requiring a human to verify key actions before they execute.
  
  The workflow includes features like:
  Researching topics using AI.
  Generating images with AI tools.
  Drafting and publishing Facebook posts, while integrating a safeguard to ensure intentionality.
  
  Through a step-by-step breakdown, I show how the approval mechanism stores requests, sends secure links for validation via Telegram, and prevents unauthorized actions. This approach guarantees reliability and mitigates risks in your AI automations.

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Agents"
difficulty: "Intermediate"
audience:
  - "Engineers"
entities:
  companies:
    - "OpenAI"
    - "Perplexity"
  people:
    []
  products:
    - "Perplexity"
    - "Make"
  models:
    - "Flux"
concepts:
  []
summary:
  - "com and open AI assistance on this channel we're interacting with this agent via Telegram we can ask this bot to research topics generate images and publish to Facebook the make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "coding"
  - "make"
  - "meta"
  - "openai"
  - "perplexity"
  - "prompting"
  - "tutorials"
  - "workflows"
---

# How to Build AI Agents with Human-In-The-Loop

everybody's talking about AI agents right now but they come with a risk and that is they can make mistakes and do things like spam your social media send out email blast by mistake or just end up in these really dangerous feedback loops I'm going to show you a vital technique that will make your agents way more reliable we're calling this an agent Safeguard this technique absolutely guarantees that your approval will be sought before any key actions I recently covered how to build an AI agent using make.com and open AI assistance on this channel we're interacting with this agent via Telegram we can ask this bot to research topics generate images and publish to Facebook the make.com scenario is surprisingly simple and within this agent we're specifying tools such as this perplexity scenario this image tool scenario and this pulse into Facebook scenario the AI agent from there is able to figure out what tool to call and when but it comes with a risk it could post to Facebook by mistake or without our approval in this video I'm going to show you how we add an agent Safeguard to this Facebook posting tool to guarantee that it's going to seek our approval before or pulse unit by the way if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates including this one I'm going to start with a demo and then after that I'll go through the entire process for how you can use this technique in your own agents so I'm asking this to research the topic open A3 mini and draft a Facebook po as we're waiting for that here it's going to hit our main make.com scenario it's going to go to the openi assistant and we're expecting this going to call perplexity via our research tool and this is just a simple scenario within me.com with this webook again check out the link in the description if you want a bit more information about how they work okay this is the response it's pretty concise looks good enough for our testing now I'll say looks good generate an image and now as that's happening I'm expecting that it's going to call this AI image tool behind the scenes which is this micro template that we've set up within make.com we're using file. to generate fluxor images there we have an image generated it looks pretty cool and futuristic it's not massively relevant to this content so we could have a back and forth conversation to get that right and also update the prompting within our openai assistant for this exact use case but to demonstrate this concept I'm going to keep going with this and I'll just ask it to post this to Facebook now we have this interesting new message which is this is the agent Safeguard please click on this link to publish this post to Facebook and then it shows us the post text we can click on this link and it opens up the image link so once we click on this link and now we have a pretty much instant response to say that this is the agent safe card your pulse has been published at Facebook so let's have a look at Facebook perfect there we see the PSE has been published we have the text as we wanted it and the image that was generated by flux one let's break down what happened there once we got to the stage where the assistant was ready to post to Facebook it called the new version of our Facebook posting tool which looks like this within me.com and remember in our main scenario within the main openai assistant we just connected this Facebook posting tool via web hook to this scenario and this is not posting anything to Facebook what it's doing is it's saving an approval key within a data store in make.com and then behind the agent back it's effectively just sending a direct message to the telegram bot and we've coded that here this is the agent Safeguard please click on this link to publish the post to Facebook the openai assistant is completely unaware of this link that's been sent to our telegram bot so it's impossible for the open a assistant to trigger this link and therefore they cannot post a Facebook without us clicking on this link this is way safer than trying to build in approval into the open a assistant prompts because it's still very possible that the agent can make mistakes and misinterpret your directions and when you're sending this telegram bot make sure to disable link previews at the very end because otherwise telegram might visit that link and then trigger the creation of the poll on Facebook and by the way in this workflow if you do not click this link within 2 hours it expires and will not work in the future of course you can adjust that however you want how does this work when the open ey assistant requests to post to Facebook it hits this web hook it goes to this tool which is this set multiple variables we're going to create this approval key and it's creating this hash so what it's doing is it's getting a random number mixing a Tim stamp has a secret key in here you can change that to whatever you want and then from that we get this really long approval key we're then saving that approval key in a data store and within this data store we have the approval ID the request type which is Facebook so this is one data store that could work for lots of different social networks across different automations we have the status which is published in this case and the text content and the image link this is all stored within this data store and ready for the user to click the link within telegram we then send this telegram bot message it's identifying itself as the agent Safeguard please click on this link and it's the wook URL and the approval key the end result of this is that we'll have this link sent to us that we can click for approval when we click on that link that directly triggers this second part of the scenario and this completely bypasses the openai assistant so there's no possibility of mistakes or confusion because we're triggering it directly it's going to get the approval ID that was embedded in the link so how do we do that we get this URL within this web hook we can copy this web hook to our clipboard as you see there that's the web hook URL that we use to hit the scenario but we've added in this approval ID at the end and added in our unique approval key that's exactly what you see here you have the approval URL and we're constructing this approval ID at the very end and adding in the approval key that we generated earlier on here we're trying to find that approval ID within the data store such as as you see here and it's only going to return it if the status is open and if the request type is Facebook if that had already been published before they will not pick it up from there we have a bunch of routers and responses to telegram but these are only to handle edge cases such as if the ID does not exist if it cannot find anything in the data store and if the link has expired the main thing you should be interested in is this post to Facebook if there is not an image link it will create a Facebook text post it will update the data store to mark it as publish so it'll Mark that particular record as published as you see here this will then send a direct response to telegram such as here where we see the post has been published to Facebook once the openingi assistant call the face of posting tool that sends a direct secret approval link to your telegram Channel and then as a separate action entirely the user clicks on the approval link it goes to the second part of this Facebook posting tool and then that directly sends a telegram response this is effectively a hardcoded workflow but our open Assistant decides when to start triggering it but it does not have the full capability to do the final publishing so if you're building an AI agent and if there are certain parts of the workflow where you just absolutely cannot accept blunders or mistakes in certain actions such as posst to an email list or to your Facebook account or sending an email to a client then this is an extremely reliable method where you can guarantee a human in the loop approval will be required for certain actions and you do not need to use data stores for this you could also use an air table base or any other type of external database and if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where you'll get access to all of our automations including the one in this video you can get direct support from us via our live workshops and through our active discussion boards
