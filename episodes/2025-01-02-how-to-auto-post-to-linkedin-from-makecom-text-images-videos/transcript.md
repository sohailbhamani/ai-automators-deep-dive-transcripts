---
title: "How to Auto-post to LinkedIn from Make.com (Text, Images, Videos)"
video_id: "YZQDu-h3sI0"
youtube_url: "https://www.youtube.com/watch?v=YZQDu-h3sI0"
publish_date: "2025-01-02"
duration: "6:53"
duration_seconds: 413
view_count: 18523
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_linkedin_make_connection
  
  Our other tutorials mentioned in this video:
  
  Blogging + social media automation: https://www.youtube.com/watch?v=6wJaqpJyswA
  Social media system: https://www.youtube.com/watch?v=00qppWuIW-g
  Airtable instant triggers: https://www.youtube.com/watch?v=JD48oemRUJk
  
  Chapters:
  0:00 - Introduction
  1:25 - LinkedIn Connection and Text Posting
  2:50 - Image Posting
  5:30 - Video Posting
  
  In this video, we’re going to show you how to connect LinkedIn to Make.com.
  
  We’ll start by setting up an Airtable base with posts, images, and videos that are ready for publishing.
  
  Connecting Make.com to Airtable: Learn how to use the “Search Records” module to filter out posts that are marked as “Ready for Posting” in Airtable.
  
  Creating LinkedIn Posts: We’ll guide you through connecting Make.com to LinkedIn and creating automated posts.
  
  Handling Different Post Types: Set up different workflows for text, image, and video posts.
  
  Error Handling & Final Setup: Tips for troubleshooting and finalizing your automated workflow.
  
  Step-by-Step Guide
  
  Setting Up Airtable Base
  
  Create a table in Airtable to store your post text, type (text, photo, video), and media URLs.
  Mark posts as “Ready for Posting” when they are ready to be published.
  Connecting Airtable to Make.com
  
  Use the “Search Records” module in Make.com to filter records with the status “Ready for Posting.”
  Set a limit of one to process posts individually.
  
  Creating LinkedIn Posts
  
  Add a LinkedIn module in Make.com to create a post.
  If it’s your first time connecting, authenticate your LinkedIn account and select the page you want to post to.
  
  Map the post text from Airtable to the LinkedIn message field.
  
  Handling Different Post Types
  
  Add a router to split the workflow based on post type.
  For text posts, directly publish to LinkedIn.
  For photo posts, use the HTTP module to download the image and then upload it to LinkedIn.
  For video posts, use the video URL to upload directly to LinkedIn.

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
    - "LinkedIn"
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "com (Text, Images, Videos)

in this video I'm going to show you how to connect make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "frameworks"
  - "google"
  - "linkedin"
  - "make"
  - "tutorials"
  - "workflows"
---

# How to Auto-post to LinkedIn from Make.com (Text, Images, Videos)

