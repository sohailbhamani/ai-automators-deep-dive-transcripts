---
title: "How to Trigger Make.com from Google Sheets (WITHOUT the Sheets Add-On!)"
video_id: "iQF2U3pKPIM"
youtube_url: "https://www.youtube.com/watch?v=iQF2U3pKPIM"
publish_date: "2025-02-14"
duration: "4:59"
duration_seconds: 299
view_count: 5808
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_google_sheets_webhook_trigger
  
  As of recording this, the make.com for Google Sheets extension is not available. You can use the approach in this video to instantly trigger webhooks from Google sheets to Make.com. Or as mentioned in the video, you can create an AppScript to trigger your scenario alternatively! I created this video as it's an easier way for people to get up and running quickly if their scenarios are currently broken!

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
    - "YouTube"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - ")

this is a very quick walk through for how to instantly trigger make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "frameworks"
  - "google"
  - "make"
  - "tutorials"
  - "workflows"
  - "youtube"
---

# How to Trigger Make.com from Google Sheets (WITHOUT the Sheets Add-On!)

this is a very quick walk through for how to instantly trigger make.com from Google Sheets without using the make.com extension as a few people in our community and on YouTube have mentioned today they can no longer find this make.com for Google Sheets extension here so automations have broken for a lot of people one very easy way to do this is to create a link and to link to the web Hook from that otherwise you can create a Google app script if you want to have a more sophisticated integration but I'm just going to show you here how to do a web hook which will just speed things up and hopefully get your automations up and running pretty quickly so what we need to do is go to make.com go to new scenario and go to web hook so create a custom web hook and then we're going to click add choose a web hook and then press save then copy that address to the clipboard so we have that copied and then within this web Hook connection we're going to type hyper link and then start quotation mark and then copy it in and then there we go we have the link where you can also do with add the link label so the link label will be trigger make.com okay and then I'm just going to click and drag this down now I'm going to go and press sorry I'll press save I'll click run Once on This then I'm going to go and click this button now it comes up in a new tab to say accept it you can close that but we'll go back and we see that it has hit the web hook so now we're successfully hitting the web hook but we need to pass it some data that's actually meaningful for us to be able to do something now there's a few different approaches we can take here the first is is where if you have a genuinely unique ID on the left hand side or somewhere that you can identify a certain role then what you can do is pass that data to the make.com scenario and then get the row from there that's the first example that I'm going to give you here how you do that is add in a question mark here and then pass in a query parameter so pass in for example ID equals then after the quotation mark select Ampersand and then select the ID from the start and press enter so that means that it's going to add in the ID to the end of that particular URL now let's go to back to this make scenario press Rong once I'm going to select that button and then now we have the ID successfully within make next up we're going to go to Google Sheets and go to search rows I'm going to search that row I'm going to select my spreadsheet so I've selected my spreadsheet then I'm going to select sheet one which is the name of this sheet one I'm going to limit it to one which is very important and then the filter will be the ID and then I'm going to pass in this ID for that filter and press save now I'll press save I'll try this again press run once at the bottom left click this button excellent we have the value within Google Sheets and because we have the value within Google Sheets you can now do whatever you want you can update the row you can trigger an external system or whatever you want I think based on this make.com app you need to at least have some sort of ID if you want to reference it I don't think you can just get it based off the r number like I could be wrong about that perhaps you can do it based on the make an API call module here anyway so let's say that you do not have a specific ID what you could do is pass in specific information such as an email address or the status in this case so what we could do is update this function or sorry update this URL and we'll say email and then select the email field which is there and then type Ampersand start quotation mark and then and then we'll open a quotation mark add an ampersand within the quotation mark and then from there you can pass in other information such as status and again add in an equals start the quotation mark add in an ampersand outside the quotation mark and then select whatever data you want to pass in from there and that should be a valid URL so we can try that out now and in this case we can actually delete this module press okay we'll run once and now we'll trigger this it's accepted so there we go we have the email and I'll zoom in we have the email and the status from there so then you can do whatever you want with that such as you could then search a ro based on the email the filtering criteria or you could just trigger an external system depending on what you want you could also go to extensions and appscript so you could create your own appscript to trigger your scenario depending on for example if you update a drop- down list or something like that there's you can get chat GPT for example to create that script for you but this is a pretty accessible easy enough way that you could get up and running particularly if that make.com extension is gone and of you were using it previously so I hope this helps and if you have any questions then just drop a comment in the comment section if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where you'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
