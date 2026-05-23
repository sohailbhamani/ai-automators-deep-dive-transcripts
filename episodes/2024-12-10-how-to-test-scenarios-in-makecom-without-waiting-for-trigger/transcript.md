---
title: "How to Test Scenarios in Make.com (Without Waiting for Trigger)"
video_id: "UW5MVP5YAIU"
youtube_url: "https://www.youtube.com/watch?v=UW5MVP5YAIU"
publish_date: "2024-12-10"
duration: "8:47"
duration_seconds: 527
view_count: 3357
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_test_scenarios
  
  Discover how to test automations in Make.com by using previously processed data. No need to wait for external events—learn how to simulate triggers like webhooks and Make.com app integrations with ease.
  
  Easily transition between testing and production without altering the original workflow.
  
  Save time and ensure robust scenarios for critical automations like external payments or task management systems.

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
    - "Slack"
  people:
    []
  products:
    - "Make"
    - "Projects"
  models:
    []
concepts:
  []
summary:
  []
keywords:
  - "ai-news"
  - "frameworks"
  - "google"
  - "make"
  - "projects"
  - "slack"
  - "tutorials"
  - "workflows"
---

# How to Test Scenarios in Make.com (Without Waiting for Trigger)

in this video I'm going to show you how to test your scenarios by sending in data that was previously processed which means that you will not have to constantly wait for the external events to happen in order to actually test your scenario because it's just not always practical to do so for example you could have a web hook which is listening out for a payment from a customer or for some other type of external event which is hard to replicate so I'm going to show you how to process data again even if you're using either web hooks or if you're using one of make.com many internal apps such as this slack app first off I'll explain how to test this scenario which is very simple but the concept works for far far more complex ones I'll show you how to test this without waiting for the external trigger in this scenario it simply is waiting out for an external system to send it data and then it will update Google Sheets with the task name and task description so let's just say this is like a task management system like a clickup for example what you can do is go to history and and look at a previous execution of that go to this bubble icon and click download output bundles and just press control A and contrl C this is a basic example in many cases there will be far more data than this but the same concept applies then we go into a new scenario and we select HTTP and we select make a request then go back to your main diagram and then copy and paste out that web hook address into your new scenario I'll paste that in and then for body type select raw content type Json and then copy and paste out the request content that you had copied from that past run so we'll copy in this request content and press okay now what we can do is we can click run once within this scenario click run once here and there we go it's triggered the scenario in the exact same format that we're expecting from the other system and now it has updated this Google sheet so again it's as easy just going into a past run of this downloading output bundles and adding that into a new test scenario and there you go you can now test that scenario without having to edit any part of your original scenario now let's say we're using a different scenario which is using one of mak's apps instead of using a custom web hook this example is using slack so what it's doing is it's waiting out for an event from slack what I'm going to do is I'm going to just add in a filter in here to stop the rest of the scenario from processing just add we just select one equals 2 so when this scenario is triggered it's not going to go pass this filter I'm going to select run once just wait for new data and I'm going to pass in data I'm just going to write in test now I'm just going to wait for that to pick up and a date excellent so that is good now I might actually test this properly because this what this is doing is it's extracting the first URL from the message so I'll test I'll pass that in and it'll wait for that and then this variable is going to extract the URL excellent so we have that there and then from there it could continue on with the scenario so now let's say that we want to to pass in that data without having to write this message we need to break this apart so what we can do is Select add a module so we're going to add a new module and then we're going to look for parse Json there we go parse Json and we'll break that apart pass that down there and then we'll just copy whoops what I'll do actually is move this down to there which means we're moving the starting point of the scenario to that and then I'm just going to copy and paste in this entire Json string into that now it would be great if that was enough but the problem is that these elements are actually mapped back to this original slack event so what we can do is break this apart and make it so that this is actually the starting trigger again and then we need to update this original scenario so what we can do is we can actually put that data into a variable so we go to add module and then type variable we want to set variable we're going to call that slack message okay and then in this we're going to copy this out which is the actual data item from the slack message copy that out to here so everything that's there will now be within this variable now you would think that you could just add in this slack message variable from there but unfortunately the way variables work in make.com is a little bit awkward so we need to get the value of that variable and I'll explain why in a second so the V variable name is slack message we're going to get that variable name and then that is what we're going to map to the rest of the scenario I know that might be a bit confusing but just stay with me for the moment and we're just going to call this I'm going to rename that of just get slack messages okay and within that then we map that to this slack message okay so let's test that out using the slack trigger initially because I know this is a little bit confusing now I'll press Rong once then I'll pass in manually for now this message again and great so what it's done is it's taken the message so it's got this slack message so this is exactly the data that we had initially put here directly we set the variable which is called slack message then we get the variable name again and then we map that any or else we have referencing this within the scenario we then reference that variable instead of referencing what was originally in slack let's say we want to change the starting trigger for this scenario to use our test data instead so what we do is we drag this down to this Parts Json and we break this apart so we're not actually setting the variable to start with from here we should be setting the variable from there what we can do is Click clone drag that down and then any references we then need to change so what we'll do is we will run this module only once and we see the result of this is now the exact same format as we expect from slack and a really easy to change this is to copy and paste this out into a notepad file and then to change the reference of that to 40 which is number 40 here if this is going to be in the exact same format of the original slack module then all we need to do is change the module number so we copy and paste this back in and there we go click save and now we'll try and test this out we click run once and excellent we now have that correct array now we map this back up to the original stream and because we've called this variable the same name slack message here slack message there then when it tries to get the slack message here it doesn't matter where it is originally been set where that variable has been set then it's just going to get either of those whichever one is connected to the stream and then we link this to our get slack as messages variable so this is linked to this get slack messages now let's test that out end to end from here to here click save and click run once and there we go we've successfully tested that that works which is that we've passed in a previous message that was sent via slack we've set the variable we get the variable here and the reference is now to the variable instead of to the original starting trigger so if you have a pretty complicated scenario anywhere where you are using data from your trigger you need to set that as a variable if it's only one item like this so in this case we just simply had you know a collection of messages that we were working off from here but if you were getting a bunch of different data items what you can do is actually set multiple variables so you could do set multiple variables you can add item add item and so on so you have your variable name variable value and do the exact same thing except instead of setting one variable you just set multiple variables so when you're happy with your testing what you can do is unlink link this back to your main stream and drag the starting trigger back to the slack new event and then you click save and then these just kind of stay in no man's land they're not going to be used but you can just continue on as normal with this so we'll click run once I'll pass in one of these test messages again except in this case I'll just change it to a slightly different message just to make sure and there we go we see URL of Bing which is the URL from this message if you have a pretty simple scenario that probably will not be very challenging to do if it's a very complicated scenario yes there will be some restructuring to do but it probably is worth it so that you can actually properly test things on actual code-based software projects developers can often spend pretty significant percentage of the time of creating test cases and to be able to structure their code in a way that can actually be tested and if you're working with a difficult trigger like you know external payments and things like that you really want to make sure that those are robust automations and why not just restructure your scenario a little bit just to make it easy for you to test whenever you need to if you want to get way ahead in your automation Journey then check out the link in the description to our community we'll get access to all of our automations it's an active Community where you can get your questions answered online or you can join one of our weekly workshops where you can get your questions answered directly from us thanks for watching
