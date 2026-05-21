---
title: "How to Reprocess Rows in Make (Beginners Guide)"
video_id: "VJWyL2t7RG0"
youtube_url: "https://www.youtube.com/watch?v=VJWyL2t7RG0"
publish_date: "2025-02-28"
duration: "2:10"
duration_seconds: 130
view_count: 429
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_reprocess_rows
  
  In this video, we answer a common question: How do you reprocess data that's already been picked up in Make.com? If you’ve used the "Watch New Rows" module during testing and need to run the same records again, we’ll show you exactly how to do it.
  
  Steps to Reprocess Data:
  Right-click the module.
  Select "Choose where to start" → "Select all" (or pick specific records).
  Click "Run once" to process the data again.
  
  This method allows you to retrigger operations, whether it’s updating rows, sending data to an external system (like OpenAI for AI text generation), or any other automation.
  
  Be careful! If connected to emails or external actions, reprocessing may resend messages or trigger unintended workflows.
  
  Hope this helps! 👍 Let us know if you have any questions.

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
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
  - "# How to Reprocess Rows in Make (Beginners Guide)

a very common question we get asked is how do you reprocess data that's already been picked up within make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "frameworks"
  - "make"
  - "tutorials"
  - "workflows"
---

# How to Reprocess Rows in Make (Beginners Guide)

a very common question we get asked is how do you reprocess data that's already been picked up within make.com for example if you are using this watch new RS module it's going to pick up these records but let's say you doing that during testing and then you want to pick up those records again I'll show you exactly how to do that what you do is you right click and you choose choose to start and select all in this case we're just going to pick up every single record and you would usually do something with that like call an external system or call open AI for examp example to generate some AI text and then dump that back into the sheet into this response field right now I'm not going to do anything with it but I'm just going to update the row so let's select run once here and it's picked up all of these records one by one those are all shown as bundles and then because each of these are bundles it then went through each of those operations one by one so this is effectively like an iterator in the background and it updated this colume here now if I tried to press run once again nothing happens because it is keeping track of these rols in the background now if I go right click choose where to start I can select all I'll select run once again and we'll see it updates all of those again so again just right click and select all or you can even choose the records manually when you do that for example I'm going to choose this second record from here press save that I'll run once you'll see it only updated the second and third records there so when you're choosing where to start you're choosing a particular point and then working from there of course be careful when you're triggering this like if you select choose where to start select all and if this is hooked up to an email account to contact customers or things like that do keep in mind it's going to re-trigger all of those records again so use this choose where to start wisely and be careful one good example is when you're texting you want to just keep rerunning the thing over and over again so I hope that helps and you can use this for many of your different types of modules if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
