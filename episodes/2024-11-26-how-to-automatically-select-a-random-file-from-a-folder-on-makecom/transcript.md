---
title: "How to Automatically Select a Random File from a Folder on Make.com"
video_id: "Avzv6Gthol4"
youtube_url: "https://www.youtube.com/watch?v=Avzv6Gthol4"
publish_date: "2024-11-26"
duration: "4:59"
duration_seconds: 299
view_count: 2028
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_random_folder_make
  
  In this video, you’ll learn how to select a random file from a folder in Google Drive—a seemingly simple but surprisingly tricky task. Whether you need to grab a random image for a social media post, a file for a blog post, or any other automation use case, this tutorial has you covered.
  
  What You’ll Learn in This Video
  
  Setting up your Google Drive module
  How to create a folder and configure file retrieval.
  Setting limits on the number of files to process.
  
  Working with arrays and bundles
  Using the “Search for Files and Folders” module to return an array of files.
  Aggregating multiple bundles into a single array for easier handling.
  
  Generating random file IDs
  How to use random number generation and the floor function to create an array index.
  Dynamically selecting a random file ID from the array.
  
  Downloading and using files
  How to download the selected file for further use.
  Examples of automating tasks like uploading images to WordPress or posting on social media.
  
  Expanding the workflow
  Connecting with WordPress to embed media files directly into blog posts.
  Adapting the process for various automation use cases.
  
  Key Takeaways
  
  Use Make.com’s modules to streamline Google Drive file management.
  Learn how random number logic can power dynamic automation workflows.
  Easily integrate downloaded files into platforms like WordPress or other tools for seamless automation.

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
  people:
    []
  products:
    - "Make"
  models:
    []
concepts:
  []
summary:
  - "# How to Automatically Select a Random File from a Folder on Make"
keywords:
  - "ai-agents"
  - "career"
  - "frameworks"
  - "google"
  - "make"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Automatically Select a Random File from a Folder on Make.com

in this video I'm going to show you how you can pick a random file from a folder on Google Drive it sounds simple but actually it's not that straightforward and this can be useful in cases where you might want to pick a random image to drop into a social media post a blog post it also doesn't need to be an image it could be random videos you're sent it on slack whatever the use case is if you'd like access to this blueprint so that you can import it at the click of a button like so then check out the link in the description to our community where you'll get access to all our systems and templates including our make.com masterclass where you can level up your automation skills so what we have here we have a Google drive module what I've done is I've created a folder on Google Drive just with 16 random images and I've set up my connection I've selected the location and the folder location there I've set the retrieval to files and then under limit I've set it to 100 so what I've done is I've set an upper limit there's only 16 in the folder but I've set an upper limit here and this is the search for files and folders module for Google Drive now this will return an array of items or bundles so for example if I just stop this here let me just put in one and zero and I'll press save if I run this I don't I I set one and zero there because I don't want it to go any further you can see if you open up that bubble that you have 16 different bundles so this is you know essentially 16 files and then I use an array aggregator to transform those bundles into an array so the input is 16 bundles and the output is one bundle with an array of 16 items okay so now if we zoom in on this module here this one is a random number between two numbers numers and the the variable value here is so we're looking at a random number which is a floating Point number between 0 and one times the length of the array so we have set 100 as the limit on Google Drive here but we don't need a random number between one and 100 because there's only 16 files so we're getting the length of the array here which is 16 and then we're multiplying a random number or a decimal between 0 and one times the number of items in that array and then that's going to give us a decimal so let me take out a calculator here so let's say the random number is 0 2657 multiply that by 16 we're going to get 4.2 and then the floor function Returns the largest integer less than or equal to a specified number so that's going to drop that from 4.25 down to four and then plus one at the end so that variable value will end up with five if 42512 is the number so you can test that out here press okay and run it and you can see five is the number okay so we'll put that back in again so it's random times the array length okay we'll save that up run it again and now you can see yeah we're getting seven we're getting 14 we're getting one Etc so here's a quick look at that value again so it's floor and then it's a random times the length of the array plus one okay so then we now have a number between 1 and 16 that's at random it's an integer as well so then in this module we're looking for a random file ID so then it's simply a case of opening up the array and we're looking at well we want file ID but the array index will be the random number that we just generated so again you can see here for in this instance the random file ID is this one if we run it again it's going to be a different file ID this one ends in TJ this one ends in uh xjt this one ends in Zer BR so that's how you get a random file ID from a folder of files on Google Drive what you do with that then is up to you you know so that could be a case of if it was a social media posting or if it was a WordPress post you were creating you can then download that image so downloads a file and you can drop in that file ID then that you just created so if we save that and Runner you can see it's downloading the file to make and that will then give you the full binary data that you can then for example create an image on WordPress or upload to social media for example so how that would look on WordPress for example just out of interest um you would pick WordPress and you're looking for media so let's create a media item this requires a a binary stream which is now what we have because we've used this downloader file module so you would press map and then the data well actually sorry that was it yeah you can see the data here it's essentially this binary representation of that image so that's data and then you would have the name as is and that's pretty much it that's how you would upload that media item to Wordpress and from there then you're going to get a WordPress media ID that you could embed in a WordPress post that's how it would work if it was a WordPress that you were trying to embed a random image into that will differ dependent on your use case so that's it if you found that useful then check out our automation Community my brother Alan and I run the AI automator where we have in-depth AI automation courses we have a make.com masterclass where you can learn things like this select a random file we also have a wide range of system templates built mostly on make.com that can do everything from blog automation social media automation video automation lead gen automation Etc and then we also have lots of micro templates so you can connect and plug and play lots of different services so check out the link in the description for that we'd love to see you there thanks for watching and I'll see you in the next one
