---
title: "How to Fetch Wikimedia Commons Images with Make.com (with Attributions)"
video_id: "46m7FE16d98"
youtube_url: "https://www.youtube.com/watch?v=46m7FE16d98"
publish_date: "2025-01-20"
duration: "11:15"
duration_seconds: 675
view_count: 589
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_wikimedia_commons
  
  Connect make to Wordpress: https://www.youtube.com/watch?v=SQsFd6xIyY0
  How to upload images to Wordpress: https://youtu.be/P58OvNdpPYk
  
  Our more advanced blogging automation tutorials:
  https://www.youtube.com/watch?v=6wJaqpJyswA
  https://www.youtube.com/watch?v=sJ4QrtWwkBA
  
  URL for HTTP module (I've added spaces after the "https://  " here so the URL shows up correctly, remove these spaces when pasting into Make.com!)
  https://  commons.wikimedia.org/w/api.php?action=query&generator=search&gsrsearch={{1.query}}&gsrnamespace=6&prop=imageinfo&iiprop=url|user|extmetadata&format=json
  
  Chapters:
  0:00 - Introduction
  0:50 - Setting up a Wikipedia Commons query
  1:30 - Parsing the response
  3:00 - Filtering results
  3:43 - Integrating OpenAI GPT for attribution
  6:20 - Uploading images to WordPress
  7:00 - Adding attributions to blog post
  
  In this video, you'll learn how to integrate Wikipedia Commons photos into your Make.com scenarios and upload them to WordPress as featured and in-content images. We'll explore handling attribution, which often comes in various formats, by leveraging OpenAI's GPT-4o to standardize and simplify the process.
  
  Starting with a basic Make.com scenario, you'll see how to fetch and parse image data, set up dynamic queries, and convert collections to arrays for more precise results. The tutorial covers creating robust workflows with filters to ensure only valid results pass through.
  
  Discover how to automate attribution formatting using OpenAI and implement SEO-friendly features like "nofollow" links. The process also includes using Make.com to map data for WordPress media uploads, preventing file overwrites by appending timestamps to filenames, and constructing HTML for embedding images and attributions in blog posts.
  
  By the end of this video, you'll have a comprehensive workflow to dynamically pull Wikipedia Commons images and metadata into your WordPress site.

yt_tags:
  []


# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Engineers"
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
  - "com (with Attributions)

in this video I'm going to show you how you can fetch Wikipedia Commons photos within your make"
keywords:
  - "ai-agents"
  - "ai-news"
  - "coding"
  - "frameworks"
  - "google"
  - "make"
  - "microsoft"
  - "product-management"
  - "prompting"
  - "tutorials"
  - "workflows"
---

# How to Fetch Wikimedia Commons Images with Make.com (with Attributions)

in this video I'm going to show you how you can fetch Wikipedia Commons photos within your make.com scenarios then I'll show you how you can upload those to Wordpress as both featured images and in content images as well as adding relevant attributions this image attribution data we get from Wikipedia Commons can be in a lots of different formats it's quite awkward so we're going to pass in the response into open ai's GPT 40 to give us a consistent response when you know how to do this you can adapt our bigger blogin automation scenarios so instead of grabbing AI images you can grab images from Wikipedia Commons which may be a lot more suitable to your use case okay I've started with a blank scenario here I'm just going to start by set in a variable the variable name will be query I'm just going to type in Birds I'm doing this to hard code the query we're going to send to Wikipedia generally you will be linking this to an air table or a Google sheet or some other trigger where you're passing in this value we need to add this URL into the request you can find this in the description of the video and then just update this GSR search after this section here you need to add in the variable or the reference to the data item for your query so that's what I add there then go down and parse response and everything else can be default this is a basic request right I'm going to click run once and see what response we get so we've pared the response and we go down to data query Pages we see we get a bunch of responses along with the image info and the URL so let's look at the first result we can get this URL looks good now if you just want to use those images without attributing the images I would not recommend that but if you are doing that then you can just use the output from that so the data query and pages and get the image info so what you can do is set variable we'll go to set variable and the variable name will be image URL and then go to data query Pages this so what you would do here is go up to arrays and you see we have this first option and the first option is going to return the first element of an array and then select Pages now let's just see data query pages is a collection I think it's first and then I think we need to change this to an array so two array so first off we get the pages response from Wikipedia we're going to return we're going to convert that from a collection to an array then get the first item from that okay let's work from there we we'll press run once okay we've got a response and then we have the image URL and value and image info and okay we got something right so let's say that we're going to use this we're going to upload this to Wordpress or something like that to test this out I'm just going to another set variable and then the value image info and URL so image I'm going to call this image URL I'm actually going to change this to first result sign out there's a bit of messing around there but I'm going to call this first result and there we go okay I'll press okay save I'll run again perfect so we have the value now I'm going to add a filter here because we do not want this to continue if there are no results so I'll go to if query pages and select exists and I'll just add results as the the name of that filter so I'll I'll press save now I'm going to just add in a big query that there should not be a result does it pass through this no that's perfect so let's go back we'll run this again that looks good so now we get a result so now we could just pass that image URL directly to Wordpress using the steps I'm going to show you later on but for the moment I'm going to remove these mod modes and then show you how to do the entire process of getting the image and getting the attribution and then uploading that to Wordpress so I'll click add a module and then I'm going to unlink these going to press shift down I'm going to just move those away from the scenario for the moment now what I want to do here is add a transform to Json object I want to get the first result from this similar to what we did already so I'm going to select this two array add that to the end and respond with the first one you could if you want to shuffle the responses and get and select a random result you could add in a shuffle module here and then that will Shuffle the array and then return the first one from that press okay looks good and save that next up we want to get an open AI module create a chat completion prompt going to select chat 40 latest now I'm going to add in a system Ro which will give the AI the exact instructions that we want so we've given very specific instructions for what we wanted this to do you will respond in Json format with the following values and I'm getting to respond in Json so that it will respond with multiple data items that then we can use in in the automation later it's pretty cool if you've not seen this already so it's going to respond with the image URL in plain text without the extension and the file extension like jpeg or PNG I'll tell you exactly why I'm doing that later but this is used to get around a quirk with the WordPress upload module so if you're not uploading this to Wordpress you might not want to do this maybe you could just get the full image name and URL then this attribution I'm getting this respondent HTML starting with this P image credit the attribution should be in plain text other than the link to the line license must include the attribution author license details and playe text available if link to a license then add the license name and link to the license with a no follow link if nonone available then respond with an empty string so this is no follow this is for SEO purposes it means that we're not going to pass the link juice to those pages and we'll retain it for our own website now for add message I'm going to add user Ro and then we're going to select the Json string that we selected over here then go then I'm going to go down to show advanced settings respond format must be in Json object par Json response press save perfect that looks good I'm going to click run once it's got the response and now it's passing that to open AI now if we go down here go to the result excellent so we have the IM the full image URL here looks perfect we have the file name and the file extension and we have the image credit which is perfect really that's the difficult part after this we're going to upload this to Wordpress so I'll select this HTTP module going to get a file I'm going to pass in the image URL so as you see here because we responded in Json format we we see these four different data items from that one open AI gbt 40 response so we do not need to have four separate calls to open AI which is a lot more efficient and just easier to work with I'm going to add in a label here which is if image URL exists and for image URL exists so we do not want it to go through this process if there's no image returned from open AI now we've now we will have gotten the httv data I'm going to press save just to make sure this map's in The Next Step under WordPress go to Wordpress and just type media I want to create a media item we have an entire video on this channel of how to upload images to WordPress but I'll just give you a crash course here you will select your WordPress connection again I have another video on how to do that instead of selecting this get a file mapping it's quite nice that make.com does this autom mapping but there is a quirk in this make.com module whereas if you have the same file name it's going to overwrite existing files on server which is not good so instead of getting the file name we're going to keep this data item mapping but we're we're going to use this file name that we got back from open AI we're going to add in an underscore going to go up here to the date and then add in a time stamp which really should make sure that we have unique values for this there's another approach I've talked about in the other video linked below but this should be perfect then finally go back up here and we'll select the file extension that's everything for now you can add these other fields if you want so I'll press okay press save after you do that you go to Wordpress and you then want to type in media again you want to get the media item and then select the media item id here press Okay the reason for this is that we want to get the actual image URL the publicly accessible image URL for that image that's been created in this create a media item module then finally we'll go to Wordpress create a post again make sure that you're using the same connection for title I'm just going to write this is a test blog post of course you will be populating this data with a dynamic value from Air table or generated by AI or throughout a more advanced process like in or other blueprints okay for the content of this post I'm just going to add in some test text at the start just to show that this is the start of the blog post this is the starting content of the blog post okay after that we're going to add in an image tag just to take a step back here if you just want to make the featured image the image that we just got via wik Wikipedia which is that you see here it's at the very top of the blog post then what you would do is go all the way down to the featured media ID element here and then select this media item ID from this create a media item module which was this here so if you want to upload this as a featured media item you actually do not need to add this step to get the media item because adding the media item via the featured media ID field here it will automatically map all of that but if you want to use the image within the content itself then you should use this get a media item module within this type drop down I'm just going to select post now let's say that we want to add this in as an in cont cont image what you do is just construct some HTML so we say image SRC equals and then go down and then select the source URL from that gam media Item ID and that's everything you need to display an image if you want you can add other things like alt text and titles and all of the rest after that we'll want to add in our attribution so just add in this just select your attribution that we got back from open AI we've already constructed the HTML so that should be good and you if you want the HTML to be in a different format just tweak the prompt from open AI earlier on finally if you want to add in the attribution for the featured image there are a bunch of different ways to do that but let's just say we could do featured image credit and just add that in the very bottom of the blog post so I'm going to add in a P tag and then a closing P tag and then select the attribution like we see here now generally you're probably not going to do both but just pick the one that you want so that looks good I'm going to press save I click run once to run the automation right that looks good we've got the file it's now uploading the file to Wordpress okay it's uploaded the file and it's created the post perfect that looks good we have the featured image we have just test text that I added at the start we have the in content image which looks good we have the image credit as you see here with clickable links that looks good but I just notice that these links are not marked as no follow within the code so I'm going to go in and be more specific in the promp in here with a no follow link so if link to a license add a license with a a link you must incl include a real no follow attribute to the link so okay press save I'll run that again okay that's finished processing and perfect that worked we have this real no follow tag as expected you'll see these image credits vary a bit from image to image the data that we get from Wikipedia can be quite different for this and also the way the AI constructs this image credit could vary a bit too so if you want an exact format for how you want them to appear then just update this prompt with the exact style of attribution that you want and you can provide some simple examples if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
