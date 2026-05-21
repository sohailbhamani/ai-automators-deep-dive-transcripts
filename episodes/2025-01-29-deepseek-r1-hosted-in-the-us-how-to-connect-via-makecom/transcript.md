---
title: "\"deepseek R1 hosted in the US?\" How to Connect via Make.com"
video_id: "DEWIPPe5LlY"
youtube_url: "https://www.youtube.com/watch?v=DEWIPPe5LlY"
publish_date: "2025-01-29"
duration: "7:57"
duration_seconds: 477
view_count: 914
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_deepseek_connection_make
  
  Our openrouter video: https://www.youtube.com/watch?v=EsGniZ7Sl8k
  Escaping JSON: https://www.youtube.com/watch?v=18wgBZxOp0U
  Deepseek blogging system: https://youtu.be/T54TIvCOCpY
  
  Chapters:
  0:00 - Overview
  0:34 - Deepseek API options
  1:42 - Connecting via Fireworks AI
  2:10 - Setting up Fireworks API Key
  4:34 - Handling Chain of Thought responses
  6:09 - Direct connection to Deepseek API
  6:46 - Using OpenRouter for flexible integrations
  
  In this video, you'll learn how to connect Deep Seek R1 (using a USA-based service) to your Make.com scenarios. We start by demonstrating a simple example using Google Sheets to trigger a response from Deepseek R1, excluding its "Chain of Thought".
  
  We explore various connection options, including direct API usage, Fireworks AI for enhanced privacy and security, and OpenRouter for flexibility when switching between models.

yt_tags:
  []


# AI-enriched metadata
content_type: "Framework"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Engineers"
entities:
  companies:
    - "Google"
    - "AWS"
  people:
    []
  products:
    - "Make"
    - "o1"
  models:
    - "DeepSeek"
    - "o1"
concepts:
  []
summary:
  - "com

in this video I'll show you exactly how to connect deep seek R1 to your make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "aws"
  - "frameworks"
  - "google"
  - "make"
  - "o1"
  - "prompting"
  - "tutorials"
  - "workflows"
---

# "deepseek R1 hosted in the US?" How to Connect via Make.com

