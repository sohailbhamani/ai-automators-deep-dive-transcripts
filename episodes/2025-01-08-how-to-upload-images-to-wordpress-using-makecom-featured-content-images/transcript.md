---
title: "How to Upload Images to Wordpress Using Make.com (Featured + Content Images)"
video_id: "P58OvNdpPYk"
youtube_url: "https://www.youtube.com/watch?v=P58OvNdpPYk"
publish_date: "2025-01-08"
duration: "8:04"
duration_seconds: 484
view_count: 9576
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_wordpress_images
  
  Connect make to Wordpress: https://www.youtube.com/watch?v=SQsFd6xIyY0
  
  Our more advanced blogging automation tutorials:
  https://www.youtube.com/watch?v=6wJaqpJyswA
  https://www.youtube.com/watch?v=sJ4QrtWwkBA
  
  In this video, learn how to automate uploading both featured and in-content images to WordPress using Make.com. This simple setup uses Airtable to store images and builds the foundation for more advanced blog automation workflows.
  
  Chapters:
  0:00 Introduction
  0:34 Setting Up Airtable
  1:50 Wordpress Post
  2:30 Featured Images
  5:30 In-Content Images
  7:21 Finalizing Automation
  
  Key Takeaways:
  - Initial Setup: Use Airtable to manage article titles, statuses, and image URLs.
  - Automating Featured Image Uploads: Configure Make.com to retrieve featured image URLs, map them to WordPress media items, and attach them to posts.
  - Handling In-Content Images: Automate the addition of in-content images with unique file names to avoid overwriting existing media.
  - Improving Post Content: Convert markdown text to HTML for better formatting and embed in-content images into the post body.
  - Automating Status Updates: Update Airtable statuses after successful uploads to prevent duplicate operations.
  
  Step-by-Step Process:
  - Prepare Airtable Base: Include fields for article title, text, image URLs, and status (e.g., Publish to WordPress).
  - Set Up Make.com Scenario: Create a scenario to fetch Airtable records with status "Publish to WordPress" and limit processing to one record at a time.
  - Automate Featured Image Upload: Use the HTTP module to retrieve image files, map them to WordPress media items, and attach them to posts.
  - Automate In-Content Image Upload: Follow the same process for in-content images and embed them in the post content using HTML img tags.
  - Update Airtable Status: Add a final step to update Airtable status to Published, preventing duplicate uploads.

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
    - "Claude"
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "com (Featured + Content Images)

in this video I'm going to show you exactly how to upload images to Wordpress via make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "anthropic"
  - "claude"
  - "make"
  - "product-management"
  - "tutorials"
  - "workflows"
  - "youtube"
---

# How to Upload Images to Wordpress Using Make.com (Featured + Content Images)

