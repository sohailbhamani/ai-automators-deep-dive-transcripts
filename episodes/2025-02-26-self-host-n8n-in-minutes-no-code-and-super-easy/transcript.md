---
title: "Self-Host N8N in Minutes! (No Code and Super Easy!)"
video_id: "0nYS2XP44k8"
youtube_url: "https://www.youtube.com/watch?v=0nYS2XP44k8"
publish_date: "2025-02-26"
duration: "7:30"
duration_seconds: 450
view_count: 3108
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our n8n & Make.com templates, courses, and resources here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=elestio
  
  Want to self-host n8n without the hassle? In this video, I'll show you how to deploy n8n on Elest.io, a fully managed DevOps platform that makes self-hosting easy—no coding or terminal required! 
  
  Elestio - https://elest.io/
  
  🔥 What You’ll Learn:
  How to deploy N8N on LSTO in minutes
  Choosing the right cloud provider (AWS, DigitalOcean, Hetzner, etc.)
  Configuring and optimizing your N8N instance
  Setting up backups, security, and performance monitoring
  How to manage software updates, logs, and more!

yt_tags:
  []


# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Strategy"
difficulty: "Beginner"
audience:
  - "Engineers"
  - "Product Managers"
entities:
  companies:
    - "X"
    - "AWS"
  people:
    []
  products:
    - "Make"
    - "n8n"
  models:
    []
concepts:
  []
summary:
  []
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-strategy"
  - "ai-tools"
  - "aws"
  - "career"
  - "coding"
  - "frameworks"
  - "make"
  - "n8n"
  - "product-management"
  - "workflows"
  - "x"
---

# Self-Host N8N in Minutes! (No Code and Super Easy!)

