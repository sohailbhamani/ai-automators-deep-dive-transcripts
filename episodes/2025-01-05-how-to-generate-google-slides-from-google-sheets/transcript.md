---
title: "How to Generate Google Slides from Google Sheets"
video_id: "GyQwN5z4YTE"
youtube_url: "https://www.youtube.com/watch?v=GyQwN5z4YTE"
publish_date: "2025-01-05"
duration: "5:11"
duration_seconds: 311
view_count: 7385
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_google_sheets_to_slides
  
  Our more advanced google slides automation tutorial:
  https://www.youtube.com/watch?v=0ChgBZoTPcs
  
  Chapters:
  0:00 - Overview
  0:55 - Sheet and template
  1:30 - Sheets module
  1:55 - Slides module
  4:07 - Extending the automation
  
  In this video, you'll learn how to use Make.com, a no-code automation tool, to automatically generate Google Slides presentations directly from data in Google Sheets. This tutorial walks you through the setup process step-by-step, starting with a simple example that you can scale to handle larger datasets.
  
  The process begins by preparing a Google Sheets file containing your data, such as company names and focus areas. You'll also need a Google Slides template with placeholders, formatted using curly brackets (e.g., {{Company Name}}), where your data will be inserted. Using Make.com, you'll create an automation scenario that links Google Sheets to Google Slides. This setup involves selecting the spreadsheet, mapping the data fields to the placeholders, and specifying where the generated presentations will be saved in Google Drive.
  
  The tutorial demonstrates how to configure the scenario with just two modules and explains how to run the automation either on a schedule or using instant triggers. By the end of the example, you’ll see how to generate multiple slide decks effortlessly and how to refine the setup to create presentations in bulk.
  
  For advanced users, the video explores additional features such as integrating OpenAI GPT for text generation, creating custom content for slides, and adding connections to other tools like Slack, email, or Airtable to enhance your workflow. It also touches on scaling the workflow by integrating multiple data sources like SEO analytics, Google Analytics, and WordPress to create comprehensive reports.
  
  If you’re interested in diving deeper into automation, check out Daniel’s video linked in the description. It shows how to create a more sophisticated SEO monthly report using similar principles.

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
  []
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

# How to Generate Google Slides from Google Sheets

in this video I'm going to show you how to create Google Slides directly from Google Sheets and you can do that at scale for as many as you want this is a really simple example where we just have a few different fields in a Google sheet and we've created a really simple template in Google slides and when our automation runs it will create separate slide decks for those and put them into a Google drive folder I'm using a service called make.com for this which is a no code automation tool and it's really easy to get set up with this this only takes two modules in this scenario and you can run this on a schedule basis or use instant triggers which we've also covered on the Channel Once you understand these Concepts then you can get far more sophisticated and check out the link in the description to Daniel's video on our main Channel where he gets data from multiple different data sources and then injects all of those into a far more complex and sophisticated Google slide deck in this case it's for the use case of an SEO monthly report but let's start from the start with a basic example I have this test data here the data is a little bit contrived but I'm simplifying it so you really understand the concepts of how these templates work I simply have five different columns I'm using a Google Slides template but I've added in these curly brackets for company name proposal title whenever we have these placeholders here then the automation will inject that data into the slides from the spreadsheet this is the first slide and this is the second slide where it's simply just going to inject Focus Area 1 2 and three from this spreadsheet and then you can make this as complex as you want afterwards but let's start off with this simple example I've opened up my make.com scenario here from here I'm going to select Google Sheets and watch new roles then I'm going to search by path my drive and then I'm going to select my spreadsheet so Google Sheets to Google Slides then I'm going to select this SEO workshops spreadsheet that I just created here the sheet name will be the first name and I'm going to limit to one to start with so it will only pick up one row at a time I'll select all because we want it to start from row number two then I'm going to go to Google slides and show more and create a presentation from a template now I've of my connection if you do not have a connection then press add and then a popup will show up for you to authenticate with Google Slides so next I'll select the title for this I'm just going to type in the company name and I'm going to go to date up here and just add in now which is the Tim stamp current time stamp then I'm going to copy a presentation by dropdown so I'm going to choose my drive and I'm going to choose this presentation ID which is this template that we created separately go to make tutorials Google Sheets to Google slides and then it should show up with this Consulting proposal template example and a really neat feature of this make.com app for Google Slides is that it automatically grabs all of these placeholders that we've created so all we need to do is map those directly from Google Sheets so for company name I'll select company name from Google Sheets which is this here I'll do the same for this Workshop title area Focus Area 3 Focus area 2 then at the very end I want to select the document location I want all these documents to end up in this presentations folder so I'll go to Google Sheets Google slides and select that presentations folder and press okay now I'll press save now I've pressed run once down here it should have picked up the first row from this Google slides and created a presentation so let's go back to here looks good it's created that presentation excellent so we see it has added this title in here the discovery Workshop the areas to focus on and so on that's looking pretty good although the title does not look very good especially if you're going to be presenting this so what I'm going to do is I'll just for the moment get rid of that date from the very end and I'll update the limit here to 10 so it can generate 10 slide decks at a time and then I'll press run once it's going to pick up all of the remaining rols from Google Slides as you see here it's done one operation to take all of those and each of those show up as a bundle within make.com and you see here it's been processing each of those and that shows up with three operations so it's done all of that now let's refresh the page here now I go back to my Google Drive I can see it's automatically created all of those so I'll go into this one and we see it's created this presentation based on this template now you can extend this with as many placeholders as you want you can also add in other modules such as open AI gbt 40 and start injecting AI into the equation where you could for example take some of this data create its own text and then inject that into the slides you could then add lots of other modules to this such as email integration slack integration or whatever else you want to integrate this into your overall workflow then if you want to really take this to the next level you can check out Daniel's automation on our main Channel where we created an SEO monthly report audit integrating lots of different data items like data for SEO Google analytics WordPress all together so this shows how you can use things like air table and lots of different data sources and then inject those into Google Slides so check out the link in the description for that and if you want to get way ahead in your AI automation Journey then also check out the link in the description where you can get access to our community where you'll get access to all of our automation templates including the one in this video we also have these courses and more on the way you can get Live support from us directly through our live workshops and in our active discussion boards thanks for watching
