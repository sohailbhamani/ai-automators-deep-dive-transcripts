---
title: "How to Generate Google Docs from Google Sheets"
video_id: "8LEP1bKY0LU"
youtube_url: "https://www.youtube.com/watch?v=8LEP1bKY0LU"
publish_date: "2025-01-10"
duration: "4:43"
duration_seconds: 283
view_count: 7007
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_google_sheets_to_docs
  
  In this video, learn how to automatically generate personalized Google Docs from rows in a Google Sheet using Make.com. This step-by-step tutorial covers setting up templates, automating the creation process, and saving the files to a specific Google Drive folder.
  
  Chapters:
  0:00 Introduction
  0:50 Setting Up Google Sheet
  1:06 Creating a Google Docs Template
  1:58 Configuring Make.com
  3:10 Generating Documents
  4:06 Extending Automation
  
  Key Takeaways:
  - Use a Google Sheet to store data for generating documents.
  - Create a Google Docs template with placeholders for personalized fields.
  - Set up Make.com to automate document creation and storage.
  - Extend automation to download documents as PDFs, email them, or send notifications.

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Engineers"
  - "Executives"
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
  - "com for notes we want to just add in notes at the start and then the notes will show up after that okay that should be good enough for the moment we have this Guardian service response template I'm go"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "coding"
  - "google"
  - "make"
  - "product-management"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Generate Google Docs from Google Sheets

in this video I'm going to show you how to create many Google Docs using a single Google sheet you can populate as many roles as you want here and then it will create Google Docs based on a template that you provide for example we have first name last name service type and then it will create personalized individual documents for each of those after that it will store that in a specific Google drive folder we're using a service called make.com for this which is a noode automation tool and it's really easy to use when you understand the building blocks of this you can then extend this automation to do lot of other things such as download the documents to PDF email them to others send yourself a slack message or whatever else you want you can then run this automation on a scheduled basis or use instant triggers which we cover on this channel as well I'm going to be going through the process for this which is pretty straightforward but if you want to get access to all of our automation templates then check out the link in the description to our community to start off we just need a Google sheet and then a folder where we're going to store all of our Google Docs that are created so I have this Google sheet I've asked chat ift to generate some sample data from here I'm going to use to populate okay so we have first name last name email appointment date and so on next up we need to create a template for Google Docs again chpt has generated a template for me here which is good going to call this gardan service response template so this is our template and by the way template is just a regular Google doc and we just add in these special placeholders as you see here first name last name chb has added a placeholder here where we should add in our own business name I'm just going to remove that for the moment what we're going to do is we'll get make.com to pop all of these we have first name last name service type appointment date price and notes and then we have this text which is going to be hardcoded so for this email we actually want this to be our own email so I'm just going to type in an example email address example support email example.com for notes we want to just add in notes at the start and then the notes will show up after that okay that should be good enough for the moment we have this Guardian service response template I'm going to leave that as it is then I'm going to go to make.com and so I'm going to go to Google Sheets so just type in Google sheet and then watch new rows I'm going to search by path you just go and select all of these I'm going to select my spreadsheet so you just select your folders as you're going along I've selected my spreadsheet here select sheet one I'm going to limit to one at a time just to make sure we're doing what we should I'll select all then this will just start picking all of these up next up I'll press plus and search for Google Docs and then create a document from a template then I'll just search for that Google doc from there that's the guardian service response template that we just created a really nice feature of this make.com app for Google Docs is that it autop populates these placeholders so we have first name last name appointment date price and these are all autop populated which is fantastic we then just need to select the first name the last name and so on from the spreadsheet appointment date price and notes for the title we'll just select the email address and the first name and last name and so this is just going to be an amalgamation of a bunch of fields together for the drive location I'm going to select the location I want want which is that folder which is this docs folder here I'll press okay so now it should create new Google docs for every Row in this spreadsheet I'll start with the first one so I've pressed run once down there and it's now created this document here we go it's automatically created this with the correct placeholders we see we have some extra markdown kind of text that I copied in from chat gbt earlier so what we can do is delete those and you know change those as bold you see there and I'll just make some slide updates there to to add correct bullet points and then the next time this is generated for the next one then it will use this formatting as you see so let's press run once again and just wait and it will create the next one which is perfect finally we'll update the limit on this first module so it can do up to 10 at a time you can make that number as big as you want so I'll press run once again and then it will process all of those so you press run once it has gathered two of those bundles so that's two rows then in this speech bubble here you see it's used two operations so it's created two different documents and once we refresh the page here we'll see it's created two of these new documents so once you have those you can do whatever you want with those documents you can even then go to do Google Docs you can download the document in PDF form for example then upload that to Google Drive you can integrate it with your email you can send yourself notifications via slack or whatever else you want but you can use this as a build-in block to really understand how these kind of templates work within me.com if you want to get way ahead in your AI automation Journey then check out the link into the subscription to our community where you'll get access to all of our automation templates including the one in this video you get access to all of these courses and more are on the way you can get Live support from us via our weekly workshops and Via our active online discussion boards
