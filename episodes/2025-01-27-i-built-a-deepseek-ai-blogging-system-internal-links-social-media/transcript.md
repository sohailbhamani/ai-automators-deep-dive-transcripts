---
title: "I Built a Deepseek AI Blogging System (Internal Links + Social Media)"
video_id: "T54TIvCOCpY"
youtube_url: "https://www.youtube.com/watch?v=T54TIvCOCpY"
publish_date: "2025-01-27"
duration: "4:48"
duration_seconds: 288
view_count: 3984
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_deepseek_blogging
  
  Our blogging system walkthrough: https://www.youtube.com/watch?v=6wJaqpJyswA
  Our more complex blogging system: https://www.youtube.com/watch?v=XoDuyqeX4tU
  Our openrouter video: https://www.youtube.com/watch?v=EsGniZ7Sl8k
  How to connect to wordpress: https://www.youtube.com/watch?v=SQsFd6xIyY0
  How to post images to wordpress: https://www.youtube.com/watch?v=P58OvNdpPYk
  
  0:00 - Introduction
  0:46 - Using OpenRouter and comparing models
  2:17 - Comparison and Verdict - Deepseek vs Claude writing
  4:09 - Perplexity Improved Citations
  
  In this video, we dive into an innovative AI blogging system powered by DeepSeek. With its affordability and impressive capabilities, DeepSeek is making waves in the AI world. We'll demonstrate how to create an automated workflow using Airtable, Perplexity, and DeepSeek V3 to generate fully formatted WordPress posts.
  
  You'll see examples of AI-generated blog posts with structured intros, key takeaways, internal links, and accurate source citations. We'll also compare the performance of DeepSeek V3 to Anthropic Claude 3.5 Sonnet, analyzing writing style, tone, and cost-effectiveness.
  
  You'll also see how OpenRouter enables seamless switching between models like DeepSeek, OpenAI, and others within your automation setup. Plus, learn how recent updates, such as enhanced citation reliability through Perplexity, make the system even more robust.
  
  If you're looking to scale your content creation while keeping costs low, Deepseek could be a game-changer. Though, if you really want the best writing, I still think Claude is a better option if you're willing to pay for it!

yt_tags:
  []



# AI-enriched metadata
content_type: "Framework"
primary_topic: "AI Agents"
difficulty: "Intermediate"
audience:
  - "Engineers"
entities:
  companies:
    - "Anthropic"
    - "Box"
    - "Perplexity"
  people:
    []
  products:
    - "Claude"
    - "Perplexity"
    - "Make"
  models:
    - "Claude 3"
    - "Claude 3.5"
    - "DeepSeek"
    - "Flux"
concepts:
  []
summary:
  - "5 Sonet for this you can add topics to an air table base this automation will pick it up use perplexity to research the topic and then create a fully formatted WordPress pulse with flux 1"
keywords:
  - "ai-agents"
  - "ai-news"
  - "ai-tools"
  - "anthropic"
  - "box"
  - "claude"
  - "frameworks"
  - "make"
  - "meta"
  - "perplexity"
  - "prompting"
  - "workflows"
---

# I Built a Deepseek AI Blogging System (Internal Links + Social Media)

today I'm going to show you an AI bloging system using deep seek everyone's talking about these models at the moment because they're very very cheap and highly capable I'll show you what a deep seek blog post looks like and compare it against a blog post using Claude 3.5 Sonet for this you can add topics to an air table base this automation will pick it up use perplexity to research the topic and then create a fully formatted WordPress pulse with flux 1.1 Ultra images here is an example of the outputed article where you see pretty well structured text a key takeaway section as we scroll down we actually have internal links which have been scraped from the website sitemap and here we have correct links to the sources this is an adapted version of the AI bloging system that I went through on our main channel so check out the link in the description for that that one used anthropic Claude to come up with some really good text I then released a separate video talking about open router which is a fantastic service that you can integrate directly with make.com to very easily swap out whatever models you want using this service you can swap back and forth between so many different language models such as clae open AI metas Lama Gro and many more in this case we have a variable set at the bottom here and then we're set in whatever language model we want to use for the entire automation deep seek have a bunch of different models we can use for this deep seek V3 is like their main competitor to claw 3.5 sonit or open AI gbd 40 it's quite a capable model but look at the difference in price this is 14 Cent per million input tokens or 28 cents per million output tokens if we compare that against Claude $3 per million input tokens or $15 per million output tokens so that's just so much cheaper you can see the difference between deep seek R1 and open AI 01 equivalent here again just way way cheaper in the article I'm about to show you I use deep seek chat which is deep seek V3 deeps V3 worked very nicely for this automation it came out with this article I'm about to show you the model that everyone's talking about at the moment which is deep seek R1 just did not work properly within this setup that I had in this Automation in some cases it just was not really returning the output that we wanted and in said was returning what seemed to be like its Chain of Thought such as don't return the full HTML for the article I'm not sure is it open routers integration with R1 or not but overall deep seek chat V3 was the best model to use for this Automation and also very very cheap I'm quickly going to compare the output of an article using deeps V3 compared to anthropics claw 3.5 Sonet which is the main model we recommend for blogging at the moment okay we have this flux 1.1 Ultra image out of the box I think deep seek V3 writing is very good and very technically correct its tone is quite robotic out of the box kind of similar to gbt 40 deep seeks models at the moment are really taking the AI World by storm due to their reasoning capabilities and perhaps I'm making incorrect correlations here but it really seems to be pointing out the particular facts and data items within this Bolding within the text in general the same applies throughout the rest of this article really overall it's been very concise it's trying to hit all of the data items quickly with this they very much which reads like a report but it is very solid and very cheap as you can see here it's correctly added in these internal links which is scraped from the website sitemap and it's added in these sources at the end of the article which are correct links to websites if we compare this against what Claude 3.5 Sonet was coming out with overall the difference here is tone I know this slightly different research in data items but when you're comparing these models it's mostly just a kind of a Vibe test when you're comparing them especially when it comes to something as subjective as writing style and tone but overall I think the clawed version of this article just kind of reads a bit better and feels more like a blog post but it's very difficult to argue with the cost difference here this is deeps V3 is 28 Cent per million output tokens claw 3.5 son is $15 per million output tokens if you're happy with the overall writing style of this and if you need to scale your condent systems then this could really be a good option and of course you can use this open router template setup to be able to go back and forth to be able to test lots of different AI models all you need to do is go to open router find an AI model copy and paste this out and just change the variable value there and every single model call for the rest of that scenario will then call that model an upgrade that I added to this version of the automation is that now perplexity returns a list of citations in the response so the URLs for the sources within your article are now way more reliable we're now adding these as links to the bottom of the sources in the article and with real no follow in the links if you want to learn how these blogin systems work in more detail then check out the links in the description to other videos on our channels if you want to get way ahead in your AI automation Journey then check out the link in the description to our community we'll get access to all of our automation templates you'll get instant access to all of these courses with more on the way you can get support from us via our live workshops and through our active discussion boards