in this video I'll show you exactly how to connect deep seek R1 to your make.com scenarios I built one of the simplest examples I could here which is where it's listening out for new topics within this Google sheet then it will call Deep seek R1 and respond with the result I've also added a trick so it excludes its Chain of Thought from this once you understand how this connection works then you can use this in far more advanced automations such as our blogin system as you can see here and by the way if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates including this one there are a bunch of different ways to connect to deeps R1 right now and it's important to talk about this first you can connect to deep seek directly using their API it's currently actually down because it's probably being bombarded with requests if you're looking to quickly access deep seek via API this is by far the cheapest option but I'm going to show you how to connect a fireworks AI That's for two reasons first is that the model might be available when deep seek is not and secondly it's due to privacy and data security concerns when using this main deep seek API there are genuine questions over whether your data will be used to train future models and the data is stored in Chinese data centers which generally is not going to be directly aligned with us and EU laws a key point of deep seek is that it's open source and that it can be holed anywhere I'm going to show you how to connect to it via the fireworks API which is a company headquartered in California and they have a zero data retention policy the cost to call these models via these Services is significantly more than calling deep seek but it's still a lot less than using models like open Ai or1 and by the way if you have very strict data security requirements there are other options to host these such as on private cloud services such as AWS or Google Cloud so let's start from the very start I have a blank make.com scenario here I have a Google sheet where I just have two columns here topic and response and I'm going to go to search more and then watch new rols I'm going to search by path and click here to choose file now I'm just searching for my spreadsheet I've now found my spreadsheet I'm going to select the first sheet table contains headers I'll keep the limit as that for the moment and press save if it choose where to start I'll select all so now it should pick those up correctly I'll press save next up to interact with fireworks we need to use a HTTP module so I'll type HTTP make a request then go to fireworks. a click get started set up an account once you have an account set up here you can go to the top right go to billing and add some credit then go to API Keys then create an API key enter in your API key name and then you will get an API key copy that out and then you can use this within your make.com scenario next up we need to construct this request so we'll go to http and then go to fireworks. a then I'm going to click deep seek R1 and then you'll see some guidance on what you need to do from there so copy out this URL the chat completions URL into there so that's the URL we'll select post add a header then we'll type authorization and then Bearer and then finally we need to copy out the API key that we made within fireworks so I've added in this API key here I will delete this afterwards body typ I'll select raw content type Json application Json and then we'll copy out this payload just to start with as you see there and then par response yes then click save so now I'm just going to try to call this request directly run this module only perfect so we have data choices number one message excellent so we already have a response that did not take very long I'll show you a trick afterwards to get rid of this P section from the start sometimes it will output a lot of its Chain of Thought and then we'll then provide you with the actual answer from here before I do any of that I now want to add in my topic here and then link that so map that text from the Google Sheets to this so all I need to do there is go down and then under content we'll select the topic from the Google sheet I'll also add another trick here later on to escape this Json just in case you are coming up with errors but for the moment we'll work with this and then click save again now finally before we do that I'm going to click Google Sheets update a row and going to select enter manually and I'm going to select the spreadsheet ID from the start and then I'll then update the r with the respon resp from this so sheet name will be the sheet name from the first one row number is a row number first up and then A to Z and then within column B which is the response so that's where we want to respond the data we from the make a request we'll go to choices message content and click save click save again now I'll just enter a topic explain AI agents now I'll click run once then that will pick up this first topic then it's now going to make the request then it should update this with the response perfect we've got a response so let's have a look at this now we have an entire Chain of Thought at the start which is not what we want this is what deeps R1 has is it has this Chain of Thought similar to open AI o1 but it's shown us here so I need to explain AI agent let's start by breaking down what we know that's the thought process then after that it's shown us its actual answer as you see here we want to exclude this from the output an easy way to do that is to use the split function and then add in a semicolon and it's going to respond with this P string so we'll split that and then we'll use the last function to return the last element of the array what it's doing there it's splitting the array based on when this appears so we will return the last part of that array which is going to be this and finally we want to only do this if that text includes think within the output so I'll select contains over here this contains think so if that's true I'll add in a semicolon then it's going to return the last item of that array which is everything after thing however we need to finish it off if it does not include think then we just want to Output the entire string now click save but we actually need to close one of these functions if contains closing function there I think we need to close this the last okay I think that's good let's press save save again now I'll just add this again all right so I've added in a new row and now we'll try that again click save run once now it's calling deep seek R1 again okay that's processed now excellent it looks like it's worked correctly let's have a look the choices content looking at the response it did come back with this big long Chain of Thought we've removed that entirely using this function using this horrible function here and then we now see the result here that's how to connect via fireworks AI it's not the cheapest so if you want to connect to deep seek directly then go to deep seek.com at the top right you see API platform as a button when you go into that at the moment I'm getting this our website is currently unavailable deep seek is topof the world news at the moment so I think it's getting heavily bombarded but if you can get an API key and if the service is actually usable then type deep seek and you see there are a few different options here go to deep seek Ai and then create a track completion so select create a connection and then you can add in your API key there and the process is going to be quite similar to what we did for fireworks. a but it will be a little bit easier finally you can connect via a service called open router this is a great middleman service where you can connect to one API which is open router it's really good value and you can even bring your own Keys within this module then you've very easily set up a connection then you can very quickly switch back between deep seek R1 and many many other models this is great when using a no code tool like make.com where it's not always easy to swap between models especially if you're using the native modules it could take a long time to swap back and forth between them if you want to learn how to connect to open router then check out the link in the description where I go through that in detail I also released a separate video recently explaining how to connect deep seek to our bloging automation I was having some issues with the output of or one at the time that may have been an issue due to open router swapping providers if you are having issues with open router you can connect directly via fireworks as I mentioned there and you will probably get a good connection or you can connect to deep seek directly with potential concerns for data privacy and security as I mentioned earlier if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
