---
title: "I Built a Bing Keyword Research Tool Using Make.com and BuildShip"
video_id: "6Dza9qf5Ny8"
youtube_url: "https://www.youtube.com/watch?v=6Dza9qf5Ny8"
publish_date: "2025-01-03"
duration: "6:41"
duration_seconds: 401
view_count: 505
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_bing_keyword_research_tool
  
  Our original Google keyword research tool automation: https://www.youtube.com/watch?v=zn6Qiqkhf98
  
  In this video, we dive into using Make.com alongside BuildShip to streamline keyword analysis and build comprehensive Bing keyword reports.
  
  Follow along as I demonstrate the process.
  
  Setting Up Your Workflow:
  
  Starting with a Google Sheet, we demonstrate how to list URLs for analysis and pull comprehensive Bing keyword data.
  
  Using Google sheet's bulk mode, you'll learn how to save 1000's of Make operations when adding keywords to Google sheets.
  
  Integration with Make.com: A step-by-step walkthrough of integrating BuildShip to collect keyword data from each URL.
  
  Generating & Exporting Keyword Reports:
  
  Explore how reports are created in Google Sheets in a single operation, minimizing API calls and maximizing efficiency.
  
  See how reports show keywords, search volume, and competition level using the Data for SEO API.
  Cost Comparison: Understand the savings of using BuildShip and Data for SEO, with reports costing only a few cents each.
  
  🛠 Tools & APIs Used:
  BuildShip: For bulk automation and low-code customization.
  DataforSEO API: For ultra cheap, in-depth keyword data.
  Google Sheets: For report generation and storage.
  Make.com: To automate interactions between tools.

yt_tags:
  []



# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Tools"
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
  - "com and BuildShip

in this video I'm showing you a powerful keyword research tool for Bing and it generates full keyword reports for every single one of those in an incredibly efficient manner we coul"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "coding"
  - "frameworks"
  - "google"
  - "make"
  - "microsoft"
  - "workflows"
---

# I Built a Bing Keyword Research Tool Using Make.com and BuildShip

in this video I'm showing you a powerful keyword research tool for Bing and it generates full keyword reports for every single one of those in an incredibly efficient manner we could have a thousand roles in this report and it only uses one operation in make.com using the bulk functionality on our main Channel I showed you a version of this that I created for Google Search now it just requires a very small tweak to adapt this to use Bing instead if you are a member of our community go to the keyword research automation section in our system template and now I've updated that section to include this Bing template and you can generate your Bing keyword reports at scale you can get set up with that in minutes without having to write a single line of code at a high level what this automation is doing is it's watching out for new spreadsheet roles as you see here so it's just looking for a new URL and we should populate the number of results we want and the max position for those keywords we only want to show keywords that are in position 10 or better it's going to pick up each of those rowes one by one then we're calling a SE Bill ship project and this is where the magic happens within this automation Bill ship is a low code automation tool that offers a ridiculously generous free tier I've used it quite a lot and I've never had to pay for it in this case I've created this scenario that it receives a call from make.com then it extracts the number of results and Max position from there then it calls data for SEO directly from within this project this is call in the ranked keywords API endpoint from data for SEO if you've never used data for SEO before it's very powerful tool that a lot of other keyword tools actually use this as their main data source where you can get lots of really rich SEO data for example in this case we're getting data from the ranked keywords endpoint you can select whatever data you want and then when You' when you're done with that you can request check out the response and then go to this code example then you can copy out that code into the service you're using such as Bill ship or make.com in order to construct that request so you can see we've done that within the body of this request the root URL is the URL that we provided earlier on and then all of these other parameters are hardcoded in similar to what you see here I've added a bit more logic to the filters here but it's not explicitly required after that I got Chachi VT to generate code for me so what I did was I went into data for SEO I added in a request for playground here and then it come out with an example output that we're getting from data for SEO then I copied that into chat gbt and noted that I need to get the output in this exact format which is this values and values list format and then I asked it to provide the specific fields from the output and with a bit of back and forth I was able to get some work in JavaScript code that I could inject straight into this and that's great because I'm not particularly good at R in JavaScript and that gets around the limitation that make.com has massive limitations towards handling text and arrays and reports once it's done with that once it calls data for SEO pares the result and then returns back to our scenario then creates a new Google sheet so we have this create a sheet module and the title for that is just the URL so it creates this new spreadsheet for example this keyword report it just creates a blank sheet to start with after that it moves it to a folder so we have a specific folder within Google Drive we want to store all of these keyword reports so it moves that spreadsheet to a folder then after that this is where the magic happens here where we do a bulk API call so spreadsheet spreadsheet ID values a toz append so instead of using iterators and aggregators like a thousand times for a thousand roles we make one single API call and we add method of post content type application J and very importantly we have data this is the response data that we're getting directly from Bill ship which is as you see here values SE type keyword search volume so we do not need to Define What fields what roles or anything within make.com this is all handled within this because this code is constructing all of that for us then once it makes the API call it populates everything there and then updates the r on Google Sheets here for a link to the keyword report so as you see here I've hardcoded this URL here but I want to be able to update my make.com scenarios so that from one scenario I can ask it to provide Google data and the other scenario I want to ask it to provide Bing data so I've made a duplicate of this scenario and within this get keywords I'm send in the data for SEO URL that I want to Target within this playground we see search engine type of Google we can move down to Bing and go on to ranked keywords and then when we go down to code example we see the exact post URL that we need to hit in order to get that Bing data so I've just copied that in here then we're passing that to Bill ship and then within the bill ship scenario instead of hardcoding the data for SEO URL we want to provide I'm now getting that the data for SEO URL exactly as it's been provided there data for SEO URL so that's getting it from the request body which is this request body so now we could have two scenarios targeting the exact same bill ship endpoint here without having to create a separate bill ship project let's reprocess these from the start I have these URLs I'm going to go back to Google Sheets I'll click choose where to start and select all then I'm going to process these and I select run ones and you see how quickly it gets that data from Bill ship we already have the first keyword report done and the second one and the third one so that is ridiculously fast to update that many roles in one go using me.com we've gone to the first garage gym reviews report and we see we have all the keywords that it's ranking for in Google according to data for SEO the search volume the rank it has keyword difficulty for some of them and there you go you can add in as many URLs you want and it will just take a few seconds to process quite a lot of them you see I've passed in a single URL and it's still able to process that as well it shows the search volume keyword difficulty for some as well you may be wondering why I'm including some of these fields that are not being populate that's to keep it in the exact same format as our Google Keyword tool then you can merge these reports together and it'll work completely fine so that was relatively Advanced but it shows you that if you can piece these kind of systems together then you can overcome the limitations of no code tools like make.com and be far more flexible and efficient for outputting these kinds of reports if you want to get access to all of our automation blueprints then check out the link in the description to our community we'll get access to all of our automation templates including the one in this video you'll have access to all of our courses and more are on the way you can get your questions answered through our live workshops and you can post questions and discussion items through our community as well
