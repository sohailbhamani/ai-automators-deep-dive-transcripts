---
title: "How to Use Scenario Inputs in Make.com (Quick Guide)"
video_id: "yPET9I-0hsU"
youtube_url: "https://www.youtube.com/watch?v=yPET9I-0hsU"
publish_date: "2024-12-12"
duration: "2:21"
duration_seconds: 141
view_count: 5203
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_scenario_inputs
  
  In this tutorial, we’ll explore how to use scenario inputs in Make.com to manually run scenarios with dynamic data—without relying on tools like Airtable or Google Sheets. This method can simplify your workflow if you want to build something quickly without integrating with external systems for your starting trigger.

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
    - "Google"
    - "Slack"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "com (Quick Guide)

in this video I'm going to quickly explain what these scenario inputs are in make"
keywords:
  - "ai-agents"
  - "coding"
  - "frameworks"
  - "google"
  - "make"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Use Scenario Inputs in Make.com (Quick Guide)

in this video I'm going to quickly explain what these scenario inputs are in make.com and how you can use them generally in order to run a scenario you either schedule that scenario to run at regular intervals or you use web hooks or instant triggers there's on demand scheduling which means that this is going to wait and like click activate scenario this is going to wait for either you to click run once at the bottom left or it's waiting for this to be externally triggered in this example we're just going to click run once in order to run it for the scenario input we can Define mandatory data that we need to add every single time the scenario is run in this really simple example we're going to interact with a stock photo library called pixel Bay we're making a simple request to get a bunch of search results then we're going to pick the first search result and upload that to Google Drive in this example we've hardcoded the search term of birds whereas we're going to want to make this dynamic in this example we're not going to use air table or Google Sheets or slack or some external trigger we want to dynamically send in data every single time it's run but do it when we click the Run ones button you could do this via variables but it's actually a better option to enforce this true scenario inputs so I'll give you an example in scario inputs go to add item I'm going to type in search term type of text and make it required and you can add in lots of different fields and then under this go to custom and system variables at the top and then you will see the scenario input up here of search term click okay now when I click run once this search term shows up and I then then need to add in a search term so let's say instead of birds I'll type in office I'll click okay by the way I've temporarily set up a filter so it does not uploaded to Google Drive but let's see the result so it looks like it responded okay let's have a look at the result and there we go we have a picture of an office for these scenario inputs you can add in as many of these items as you want and actually have a member of a team working directly within make it's not always the best option but if you want to do something quickly if you do not want to integrate with air table or any other internal system as your starting point make.com can be your entry point into a scenario using these scenario inputs so I hope that was helpful if you want to get way ahead in your automation Journey check out the link in the description to our community we'll get access to all of these courses all of our automation templates weekly workshops and pro level support to get you way ahead thanks for watching
