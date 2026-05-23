---
title: "Stop Duplicating Workflows! Try This Make.com Solution"
video_id: "yEk-y5DtRfk"
youtube_url: "https://www.youtube.com/watch?v=yEk-y5DtRfk"
publish_date: "2024-12-05"
duration: "5:40"
duration_seconds: 340
view_count: 5313
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_converger
  
  In this video, I show you how to stop duplicating workflows in Make.com and streamline your automations! If you’ve ever struggled with adding or updating rows in Google Sheets or Airtable without creating messy, duplicated logic, this is the solution you need. 🚀
  
  With the Converger Pattern, you’ll learn how to:
  ✅ Check if a record exists in your database or Google Sheet.
  ✅ Add new rows or update existing ones – all in one workflow.
  ✅ Avoid duplicating modules and keep your automations clean and scalable.
  
  Converger Documentation: https://www.make.com/en/help/modules/converger
  
  Make.com doesn’t have a native module to merge tracks, but with this clever workaround, you’ll build smarter workflows that save you time and effort.
  
  🔧 What you’ll learn:
  
  - How to use routers, variables, and iterators.
  - A step-by-step guide to implementing the Converger Pattern.
  
  🚀 Ready to level up your Make.com skills?
  Join the AI Automators Community for advanced tutorials, system templates, and access to our Make.com Masterclass.
  
  💬 Got questions? Drop them in the comments! Don’t forget to like and subscribe for more videos on AI, no-code, and automation.

yt_tags:
  []


# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI News"
difficulty: "Intermediate"
audience:
  - "General"
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
  - "com or if you'd like access to boilerplate blueprints for full systems using air table using AI automations and make and we also have a make"
keywords:
  - "ai-news"
  - "google"
  - "make"
  - "workflows"
---

# Stop Duplicating Workflows! Try This Make.com Solution

I've got an interesting use case here that one of our community members come across and we come up with a bit of a solution for it and it's a case where you're Gathering lots of data on a regular basis and you're saving that data to the likes of Google Sheets or air table and when you process each row of that data you need to check does the row exist already in the database or in the sheet and if it does you update the row and if it doesn't you create a new row so that's the kind of situation and that's typically handled with a router in make so let me just show you this so this is a test sheet that I have and I'll delete that out and if I run this I have a node here just kind of creating some dummy data so here it's just like a a campaign let's say an ID and a metric or a number and we have three of them and then we're searching in Google Sheets to see does that ID already exist if it doesn't exist it goes and adds the row as you can see here if it does exist it goes and it updates the row so I just ran that and the add a row has triggered three times as you can see here and now for example if I just delete that out and even let's just reshuffle it and let's say now that this runs the next morning and if I click run once again it now has gone down this track to update three of the rows and it's added back in that number so perfect this update scenario is now working and if I look to let's say add more data so let me add another item here so this can be ABC we'll save that and run it again you'll see now that those three are actually going to update even though nothing is going to change and then the extra row is going to drop in there there's ABC and there's the number so this kind of create or update is now working the problem with it is that what happens if you are doing lots of things after this so let's say you have all of these kind of modules this large workflow and let's say that is connected here well now you're going to need to duplicate everything you're going to need to copy modules paste them here connect everything and then Within These if they're using kind of values from these modules you'll then have to remap so because we've copied from here they might be using the variables from this module because I've cloned these down here these ones now need to use the variables from this module so it's just a lot of dup application it's it doesn't look great if you want to make a change you need to make a change in two different places it's just not ideal so what we're missing is a converger module or a merger module so we have a router which splits off what we're lacking is some way to kind of reconnect these as you can see here and then you could kind of just follow on the track the problem is it's not possible in make to do this there is no native module to merge tracks back into a single track like that and is a shortcoming of the platform so there are a couple of ways around this and I'm going to show you just one way that we went through with our member in the community which is this scenario here so let me move up the trigger and we'll zoom in and let's delete out this again before even explaining it let's just run it and I'll explain what happens so all of this is the same as before except what we're doing here is we're setting a variable so if we jump in here we're setting the row ID of Google Sheets and we're actually resetting it to zero I'll explain that in a second so that's the row ID so the first row has come in from the array or from it could be a web service or whatever else it's hitting this router we have one two three streams there's no filters on these streams so it's going to go down each track for each item or each bundle in this iterator so the first one's going to go down is the search rows which is what we used a few minutes ago and it's going to search the table for that ID and then if it exists or if we get something back from this search rows module then we set the variable the row ID so this is a this stream is if the record already exists so then it jumps to the next stream and it gets that variable that we just set here so we're using the get variable module and if that variable is equal to zero it means that this hasn't triggered in other words a record doesn't exist so then it's tracking true here and it's going to add the row so it adds the row to the table as you can see here it sets the ID and then it sets the variable to that row ID so now at this point we have an ID in the sheet for a new record we don't have the metric then we come down to the third stream and we get the variable and the variable will either have been set here or it'll have been set there so we definitely have a row ID now no matter what so we can then go and update that row with the metric as you can see there and then I put in a text aggregator just to close this Loop because this is an iterator this is going to run multiple times for each record coming in from the service let's say so every time that it runs through we need to reset the variable because row ID is going to be declared here here or here so then the next time we run through this iterator it'll still be declared which will mess up the entire system so that's why this module here resets it to zero so that it can be set again so that's a very important module here so then the beauty of this system is we have this kind of design pattern to check if a record exists if it doesn't we add it and then we update it so then this is the main stream we don't need to duplicate the modules for stuff that happens after this so down here let's say we have all of these modules we can then just hook them up like this so we don't need to duplicate the logic the logic is still only declared once and there's only one place to update it so that's essentially the converger pattern they talk about it here on the make documentation they use a data store which I think is a is a bad idea you shouldn't really need to persist data for a single runtime um so I don't know why they recommended that if you'd like to learn more advanced tips and tricks on make.com or if you'd like access to boilerplate blueprints for full systems using air table using AI automations and make and we also have a make.com masterclass where you can really level up your make skills then check out the link in the description to our community the AI automator we'd love to see you there thanks for watching and I'll see you in the next one
