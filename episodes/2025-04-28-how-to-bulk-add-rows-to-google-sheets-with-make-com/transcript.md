---
title: "How to Bulk Add Rows to Google Sheets with Make.com"
video_id: "wWcqUdCBYCo"
youtube_url: "https://www.youtube.com/watch?v=wWcqUdCBYCo"
publish_date: "2025-04-28"
duration: "unknown"
duration_seconds: 0
view_count: 0
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our blueprints, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_bulk_add_rows
  
  Chapters:
  0:00 - Introduction to Bulk Adding Rows
  0:27 - Simple Example Setup
  0:42 - The Inefficient "Add a Row" Method
  1:53 - The Efficient "Bulk Add Rows" Method
  2:27 - Using the Array Aggregator
  3:51 - Configuring the "Bulk Add Rows" Module
  4:13 - Running the Automation and Observing Results
  
  In this video, I'm going to show you how you can bulk add rows to a Google Sheet in one operation in make.com. This massively saves on the number of operations used while also being a lot more efficient and quicker to run the automations if you're working with a lot of data within your scenarios in Google Sheets. The operations could stack up quite a lot, and by using a more efficient method that I'm about to show you, you could save a lot of money on your make.com plan. Also, the method I'm about to show you may also be relevant to other apps.
  
  I'll illustrate using a very simple example where I have a Google Sheet with a list of orders, and I want to export the rows across to another sheet. If you're doing this using a standard "add rows" module, it's going to have to call the Google Sheets API for every single row added. I'll start off by showing you the slow way of doing this and then afterward show you the better bulk add method.
  
  Next, I'll demonstrate how to use the "Bulk add rows" module in Google Sheets to achieve this in a single operation. To prepare the data for this module, I'll introduce the Array Aggregator, explaining how it takes multiple bundles (representing individual rows from the initial Google Sheet search) and consolidates them into one bundle containing an array of all the rows. I'll also touch upon a useful feature in make.com where you can define the target structure based on a subsequent module.
  
  Finally, I'll configure the "Bulk add rows" module to map the data from the Array Aggregator correctly and then run the automation to show how all the rows are added to the destination Google Sheet in one go. This method is not only more cost-effective for large datasets but also more efficient and less prone to API rate limiting errors.
  
  If you're dealing with significant amounts of data in your make.com automations, understanding and implementing bulk operations like this can be a game-changer for efficiency and cost savings.

yt_tags:
  []



# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Executives"
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
  - "# Unknown

In this video, I'm going to show you how you can bulk add rows to a Google sheet in one operation in make"
keywords:
  - "ai-agents"
  - "google"
  - "make"
  - "product-management"
  - "tutorials"
  - "workflows"
---

# Unknown

In this video, I'm going to show you how you can bulk add rows to a Google sheet in one operation in make.com. This massively saves on the number of operations used while also being a lot more efficient and quicker to run the automations. If you're working with a lot of data within your scenarios in Google Sheets, the operations could stack up quite a lot. And by using a more efficient method that I'm about to show you, you could save a lot of money on your make.com plan. And also, the method I'm about to show you may also be relevant to other apps. I'm going to illustrate using a very simple example here where I have a Google sheet and I have a list of orders and I want to export the rows across to another sheet. If you're doing this using a standard add rows module, it's going to have to call the Google Sheets API for every single row added. So, I'll start off by showing you the slow way of doing this and then afterwards show you the better bulk add method. I'm going to start by adding a module and selecting Google Sheets. I'm going to select search rows. Then in this case, I'm just going to select this orders sheet. I'll select orders. Then the sheet name is orders. Table contains headers. And I'll just leave all of that as default and press save. So this is effectively just going to pick up all of the rows from that particular sheet. Again, this is a basic example. You could filter those by a certain date, for example, or you could use the watch rows method to only watch for new rows that are added to the sheet and then run this on a scheduled basis. For the moment, I'm just using the search rows as a basic example. So next up then we'll go to Google Sheets and we'll now select this new orders received spreadsheet and I'll select add a row. Then I'm going to go to my drive and then choose the spreadsheet ID. Okay, I've selected my spreadsheet ID from there. Sheet name is sheet one table contains headers. From there I'm just going to map the values from the original sheet into this new sheet. So I'll select order ID and then total price. So this is effectively just going to copy and paste all the rows. So now let's run this automation. I'll click run once. It searched the rows and now it's adding those one by one. Then we see it's added all of those in. Now, instead of using this approach, let's add them all in one go. So, what we can do is delete this module and then we'll go to Google Sheets and then go to bulk add rows. From there, we'll then need to select our spreadsheet that we were just working from. So, we'll go to ID finder. I'll type in orders received, which was the file name. It should hopefully select that. And there we go. We have a spreadsheet ID. For sheet name, I'm going to deselect this map function here. Then, it should find the sheet name. Column range, I'm going to select A to Z. And then rows we will leave that as mapped. So from there make.com should know the data structure we need. I'll press save. Next we're going to use an array aggregator. Flow control and array aggregator. We have a separate video on our channel where we go through iterators and aggregators and to try and demystify those a little bit and I go through this example also within that video. So effectively what this is doing is Google Sheets when you search rows it's creating a lot of different bundles and each different bundle represents an individual row. Every time you have a bundle, it's going to execute those ex execute the rest of the flow once for every bundle. So that can really stack up the operations you're using and can stack up the number of times that an API can be called. What an array aggregator is doing. It's taking many bundles and consolidating those into one bundle. And that's effectively what we're going to do here. So we take all these Google Sheets rows. Then under target structure type, this is a pretty cool feature of make that I don't see used very often where it can take the target structure of a module later on in the scenario and try to map it to that structure. So I'm going to select rows and then from there you can select add value and add value and from there we can then define how we want to map these Google Sheets value to the new data structure which is pretty cool. So now in orders received, I'm just going to delete out the values from that sheet there. So we have order ID and total price. So column ID should be order ID and column 2 should be total price. Now I'm going to press save. And from there in the Google Sheets, instead of mapping back to the original module, I'm now going to map all of the data from the array aggregator. And this make sure that this is selected as map enabled. And I'm just going to select the array. So this is the array of data. So the array aggregator will create the data in the structure that we need and then we press save and then that should now be in the correct format. So now I'm going to press run once. It should hopefully pick it up. And now the data has been transferred hopefully. Yeah, there we go. And the array aggregator has successfully combined all of those bundles into one array and it's in the exact right format that's needed for this bulk ad module for Google Sheets. And there we go. We see that the update has been made. So to add all of these rows and there we go. They're all added and it's all been done in one operation. This might seem very trivial for 10 rows, but if you're dealing with many thousands of rows per day, that's going to stack up quite a lot in terms of your make subscription. And the fact that you're only hitting the API once every time you're running the automation means that you're far less likely to run into rate limiting errors and the automation should be a lot more reliable. If you want to learn more about iterators and aggregators, then check out the link in the description to another video on our channel. And if you want to get way ahead, then check out our community where you'll get access to all of our automation templates that you can import and customize to your own business. We have an active discussion board, a packed schedule of live events, and all of these courses you can get started with right away. Thanks for watching.
