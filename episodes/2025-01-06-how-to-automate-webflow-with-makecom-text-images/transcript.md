---
title: "How to Automate Webflow with Make.com (Text + Images)"
video_id: "qwZGai5vryw"
youtube_url: "https://www.youtube.com/watch?v=qwZGai5vryw"
publish_date: "2025-01-06"
duration: "4:58"
duration_seconds: 298
view_count: 2394
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_make_to_webflow
  
  Our more advanced blogging automation tutorials:
  https://www.youtube.com/watch?v=6wJaqpJyswA
  https://www.youtube.com/watch?v=sJ4QrtWwkBA
  
  In this tutorial, learn how to automate uploading text and images from Airtable to Webflow using Make.com. This straightforward process lays the foundation for more advanced automations.
  
  Chapters:
  0:00 - Overview
  0:40 - Airtable
  1:29 - Webflow connection
  1:45 - Creating content item
  2:50 - Markdown conversion
  3:50 - Updating airtable status
  
  Key Takeaways:
  - Initial Setup: Use Airtable to manage article data (titles, text, images, and status). Configure a Webflow account and CMS collection for blog posts.
  - Automation Steps: Set up a Make.com scenario to filter Airtable records with "Publish to Webflow" - status. Create Webflow CMS items with data from Airtable (title, body, and image URLs).
  - Formatting Improvements: Convert markdown text from Airtable to HTML for better formatting in Webflow. Pass image URLs to Webflow for direct upload and storage.
  - Final Touches: Automate Airtable status updates to prevent duplicate uploads.
  
  Step-by-Step Process:
  - Prepare Airtable Base: Include fields for article title, text, featured image, and status (Open, Publish to Webflow).
  - Set Up Make.com Scenario: Filter records with status = "Publish to Webflow". Create CMS items in Webflow using Airtable data.
  - Improve Text Formatting: Use the markdown-to-HTML module in Make.com for cleaner text display.
  - Automate Status Update: Add a module to update the status in Airtable to Published after successful upload.

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
    - "YouTube"
  people:
    []
  products:
    - "Make"
  models:
    - "Flux"
concepts:
  []
summary:
  - "com (Text + Images)

in this video I'm going to show you how to connect make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "make"
  - "product-management"
  - "tutorials"
  - "workflows"
  - "youtube"
---

# How to Automate Webflow with Make.com (Text + Images)

in this video I'm going to show you how to connect make.com to webflow so you can directly post text and images to your webflow site it's really easy to get set up with this and then you can use this as a building block to create far more complex automations let's get started I've set up a webflow account from scratch that we can use for this and I have this air table base where I have the article title and the article text I just have some dummy text in here with some formatting and a featured image which I just generated using flux one of course you can generate this using AI we have multiple blueprints on our YouTube channels as well as in our community where we go far more into detail with this but I'm keeping things simple to start with so you understand how the integration works and then you can adapt it to the more advanced use cases later to get started all we need to do is go to air table and I'm going to select search records going to go all the way down to this webflow base that I've just created I'm going to select my table of posts you see in my air base here I have the article title and I have the status so this status has options of open and publish the web and publish so three statuses and then the article text and a featured image as an attachment type I want make to pick up records where the status is published to web flow go to formula open a curly bracket status equals to publish to web flow and I'll go limit of one for the moment to only pick up one record every time I press run once and there we go it's picked up this record which is great now I select this plus button here and I type in webflow I'm going to select show more and go to create an item so we want to create an item for a collection when you're doing this the first time around you need to press add and then I'll click save and then a window like this will pop up I'll just check the boxes and press authorize app perfect that looks good so that's really really fast to get set up now we just select our website and the collection will be blog posts and the name of the blog post will be the article title from a table and the post body will be the article text and we'll just do that to start with for the image all we need to do is pass the URL from Air table and then web flow will grab that image and then store it on its own servers which is very handy so that's a quite a quick way to get up and running with this sometimes it's more difficult than that for other website Builders so that's really useful so now we have the featured image URL I'm just passing the same image URL which is this image to both the URL and the thumbnail image this will be the thumbnail and then the URL will be the bigger image in the blog post I'm just passing both of these for the moment you could also use the make.com res size module to make a smaller version of the image I'm just keeping things simple for the moment so I'll press okay press save and I'll press run once now I'll go to the CMS section in web flow here and go into this I will view the content of the blog post I'll mark that as published and then we can look at that then I'll just refresh the page the image has shown up and the article title has shown up but the text is shown up in this markdown format as you see here so how can we improve this as you see here we've used this air table formatting and when it comes through to make.com you see this article text it's in this markdown format style so what we can do instead is add a module here and go to markdown and then Mark down to HTML and then we'll select the article text from there I'll press save and then I'll go down to the web flow create an item and then instead of passing the article text from Air table I'm going to pass the HTML from this markdown module I'll press okay press save and then I'll run once again so we'll have a look at response there which looks okay to me I'll go back to the CMS okay this is the second version of that and that is now looking a lot better we have text we have bullet points and a heading of course you can then update spacing and whatever you want from within the webflow page builder when I open this image in a new tab I can see that that image is stored on web flow servers which is perfect finally we want to update this status on air table because otherwise this integration is just constantly going to be picking up the same article again and again and again so we go to add a new module I'll select air table I'll select air table or search for it if required and then I'll select update a record I'll select this webflow base table of posts the record ID will be the ID from the starting module in the search records and the status I'll uncheck map here so that might be checked for you then I've moved this to published press okay press save and now I've added I'll add a limit of 10 here so it will pick up 10 at a time and there we go it's just pushed two articles to web flow so we have these two articles showing up and then this status has automatically been updated to published as you can see it's super easy to upload content items to web flow using tools like make.com and you can use virtually any data source if you want to get way ahead in your AI automations then check out the link in the description to our community we'll get access to all of our automation templates you get access to all of these courses and more are on the way and you can get support from us directly bya our live workshops and our active Community thanks for watching
