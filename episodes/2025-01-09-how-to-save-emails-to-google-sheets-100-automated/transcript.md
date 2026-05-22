---
title: "How to Save Emails to Google Sheets (100% Automated)"
video_id: "tbjCe6a7sV0"
youtube_url: "https://www.youtube.com/watch?v=tbjCe6a7sV0"
publish_date: "2025-01-09"
duration: "4:18"
duration_seconds: 258
view_count: 3249
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_gmail_to_google_sheets
  
  Other tutorials from us:
  https://www.youtube.com/watch?v=dGkRrrb3Qos
  https://www.youtube.com/watch?v=_i_le35pOJk
  https://www.youtube.com/watch?v=4xeQ4l1NosU
  
  Chapters:
  0:00 - Introduction
  0:08 - Setting up Gmail integration with Make.com
  1:20 - Connecting Google Sheets to Make.com
  1:45 - Mapping email data to Google Sheets columns
  2:16 - Testing and verifying automation
  2:34 - Formatting date and time in Google Sheets
  3:07 - Exploring advanced automation options
  3:49 - Preview of Gmail to Google Drive automation
  
  In this video, you'll learn how to automate the process of adding new rows to a Google Sheet whenever you receive emails. We'll use Make.com to set up this seamless integration. Starting with Gmail, we'll walk you through the simple authentication process and show you how to configure filters for capturing the right emails.
  
  Next, we'll connect Google Sheets, map email data to columns, and format dates for better readability. You'll also see how to test and verify your automation, ensuring everything works as expected.
  
  By the end of this tutorial, you'll have a powerful tool for managing email data efficiently. Don’t forget to check the description for links to more advanced guides, including how to upload Gmail attachments directly to Google Drive.
  
  Join our community for exclusive templates, live workshops, and support to fast-track your AI automation journey.

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
  - "# How to Save Emails to Google Sheets (100% Automated)

in this video I'll show you how to populate new roles in a Google sheet whenever you receive emails it's really easy to get set up with this and"
keywords:
  - "ai-agents"
  - "ai-news"
  - "box"
  - "frameworks"
  - "google"
  - "make"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Save Emails to Google Sheets (100% Automated)

in this video I'll show you how to populate new roles in a Google sheet whenever you receive emails it's really easy to get set up with this and I'm using a service called make.com for this start off by pressing Gmail and then go to this watch emails from here if you have a Google workspace account just press add and it's really quick to go through the authentication process a popup window will show up and you can just authenticate with that if you're using a personal Google or Gmail account then you will likely have other steps involved with that Authentication there are other Guides Online for how to get set up with that but let's say you have a connection set up you click on this folder and I'm going to select inbox so it's going to be watching out for new emails in the inbox now to start with I'm going to use a simple filter you can use a Gmail filter later on which adds a lot more control of the types of emails that you want then send to this Google sheet in this instance I'm going to start off with a simple filter and I'm just going to select all emails I'm going to select no here and then for maximum number of results results I'm going to select one so every time I click run once it's only going to pick up one email every time later on we can schedule this and then have a lot more results shown up here so I'll get it so it will only pick up emails from now on otherwise if you want to process your entire history of emails then you can select all emails from there so I press save now I have a Google sheet set up here and I'm going to select this plus icon go to Google Sheets and select add a row again I'll add my connection here I've already set up my connection here if you need to add it press add go through a very similar authentication process that you went for Gmail going to search by path then I'm just going to go through the folders so I've selected my spreadsheet ID here sheet name is the first sheet name table contains headers so it will automatically pick up the colume headers as you see here date subject email address now all I need to do is Select each of these fields and you see date here subject email message could be the text content sender name is this and sender email address that press okay again I'll double check it's only picking these up from now on press run once and nothing shows up so what we do is I'm going to send a test email to this inbox on Gmail and then I'm going to run this again after that we can set it as scheduled and then this will run whenever you want it to run okay I've just sent myself a test email there and I'm going to now pick that up so I've pressed run once there and this has now been updated and there we go that's looking good so we have the day the subject email message the name however the date is in this awkward dat time format which we can update separately so I'll do that right now now in this we can go up to the top and go to date then I'm going to select format date then I'm going to select my date as you see it here and then the datetime format can be whatever you want so I'm going to pick date month year and just leave it at that you could even have separate columns for the date and the time where you could just add in this format but just change this date format here to only select the time for example I'm just going to go with this for the moment so I'll press save I just sent myself one more test message let's see that so now that data is in that format that we want of course we could change that to whatever you want here we're transferring that data to Google Sheets but we could also do lots of other things like for example create a task in our task management system through clickup or you could send yourself a slack message for example another option is to use this query to further refine what emails you're actually going to pick up in this automation so for example you could set up a label in Gmail and have it so that it only picks up where the label is invoice or you could say where of attached label of invoice or where the word invoice appears in the subject line or the text then pick up that as well gmail search query is quite Advanced so you can really refine exactly what you want and just test the results in this search box up here to see what results you're getting just copy and paste that directly into here in a separate video I'm going to be explaining how you auto upload attachments from Gmail directly to Google Drive and you can also use filters to narrow down the types of emails that you want this to take place in so check out the link in the description for that if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