in this video I'm going to show you how to connect make.com to LinkedIn so that you can autopost text photos and video posts directly from an airtable base of course you can use the concepts learned in this to connect from Google Sheets and lots of other different automations including ones that you'll find in our main Channel and our community like this blueprint to autocreate blog posts and share them social media and you'll also see LinkedIn in this second step of our social media system from this air table base you can add in new records add in the post text select the status so you can mark it as ready for publishing you can select what type of post you want either text photos or videos so in this case we have this video post and when you run the scenario it can be run on a scheduled basis or you can use instant triggers we have a separate video on that it will then post that content directly to LinkedIn in this video I'm going to show you step-by step exactly how to do this and by the way if you want to get access to all of our.com blueprints then check out the link in the description to our community we'll get access to all of our automation templates including this one to get started I just have this blank LinkedIn account that I just set up for demonstration for this and I have an air table base this is where you can put in whatever text you want images and videos and then once you've moved them to ready for posting this scenario will then pick up those and then send them to LinkedIn this serves as a really good building block for us to understand the connection from make.com to LinkedIn and then you can really understand how to integrate this into things like our social media system or our more in-depth blogging and social media system first off we just want to connect to LinkedIn using make.com and then we'll just send this first test post so I'll select ready for posting I will go to air table and search records now of course you could use Google Sheets or another Central repository for this I'm going to use air table because it's a nice structured tool that we can use I'm going to select no view I'll uncheck all of these boxes so it will provide all of the fields formula we want to select status equals ready for posting I think that is our status so ready for posting so it will it will pick up any of these records that are marked as that select one for the moment so it will only pick up one at a time whenever we click run so I've select run ones and that is picking up the correct post which is good now next up we want to add a LinkedIn connection so go to LinkedIn and we will create a user text post I'll click add at the top here I'm going to type in test ACC CU this is a test account press save then it will show up with this popup I will click allow and now we are connected which is great so what we do is all we do is select the pulse text from the LinkedIn field and that is everything visibility public for the moment I'll select only my connections as visibility just so it does not show up publicly and feed distribution of Main feed okay I'll press okay now we'll press run once and see if that worked excellent I've gone to this profile and now we see that there's a new post here which is great this is the test post excellent so I will now delete that now what we want to do is to add in a router and it will follow different flows depending on if it's a text post or a photo post or a video post now that we've added in a router we want to add in a filter here so we condition where St where post type is equal to text post so now it will only go down through that route if that is a text post I just types text post here so it will show up on the filter which is good now we select another route where label is image post that is or sorry photo and video so we're post type equal photo and I'll just add another one that we will work on later for video where post type is equal to video now importantly once it's posted we want to make sure that it updates the status of that to published so it does not keep posting it again and again so I will go back to this and go to air table and then update a record I'll select the first base that we were working on the correct table and the record ID should be the ID from the first module this module here then status should be published so I'll just type published or actually we should be able to select the status even better so select the status there and press okay perfect so that means that when it's published it will update the air table record I've just moved that to published for the moment and we'll test out this that update in an air table record part here in the next flow of the scenario which is to publish a photo post to LinkedIn now I'll click plus go to LinkedIn and create a user image post as you see here I've I have this generic AI Workforce image on air table what we need to do is we need to get the file from Air table first as you see here once you've made the connection we have to map the file name so we cannot just pass a URL we need to actually map the data what we do here is we add a new module and select or I'm just going to type in get a file get a file there and the URL will be the image URL from a table so sorry so go to image and then image URL press okay and now that should Auto map to LinkedIn so I'll press save first and there we go it's Auto mapped which is great so that's perfect it's mapping the file correctly which is what we want you could add a title alt text and extend this air table base but for the moment let's leave it at this and the content will be the post text which will be this pulse text here then visibility only my connections for the moment of course you'll probably want to make that public press okay after that we want to clone this module bring it down and then that will perform the exact same function of moving the status to published within air table so I'll press save now let's test that out we'll go and move this to ready for pting press run once go back to my and we see this is now a new photo post which looks good delete that again and finally we want to push a video what I'm going to do is I clone these press copy modules press paste down here and I'll delete that module I realize I need to just update that filter again so it only goes down to this if it's a video and now I'm going to get a file which is a video URL here and as you see in this air table I have this just generic video that I'm just testing out and instead of create a user image post I'm going to replace that with press delete LinkedIn and get a user video post now I need to update my permissions in order to push videos to LinkedIn now I'll press allow for this perfect so that worked again it's automatically map the file so I've selected get a file content post text only my connections press okay okay that looks good finally I will move this to ready for posting and select run once it goes down through this route as expected it's now creating that user video post looks good it's now marked as published now we go down through here we see it's posted this video which is what we want and it has the correct test video post text as you see here and if you want to get way ahead in your AI automation Journey then check out the link in the description to our community where you'll get access to all of our automation templates some of which include LinkedIn automation you'll get access to these courses with more on the way and you can join our workshops to get support from us directly you can interact with us and others through our online community check out the link in the description if you want to learn more thanks for watching