in this video I'm going to show you exactly how to upload images to Wordpress via make.com the process for uploading featured images and in content images varies a bit and I'm going to go through both of these within the same scenario I'm going to keep this as simple as possible using an air table base where we're storing the images within the air table base once you understand how to do this then you can move on to our far more advanced blogin automations where you can do things like building an article out section by section using open AI gbd4 Claude or open router if you want to get access to all of blueprints including the one in this video then check out the link in the description to our community let's get started I have an air table base here where I have the article title the article status once this is marked as published to Wordpress we want the automation to upload the images to Wordpress through this automation we'll also upload a blog post and attach those images to the blog post but if you only want to upload images you can just use that part of the automation so I've opened up a new scenario in make.com I'm going to select air I just type in air table and I'm going to select search records if you do not have a connection and press add and go through the authentication process so I'm selecting my air T base here that I just created and the pulse table is what the name is called and it's called post table I'm leaving everything else blank here and then for formula we want to pick up records where the status is equal to publish to Wordpress so I'm going to open up a curly bracket and type status equals publish publish to Wordpress I'm going to limit it to one for the moment so I only want to pick up one record every time I press run one once going to press save press run once and we see it's correctly picked up this image so we have this content image and we have a featured image the process to upload a featured image in WordPress is different to that of uploading a Content image like an image within the content of the blog post I'm going to cover both in this video first off I'll start with how to upload a featured image so we'll go to Wordpress and we'll select create a post I've already covered how to create a WordPress Connection in another video on this channel so check out the link in the description if you need to do that from scratch so I've selected my connection here for title I'm going to select the article title from WordPress the in article content will be this article text which is this here we'll need to make an update to that after but I'll start with this so for type I'll select posts so then you see we need this featured media ID unfortunately we cannot just pass a URL to this so we'll press okay and then we'll add a separate module here we select WordPress and then we will select create immediate item then we need to map that data in order to map the data make.com needs to grab the image data from Air table and then pass that to Wordpress so I'll select add a module here and then select get a file so the HTTP module of get a file then from this in the URL I'll start off with the featured image then I'll select this URL of featured image and then once we press save press save anyway then this should automatically map should be the operative word press save and it still did not I press save I'm going to refresh the page page again okay it's m the file however there is a quirk for the make.com app for WordPress which means that we need to manually Define the file name the reason being that if you pass a file name that already exists on your WordPress site this will automatically overwrite it and that could override images that are on previous blog posts which is not good that's a really serious shortcoming that they really should sort out but for the moment what we can do is just use a different file name so I'm going to use the title of the blog post but I also add in a hyphen and go to the daytime functions and select now which is the current time and just to keep things simple I'm going to add in jpeg at the end because I know that's the extension of the file names I'm uploading you can make it more complex than this but we'll do that for the moment and I'll press okay then finally for this create a post in WordPress we'll go to Media item id we'll press okay then we'll press save that by itself should be enough for us to upload featured images so it's got the file it's now about to create a media item and it's creating a post there we go we have this post we have the image and we have the text although the text is in markdown which we can improve so let's keep going with that I'm going to press shift I'm going to right click add a module select markdown mark down to HTML that being that if we look at this we see this is all in formatting but once we receive that in make.com it gets sent via markdown which is not in a format that WordPress can recognize so if we select the article text within this markdown to HTML then instead of passing the original article text from Air table we pass in the result of that markdown to HTML module then that should be good from there so let's try that again again it's create an immedate item now the text is in much better format before we work with these content images I want the automation to update the status of this so it does not keep pushing the same articles again and again to Wordpress so at the very end of this automation we select air table and select update a record we'll select our base again this WordPress image test base select posts for the record ID I'll scroll all the way down to this search records module and that's the ID from the very start of the scenario and then for status I'm going to uncheck the map here and Status should be published so from now on every time we run this Automation and it picks up one of these it will automatically change that to published and you'll see that in a second but for now we now want to upload the in content image as well in order to understand the differences between these I'm going to rename these modules to get featured image and then upload featured image then I'm going to press shift and drag I'm going to copy these modules and then paste modules in then I'm going to unlink this and then link this into the flow and I'm going to change this to get content image and then upload content image then within this I'm going to change the reference from featured media URL to this content image URL and then I'm going to upload the content image which is content image 8 in this case for the file name I'm just going to use the article title again and add two to it and it will then also append the current date time to the very end of the file name again this is all just to ensure uniqueness to make sure it does not overwrite existing images so I press save when it uploads the content image we're going to get back a image ID and maybe some other information but it will not give us the direct image link so what we need to do then finally is to go to Wordpress and get a media item and the media item id will be this previous media item id where we uploaded the content image I'm going to rename this to get content media item and press Auto align so before we add this content item to the post we're going to unlink this and I'm going to do a test to upload the featured image and the content image to the site okay that looks good now I'm going to link these again so that has worked we have a source URL here which is good so I'm going to link those back again and then within the WordPress post content we're going to then add the content image to this post content so I'm going to open up an image tag this is using HTML but it's really really simple so Type image SRC and then close that off so the SRC will be the source names that's the source of the image you can add other things like Al text but for the moment this is all you need to just render the image so I press okay press save and from there this should be everything we need to get featured and in content images so I'm going to run that once and then let that work away there we go we have the featured image and we have the text and an in content image at the very end of the article of course we can get far more complex with this build the article section by section you can add in internal links you could add images per section add YouTube videos whatever else you want we've multiple bloging blueprints on our channel that you can check out as well as within our community but this more simple automation should give you the building blocks you need to create more complex automations and if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates including the one in this video you get access to all these courses as well as more on the way you can get live support from us via our weekly calls as well as through our active discussion boards
