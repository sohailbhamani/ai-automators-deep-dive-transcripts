---
title: "Use This to Instantly Swap AI Models in Make (FREE Options!)"
video_id: "EsGniZ7Sl8k"
youtube_url: "https://www.youtube.com/watch?v=EsGniZ7Sl8k"
publish_date: "2024-12-17"
duration: "6:36"
duration_seconds: 396
view_count: 1311
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_open_router_connection
  
  Note: Our video to convert existing blueprints to use OpenRouter will be uploaded this week! Subscribe to the channel to get notified when it's available!
  
  Learn how to connect OpenRouter to Make.com and unlock access to ANY AI model, including free LLMs! 🚀 In this step-by-step tutorial, I'll show you how to set up OpenRouter, integrate it with Make.com, and use AI models like GPT-4o, Claude, and more for your automations.
  
  This is great for swapping back and forth between models, while OpenRouter also includes automatic fallback to different models in the event of an error, which can make your automations a lot more resiliant. 
  
  🔗 What you'll learn:
  Connecting OpenRouter to Make.com
  Using free & paid AI models in your workflows

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Engineers"
entities:
  companies:
    - "Anthropic"
    - "Google"
    - "Amazon"
    - "Perplexity"
    - "X"
  people:
    []
  products:
    - "Claude"
    - "Gemini"
    - "Perplexity"
    - "Make"
  models:
    - "Claude 3"
    - "Claude 3.5"
    - "Gemini"
    - "Llama"
concepts:
  - "Enabling that error handling auto retry fall back within open router so let's get started so first off just go to open router"
summary:
  - "# Use This to Instantly Swap AI Models in Make (FREE Options"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "amazon"
  - "anthropic"
  - "claude"
  - "coding"
  - "frameworks"
  - "gemini"
  - "google"
  - "make"
  - "meta"
  - "perplexity"
  - "tutorials"
  - "workflows"
  - "x"
---

# Use This to Instantly Swap AI Models in Make (FREE Options!)

in this video I'm going to be explaining how to use open router in your make.com automations which instead of calling Claude or openi gbt 40 directly within your automations you will call open router and you will be able to choose whatever models you want such as clae open AI models Gemini Gro and many others in fact there are even free models such as llama and some Gemini models using open router is Superior in two ways which is that let's say you have a big automation like this which is call in clawed directly we have clawed effectively hardcoded into the scenario in many different modules if we want to swap to a different model it's not that difficult for example you can have a variable hardcoded there however if you want to swap to a different model from a different provider such as open AI or grock or you want to test out the different outputs it's really cumbersome in a no code tool like make.com and even more importantly than this the error handling within noode tools generally leaves a lot to be desired for example I went through this in the break error handling tutorial on this channel where I explain how it implements Auto retries whereas we can call Cloud through open router we can select the cloud model so go down to Cloud 3.5 Sonet and there are multiple providers and they handle this behind the scenes so if we call Claud and if it errors out it will automatically fall back to a different provider to try and give us the response and so that means that your scenarios will not be constantly breaking and you will not have to constantly keep reprocessing the scenario SC arios which can be costly and just timec consuming to go back and forth so we're going to do that first off I'll show you how to set up your account and how to create the connection then I'll link to another video where I will be replacing all of these clawed modules with an open router module and then explaining how you can swap back and forth between different models and most importantly enabling that error handling Auto retry fall back within open router so let's get started so first off just go to open router. and go to sign in at the top right you you can enter an email address or use the Google single sign on I've done that and I have my account set up go to credits you'll see here I've just added $5 to this open router account just go to add credits and you will see this pop up just enter in your billing details the cost of calling these models is the exact same as if you were calling Claude 3.5 Sonet here directly from anthropic I believe I believe where open router earn their money is by adding a certain percent which is 5% here on top of your credit topup on the account so for $10 it's $10.95 charge which is 5% extra plus a 35 C open router fee they may also be hosting some of these models and they earn some money through that as well when you have your credit added to your account go to keys at the top right so click create key I'm going to just type in make.com key you can leave a credit limit there if you want I'm just going to select create I'm going to copy this out and press X and I will be deleting that after the video then within me.com just type in open rout router create a chat completion then you'll need to create a connection I've pasted in my API key and I'll press save so I have my connection here now I can add messages roll system rooll just type you are an AI assistant next up I'll add item this rooll will be user and I just going to Al ask you to write three about a 50% off Black Friday sale for my online cloes store that's a very generic example message but let's go with that right so I've selected anthropic cloth 3.5 son it a really important point is this automatic fallback so if automatic fallback is enabled open router will try the most appropriate open source model if available with pricing less than the primary model I'm going to select yes there I'm going to go into the settings top right go to settings and the default model I'm going to actually select a default model which will then be the primary fallback model so if we cannot get a response from the claw 3.5 Sonet providers it will fall back to a different model and in this case I'm going to select open AI gbt 40 as the default fallback model so I'll press okay here there is a separate open router module for create a chat completion with fallback you can include the fallback models you can really get quite granular with this so you'll do exactly what you did here which is Define the fallback models in this case I'll go with this more simplified scenario I press okay press save and then I'll run this scenario and see if it comes back with a response that's currently processing excellent we have a response it called 3.5 Sonet the response was from claw 3.5 Sonet which is is great the provider for this request was Google if you go into the 3.5 Sonet page on open router you see there are multiple providers anthropic Amazon bedrock and Google vertex they're all hosting the same model here and this got it from Google vertex it also supports adding your own API Keys which is very handy especially if you have lots of credit already in an account such as anthropic or open AI so you see anthropic you can add in your keys open AI perplexity and so on which is really useful so that's something that you can keep in mind or else you can just use your regular credits let's now change this and we're going to use a free model instead going to go all the way down we'll go to prompt pricing for free and we're going to pick one of the three models we'll pick Google Gemini flash 2.0 experimental this is available through two providers here so I'll just select it from the list it's Google Gemini FL 2.0 experimental press okay press save and run once we'll look at the response so we go down to choices one message and content this is our tweet it's come back with a bunch of different options so it's not ideal if you want to include this in an automation you could go down to show advanced settings and enable Json mode that's a bit more advanced but anyway to get the results I may not have shown you this in the cloud call previously but to get your results go to choices then one message content and there you go then you can include that in your automation so let's say you're creating a Google Document the content of that could be choices message content and there you go and then you choose location every time you run this it will will send it to Google Docs I know that's quite a contrived example but it's just an explanation of how you can call open router instead of calling CLA or open AI or another llm directly check out the link in the description where I go through the next video where I swap out all these direct calls to CLA with open AI so that you can very quickly then swap back and forth between different models and if you want to get way ahead in your automations then check out the link in the description to our community we'll get access to all of our automation templates you can get your questions answered online via our active Community or via our weekly workshops where you can talk to us directly members also get access to these courses thanks for watching
