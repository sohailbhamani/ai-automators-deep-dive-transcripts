---
title: "How to Automatically Summarize Emails to Slack with AI (100% Automated)"
video_id: "4xeQ4l1NosU"
youtube_url: "https://www.youtube.com/watch?v=4xeQ4l1NosU"
publish_date: "2025-01-13"
duration: "4:30"
duration_seconds: 270
view_count: 1859
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_summarize_emails_to_slack
  
  Other videos from us:
  https://www.youtube.com/watch?v=_i_le35pOJk
  https://www.youtube.com/watch?v=tbjCe6a7sV0
  https://www.youtube.com/watch?v=dGkRrrb3Qos
  
  Chapters:
  0:00 - Overview
  0:16 - Setting up Gmail integration in Make.com
  1:11 - Configuring OpenAI module for email summarization
  2:38 - Adding Slack integration and sending messages
  3:00 - Testing the automation with sample emails
  
  In this video, we demonstrate how to create a simple but effective automation using Make.com that connects Gmail to Slack with the help of OpenAI. The automation monitors your Gmail inbox for new emails, summarizes them, and sends a Slack message containing key details like the sender, subject, and a concise summary.
  
  We start with a blank Make.com scenario and set up Gmail's "Watch Emails" module to filter incoming messages based on your preferences. Next, we integrate OpenAI to generate email summaries, guiding you on how to retrieve and input API keys for seamless functionality. The Slack module is then added to ensure these summaries are delivered to your chosen channel, along with sender details and direct message links for quick access.
  
  Throughout the tutorial, we share tips for customizing the workflow, such as adding filters for specific email types, incorporating OpenAI-generated JSON objects for advanced data extraction, and even detecting spam emails.

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Agents"
difficulty: "Intermediate"
audience:
  - "General"
entities:
  companies:
    - "OpenAI"
    - "Google"
    - "Slack"
    - "Box"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "# How to Automatically Summarize Emails to Slack with AI (100% Automated)

in this video I'm going to show you an automation that watches out for new emails in your Gmail inbox and automatically sends"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "box"
  - "frameworks"
  - "google"
  - "make"
  - "openai"
  - "prompting"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Automatically Summarize Emails to Slack with AI (100% Automated)

in this video I'm going to show you an automation that watches out for new emails in your Gmail inbox and automatically sends a slack message with a summary of those emails we're using a really simple make.com scenario for this and you can update the prompting for this however you want and extend this automation to suit your needs let's get started we'll start off with a blank make.com scenario I'm going to search Gmail watch emails for here I'm just going to add in a simple filter inbox and then all emails you can use a Gmail filter to really drill down on the exact types of emails that you want to push to this automation so you could filter by certain words by ones that are assigned to certain categories or labels and so on for the moment I'll just process all emails through this that are received from the time that I Sav this automation but check out the link in the description where I have two other automations that use Gmail and I'm going through this process to filter the results in more detail for now let's continue with symbol filter and I'm going to only retrieve one result every time I press this run once button or I can then schedule the automation to happen whenever I want so press okay and then from now on is important I'll press save next up we're going to open up an openai module many of you watching this will already have an open a account but just bear with me for a second if you do not have an openai account then go to open.com set up an account and then go to the API key section and then copy out your API key this is different than a chat gbt account so I'm going to go to open Ai and open AI create a chat completion over here again if you do not have an account press add and then you need to add in your API key and your organization ID which you can get by pressing this button it will go to the settings on your open account I'm going to go to chat gbt 40 latest these 01 models are very Advanced but they're a little bit more expensive 40 is perfect for this kind of use case for RO I'm going to assign a system role and the system role here will be you are an assistant that will summarize the key points from an email be concise your response but include all of the most important key takeaways we can leave the completion tokens as is then for user got to text content and then we'll select text content from this Gmail message it's kind of Handy within make.com once you select the box then this context of data from the other modules shows up here you can leave the rest blank and then okay I'll make one more update be concise in your response would include the most important key takeaways only include maximum of two sentences your response let's start by being pretty concise I press okay we could test this out straight as it is but just to speed things up I'm going to add in a slack module I'm going to create a message I'm going to add it in this private Channel within slack I have this private Channel set up just called test Channel 2 for the sake of this so I've selected private Channel 2 and then text of that will be the result of this open AI chat completion prompt I'll leave it as that for the moment but I also want to include sender name the subject and the sender email email address and then email summary after so press okay and I'll try that out okay so I've sent myself a really verbal email looking for support request now I'm just going to run this once and try and pick that up see how it summarizes the email and then sends that slack message so I go to slack perfect so now within slack we have this sender name the subject the email summary she exploring ways to automate her social media process to save time and ensure consistency she's seeking advice on using tools like air table or Google Sheets zap here so that's a good General overall summary then one other thing is it would be nice to be able to jump straight to that message whenever you receive it so we could update this to add in message link and then select that which is this message link here so I'll just run that again just to make sure that it shows up okay and slack perfect now we have the message link as well as the email summary there are so many other ways you could take this you could get open AI to determine if the email is Spam and if it's not then it just will not send the slack message you can add in a filter into the process here to do that or you could get open AI to respond as a Json object object and then extract a bunch of different data from the emails and then push those to slack in a certain format check out the expert make.com tips video that we have on our Channel where I go through how to extract Json data from an open Ai call like this if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where you'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
