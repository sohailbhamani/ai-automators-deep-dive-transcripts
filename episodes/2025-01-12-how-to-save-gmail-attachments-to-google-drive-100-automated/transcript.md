---
title: "How to Save Gmail Attachments to Google Drive (100% Automated)"
video_id: "dGkRrrb3Qos"
youtube_url: "https://www.youtube.com/watch?v=dGkRrrb3Qos"
publish_date: "2025-01-12"
duration: "4:13"
duration_seconds: 253
view_count: 7808
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_gmail_attachments_drive
  
  Other tutorials from us:
  https://www.youtube.com/watch?v=gPG5kjHEvkQ
  https://www.youtube.com/watch?v=4xeQ4l1NosU
  https://www.youtube.com/watch?v=tbjCe6a7sV0
  
  Chapters:
  0:00 - Overview
  0:23 - Setting up Gmail connection in Make.com
  0:50 - Defining Gmail filters for automation
  1:49 - Processing attachments and limiting email selection
  2:10 - Uploading attachments to Google Drive
  2:31 - Using an iterator for multiple attachments
  3:05 - Testing the automation
  3:22 - Filtering for PDF file types
  3:41 - Advanced workflows and additional resources
  
  In this video, learn how to automate the process of uploading email attachments from your Gmail inbox directly to a designated Google Drive folder using Make.com. This tutorial walks you through setting up a connection with Gmail, refining search filters to target specific emails with attachments (e.g., those labeled as invoices or containing PDFs), and configuring the automation to ensure it processes emails efficiently.
  
  You'll discover how to use Gmail's search capabilities to customize filters, implement an iterator in Make.com for handling multiple attachments in a single email, and ensure only PDF files are uploaded to Google Drive. Additionally, the video provides insights on how to test and verify your automation to avoid processing unnecessary emails.

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
    - "Google"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "com for this and you can also really refine your queries to only upload certain file types or where you have assigned a label to that invoice within Gmail so let's get started with a blank scenario in"
keywords:
  - "ai-agents"
  - "frameworks"
  - "google"
  - "make"
  - "product-management"
  - "tutorials"
  - "workflows"
---

# How to Save Gmail Attachments to Google Drive (100% Automated)

in this video I'll show you how you can set up an automation that watches out for new emails in your Gmail inbox with attachments and then upload those attachments to a Google drive folder automatically I'm using a service called make.com for this and you can also really refine your queries to only upload certain file types or where you have assigned a label to that invoice within Gmail so let's get started with a blank scenario in make.com I'm just going to type in Gmail and select watch emails I also go through this process in our Gmail to Google Sheets automation which you can check out in the description as well but overall when you're setting up a new connection click the add button here and a new popup will show up just go through the process for that and allow access if you have a personal Google account the steps are a little bit more convoluted for that so there are Guides Online for how to set that up overall once you have a connection then just click here to choose and I'm going to select inbox to start with I'm going to enter in a Gmail filter here go to Gmail and you see the search feature up here you can use this to create pretty specific search criteria for the kind of emails that you want to pick up and in Gmail you can chain these together so what I'm doing here is if the email contains the word invoice in it in the email subject or in the text in the email this automation will only pick up emails where the word invoice is somewhere on the email and where it has an attachment and where it has an attachment with a file name of PDF however I also want to have the option to be able to manually assign emails that should be picked up by this automation as well maybe invoice was not in the name so even if an email does not have the word invoice in it you can move any emails you want into this folder and as long as they have an attachment and as long as a file name is PDF on one of those attachments then it should pick up the email okay so I'm going to press okay and I'm going to only process emails from now on so it's not going to pick up you know thousands of emails previously you can separately choose to select from a certain date or from the very first email but with this maximum number of search results I'm selecting one so every time I press run once it's only going to pick up one email so it's not going to go picking up thousands at once now I've gone to Google Drive and I want to post all of the attachments directly into this folder as you see here next up we want to move these files to Google Drive so I'm going to select upload a file when I go down here and select file name I see there's a list of attachments here but this is in an array form and that's because you can have multiple attach ments in one email so what we need to do is use an iterator to iterate through every single one of those attachments it's actually a pretty simple use case of an iterator within make.com sometimes it can be a little bit confusing so I've selected my iterator here and then simply select attachments press okay now that we have this iterator in place it automatically Maps the file from the iterator through this so all we need to do now is just select the folder that we want within Google Drive so I'm just going through the folder locations here so that is the folder that we want and select okay press okay and save now I'm going to choose where to start select from now on just to make sure okay so I've just sent myself an example attachment here it has the word invoice in the subject and I've attached a PDF okay now I'll test out this scenario I'll press run once it's gone through that it looks okay and I've gone to Google Drive I can see it's pushed that file to Google Drive one other thing that would be good to add in here I'm going to select this part of the flow which is to add a filter and select this type and where it's equal to application PDF so I effectively only want to upload PDF documents to Google Drive so this will work for as many attachments that you send in an individual email as possible if you want to take this a step further then check out the link in the description where I've gone through a more extensive kind of version of this type of system where it's processing through the files after they've been placed onto Google drive in this case it's extracting the data and adding that to a Google sheet but you can customize these kind of systems however way you want if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
