---
title: "How to Connect a Personal Google Account to Make.com"
video_id: "SH00Q8T-wQg"
youtube_url: "https://www.youtube.com/watch?v=SH00Q8T-wQg"
publish_date: "2025-03-03"
duration: "6:04"
duration_seconds: 364
view_count: 4414
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_personal_google_account_connection
  
  Make.com documentation for this:
  https://www.make.com/en/help/connections/connecting-to-google-services-using-a-custom-oauth-client
  
  The redirect URI needed: https://www.integromat.com/oauth/cb/google-restricted
  
  Scopes needed for Gmail and Google Drive
  Gmail
  https:// mail.google.com
  https:// www.googleapis.com/auth/userinfo.email
  
  Google Drive
  https:// www.googleapis.com/auth/drive
  https:// www.googleapis.com/auth/drive.readonly
  
  If connection a personal google account to make.com you might get the following error: It is not possible to use restricted scopes with customer @gmail.com accounts. For more information on how to connect restricted scopes visit our documentation.
  
  This video gets around the issue by setting up a Google Cloud console project so that you can connect your accounts without any issues. There are some steps involved, but once you have it set up then it should work no problem!

yt_tags:
  []


# AI-enriched metadata
content_type: "Tutorial"
primary_topic: "AI Strategy"
difficulty: "Intermediate"
audience:
  - "Product Managers"
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
  []
keywords:
  - "ai-agents"
  - "ai-news"
  - "google"
  - "make"
  - "product-management"
  - "tutorials"
  - "workflows"
---

# How to Connect a Personal Google Account to Make.com

if you're trying to connect to Gmail or Google Drive via a personal Google account so a personal Gmail account as opposed to a Google workspace account you need to go through some additional steps in order to connect those up so if you're seen a message like this and you're using a Google personal account then this is how you do it you're going to need to connect via console. cloud.google.com then go to select a project and new project at the top right then go in and add in your project name so you can call this whatever you want and then assign it to an organization it can be no organization if you want then let's just wait for that project to be completed that should take a few seconds and then you can go select that project to the top right then under apis and services on the left go to enable apis and services and then go to enable apis and services at the top and then to start off with we're going to search for drive then go to Google Drive API and then press the enable button to enable this API then just wait for that to be enabled then on the left hand side go to view all products then go to Google Au platform from here we want to enter in an app name you can enter in whatever you want such as make then enter in your email address then click next then select external and click next then add in your email address again and click next then click agree and continue and then click create from there go to Brandon on the left hand side then scroll down to authorized domains add in make.com and integromat docomo domains then press save enter your email address to the bottom press save add in your email address under the add users press save then go to data access on the left hand side go to add or remove Scopes and then select your Scopes so we're going to start off with Google Drive API so just type in drive and then from there we're going to search uh or we're going to select the Au Drive scope and Au Drive readon scope then scroll down from there and press save or update rather then press save at the bottom left from there we need to create a client so this will be a web application name it whatever you want such as a make web client then go down and select add URI so we're going to add this URI as you'll see in the video description this Google restricted URI then we press create and then we'll see the client ID and the client Secret so both of those will be on the right hand side you can select download o client once you do that the client ID and the client secret will show up here which you can copy out so copy those out and you paste those into make.com into the client ID and client secret sections and then press sign in with Google then a pop will show up just press continue from there you'll need to select your email address first so then just press continue from that then press continue again then you'll need to select the scope so just check all the boxes from there and press continue perfect now we'll just wait for the connection and there we go you should be able to do whatever you want within make.com such as we're going to add in a new folder here as a test we're going to press run ones then we'll go to Google Drive refresh the page and go to my drive and there we go that test folder has been created so that shows that we have a successful integration even though we're using a personal project next up we want to enable the Gmail app or the Gmail API go to enable for that we'll just wait for that to be enabled under you under the account then go to data access add remove Scopes from there we want to select the Gmail so just type in Gmail in the filters and I'm just going to enable all of those scopes from here so I'm just going to select all rows then go to the next page and select all rows again then I'm going to scroll down and press update then go on to the very bottom and press save there are some extra Scopes here but you can ignore those we're using those for a different automation platform now I'm creating a new Gmail module so I've selected this module now I'm just going to add in this account I'm going to select the previously created account that I have a continue notification showed up and now on this up press continue when it shows up press continue again and there we go just scroll down and press continue if any boxes or check boxes show up again check those press continue and from there you should be able to create your own uh Integrations whatever you want to do with Gmail such as uh adding a draft email sending an email whatever it is you want so in this in case we're creating a draft I just added some test data to that I've pressed run and you see the message uh output is correct or it's shown something anyways so now I'm just going to go into Gmail and there we go we see this test email that has been sent from make if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from all via our live workshops and through our active discussion boards
