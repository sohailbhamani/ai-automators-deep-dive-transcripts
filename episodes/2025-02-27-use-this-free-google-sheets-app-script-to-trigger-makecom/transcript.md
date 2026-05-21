---
title: "Use This Free Google Sheets App Script to Trigger Make.com"
video_id: "LTMvHKyrzLg"
youtube_url: "https://www.youtube.com/watch?v=LTMvHKyrzLg"
publish_date: "2025-02-27"
duration: "5:09"
duration_seconds: 309
view_count: 3007
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_make_google_sheets_app_script
  
  Get the App Script here (no signup required): https://www.theaiautomators.com/how-to-use-an-app-script-to-trigger-make-com-from-google-sheets/
  
  Our previous video using a hyperlink to trigger: https://www.youtube.com/watch?v=iQF2U3pKPIM
  
  In this video, I'll show you how to create a Google Apps Script that triggers a Make.com scenario instantly from Google Sheets—without using their extension, which isn't available at the time of recording. This is an improved version of a previous method where we used hyperlinks to trigger webhooks, but this approach prevents unnecessary new tabs from opening and offers a smoother automation experience.
  
  We'll start by setting up a standard webhook in Make.com and then generate a Google Apps Script to send a POST request whenever a value in column D is updated. The script will pass all row values in a structured JSON format, ensuring easy integration with other tools. I'll walk you through copying the webhook URL, implementing the script in Apps Script, and setting up triggers to automate the process.
  
  Next, we'll test the trigger by changing values in Google Sheets and confirming the webhook fires correctly. I'll also demonstrate an OpenAI integration that processes data dynamically. Later, we'll refine the script to handle multiple row updates at once, ensuring efficiency for bulk data changes.
  
  Finally, we'll test the overall performance of this integration by measuring latency when external API calls are removed. The results show that this method is quick and reliable.

yt_tags:
  []



# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Tools"
difficulty: "Intermediate"
audience:
  - "General"
entities:
  companies:
    - "Google"
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
  - "# Use This Free Google Sheets App Script to Trigger Make"
keywords:
  - "ai-news"
  - "box"
  - "frameworks"
  - "google"
  - "make"
---

# Use This Free Google Sheets App Script to Trigger Make.com

in this video I'm going to show you how you can create an app script to instantly trigger make.com from Google Sheets without using their Google Sheets extension which by the way is not available at the time of recording this is a follow- on video from the simpler example where I was triggering a web hook using hyperlink directly within the field that is a very simple approach but it has the kind of annoyance that every time you click on a link it opens up in a new tab the appscript is just a better experience where that you can get it to listen out for changes within this colume for example and every time you change it it will trigger this make.com scenario this is a simple web hook and we're just pasting in the value of that web hook at the bottom of this script I'm giving this script away for free just check out the link in the description and it's available in the free section of our community so let's get started we're going to use a standard web hook within make.com so type web hook and then select custom web hook then I'm going to select add press save sorry I'll move this over here and then we can copy this address to the clipboard so I've gone to chat gbt and now I'm going to add ask it to write a Google Sheets of script to trigger a web hook add in the placeholder web hook url.com so add a web hook whenever a value from colume D is edit is updated this should be a pulse request and pass in all of the values from the row within the Json body 2 so when we're passing the values of the RO from adjacent body so the value should be in the form of colum name for example a email if they get the column name from the header row if there are spaces then replace them with an underscore okay that should be enough for the moment so let's just run that and see the Google app script that gets created from that okay so this has been generated let's copy this in to our app script I'm going to replace what's here delete that and add this in then I'll go back to my make scenario I created this web hook earlier so I'm going to copy this address to the clipboard and from here I'll paste the so this is our actual web hook URL so I've saved this I'm going to go to triggers add a trigger on the bottom right okay the function is on edit head looks okay from spreadsheet on event type so on edit and then notify me immediately if there's a failure you can change your settings for that if you want so I'll press save and a notification box may show up to get you to approve the connection for that so I'm going to allow this connection now that's been saved so let's try it out I'm going to press save here and press run once I'm waiting waiting for that web hook to trigger now I'll go back to this sheet and I'll change the status of that and let's see if this triggers and there it's triggered which is excellent now if I zoom in something that's fantastic about this is that we have the row number here as well as all of the values that are in that sheet so far which is really good now from there I can do something like pass this value into an open AI module for example I'll go to create a chat completion I've selected GPT 40 as a model for that again this is just a simple example of what what I'm doing here so I'll just pass in the name and then I'll just say for the first name of this person only respond with their first name and and no other explanatory text okay that's good press save and now we'll go back to Google Sheets and we're going to update the row from here we'll search by path we'll select our spreadsheet so I've selected my spreadsheet here I'm going to select sheet one you could also provide the sheet name within this appscript as well for the moment we're working off a single sheet the row number is row number two and that's being provided within this web hook which is fantastic and then from here we just want to update the response so that will be the response and we'll press save so now I'll select immediately as data arrives for this press save so that means it's going to be waiting off for this web hook now now I'm going to just update this status and then that should trigger the response and update this Google sheet pretty shortly and there we go it's worked by itself now the next question here is what happens if we update the data of multiple columns at once so I'm going to press run once and then I'm going to paste in this data into multiple bu at once let's see what happens so we see that it has only taken the first row from that entire selection so we need to update the script in order to be able to handle this situation I've asm.com to format this as a list of objects that will be interpreted as a separate or as separate bundles by make.com so we're providing a flat array of objects which is the correct format that make wants for this so I will press copy I've replaced the script with a new one and I'm now passing in this web hoc I press save so I'm going to update all of these roles at once and let's see if it gets triggered into make.com right it's happening looks good behind the scenes make.com interpreted each of these as a separate bundles and it ran the scenario for each of them which means we can update a lot of roles at once and it will still work magically let's remove the open AI aspect from this equation and just check how quick this integration is overall all we're going to do is just provide a random number I'm going to update the value of each of these rows and then let's see the response so was pretty quick response pretty good so if you're not waiting for an external system then it shows that the latency is actually quite low on this so again check out the link in the description if you want to get this script