in this video I'm going to show you how you can self-host n8n on lso as you can see lso is a fully managed devops platform and it simplifies deploying open source software applications like n8n in the cloud by that I mean it handles the installation the configuration the automatic updates the security patches of your application and your server so you can focus on actually using the software for what you need it for these guys don't actually host the application for you they manage the deployment of the application on infrastructure so you still need to choose whether you want hosted on AWS digital ocean hetner lion Etc because lto brings in a layer in between the application and the infrastructure it means that it's good for no coders to get set up with self-hosting you don't need to actually get into the terminal and start deploying git repositories so to get started you can sign up for a free trial or just log in once you have an account so I already have a flow wise instance up and running here but let's create a new service and then you can just search for n8n which is there and click select and from here then you just need to choose a cloud provider and then choose what region you want your application hosted so from a data security perspective you might need this hosted within the EU or within the us so you can choose the locations here so you can also see how much it's going to cost on the right hand side here so estimated monthly price um and then as you change cloud provider or change region or plan that's all going to change so for this I'm going to choose hetner this is a budget option within Europe I'll choose the German data center I leave it at the smaller service plan as well so this will cost me around $15 a month and up on the right hand side here you can choose which version of n and you want to install so we'll just keep this at the latest version and then just click next and then you can configure your application and your instance so you have an option to configure a Network volume you don't really need it for kind of a basic implementation of NN then you also have other Advanced configuration options such as when you want software upgrades to be installed because that might require a level of downtime as well if you do want to actually SSH into this instance you can set your SSH keys there you can always do this after it setup as well so depending on how Mission critical this application is going to be you can purchase support to reflect that because I'm just testing things out here at the moment I'm just going to choose Level One support it's a 3-day response time in reality I think it's a lot faster than that but you are limited to email support okay so I'm going to click create service then you can see it's deploying the service okay and that's starting up now I found when I created the account initially there was a little bit of a delay in getting the account set up I think when I logged my payment card against the account I think they just go through Standard Security procedures which took some time it might depend on the time of day that you actually set up your account so if you click in you can see the moment the service has been deployed but I can already take you through some of the elements that you'll see here so you have an overview so here you'll be able to access the URL of your NN application and then a lot of what we've just set there in terms of the software version the service plan support levels the location is all here and can be modified or upgraded you can add a custom domain if you want and again you can change the times of software upgrades or or operating system upgrades Within These sections here great so our service is now up and running as you can see there I'll go through the rest of these tabs in a couple of minutes but if you just click on display admin UI and that's then going to load up the URL and you'll have your username and password as well and then you can easily copy them out so we'll just click into this if you'd like to level up your AI agents and automations then check out the link in the description to our community the AI automator where we have a large library of system templates active discussion boards we host a number of tech support workshops every week to help members out and we also have a number of courses to help you level up your n8n or make.com skills and then here is our nadn app so you set up your owner account and I've generated a password and then you can click next and that's it password saved so at the moment you can get these kind of additional paid features for free forever if you sign up to their email list I'm going to do this because the workflow history execution search and advanced debugging features are brilliant we use them a lot in NAD and Cloud so I've entered my application key and it has been confirmed I don't think this is actually technically necessary so if you view all plans they have these self-hosted plans like the free version because you're self- hosting it you can do whatever you want with it but then if you want it the more enterpris kind of features like collaborating on workflows single sign on L app stuff like that then you do need the the higher up plans from here I can now set up my workflows so maybe we come in and do a chat trigger then we'll do let's say an AI agent call a tools agent you know trigger a model maybe that'll be let's say open AI you can create your credentials so this is my open AI account which has successfully tested I think this is the real benefit of Hosting with the likes of ls. or the likes of render the server is configured to work specifically for n8n so this is like an n8n image so like everything like the firewall is set up whatever the application requirements are are being met by these images so so stuff should just work the way it's working here so memory I can choose Windows buffer memory which is in the instance we'll save that let's give it a click test we just say hello and there's our answer you know stuff like you can make the chat publicly available and to do that of course we need to activate the scenario so there's our chat there's your answer and then you know you can put in authentication so it could just be basic off we just do test test as a an example and there's your basic off so all of this is configured with these images so you don't need to spend any time actually within the infrastructure which is great so then to look at some of the other features here we've gone through this page and everything you need is in this display admin UI so you may want to change version let's say you may need to go to the beta version to access a new feature you may need to downgrade for example if something's no longer working in the newer stable version if you hit an error you can reboot reset restart the instance you can restart the software itself you can look at app logs to see is there any specific error that's showing up because sometimes larger workflows can throw errors particularly if you start kind of maxing out on memory and stuff like that so good to see that there you can access the dis if needed so they have this kind of files Explorer UI that you can kind of work through and look at the actual folder structure you can ssh in Via terminal as well then in terms of backups it's always good when you're sell hosed to actually take regular backups so you have automated snapshots here good to get them off dis as well because if this thing crashes you will lose your backups if they're only stored on the dis so good to get remote backups set up and you have a couple of options there one is AWS S3 and you can take manual backups every now and again just to get kind of snapshots then you can get key metrics just to see are your workflow is really stressing out the infrastructure all of that is there you can monitor how the server is progressing and if there has been any downtime you can check it out here so there we go then in terms of logs you can stream logs if you need them sometimes if you are hitting errors and you don't know what's going on it is useful to see the server logs it's very Advanced but at the same time you do have access to it Hees if full audit trail of of people's access within the platform you have access to the firewall if for whatever reason messages aren't getting in or getting out of the application and one thing that's really really useful here is the engine X configuration so if we just show config here now I really wouldn't go messing with this unless you know what you're doing but I have found that I have needed to extend timeouts of workflows um and I've done this here and finally you can enable alerts as well so if certain thresholds are hit in terms of you know CPU usage or memory capacity then you'll be able to get kind of notifications of that and you can go in and make some kind of changes to resolve the issue so this is more if you're running this in production and it's Mission critical and you need to get notified if there's downtime in the service or uh pending downtime and that's it it's pretty easy to set up most of this you will just never need usually then it's just a case of jumping head first into the application and just using it the way you would normally use it and probably the main ones you're going to use are maybe changing software version of NN or maybe just rebooting or restarting the actual infrastructure itself thanks for watching and I'll see you in the next one
