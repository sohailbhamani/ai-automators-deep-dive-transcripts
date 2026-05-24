---
title: "Resume Error Handler Explained (With A Real-Life Example)"
video_id: "_63xxWCDMOo"
youtube_url: "https://www.youtube.com/watch?v=_63xxWCDMOo"
publish_date: "2024-12-09"
duration: "4:29"
duration_seconds: 269
view_count: 1047
author: "Deep Dive with The AI Automators"
description: |
  👉 Get all of our make.com templates here: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_resume_error
  
  In this video, I break down how the Resume Error Handler works in Make.com and show you how to use it with a real-life automation example! If you've ever had your automations fail due to errors failing third party modules, this guide will teach you how to handle it like a pro.
  
  You'll learn how to:
  ✅ Use the Resume Error Handler to substitute missing data.
  ✅ Use Filters to Selectively Handle Make.com errors.
  ✅ Keep your Make.com automations running smoothly without manual intervention.
  
  In this example, I demonstrate how to fix a scenario that processes Instagram viral reels, even when the reel has no audio. You'll see exactly how to configure the Resume Error Handler, upload substitute data, and get your automations back on track.
  
  🔗 Resources
  
  Full build of the Instagram viral reels automation: https://www.youtube.com/watch?v=sXcVTS1P45M
  Resume Error Handler documentation: https://www.make.com/en/help/errors/error-handlers/resume-error-handler
  Join our community: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_resume_error
  
  If you found this video helpful, don’t forget to like, comment, and subscribe for more automation tips and tricks! 🚀

yt_tags:
  []



# AI-enriched metadata
content_type: "Deep Dive"
primary_topic: "Career"
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
    - "Flux"
concepts:
  []
summary:
  - "# Resume Error Handler Explained (With A Real-Life Example)

in this video I'm going to show you how the resume error Handler Works in make"
keywords:
  - "ai-agents"
  - "career"
  - "deep-dives"
  - "google"
  - "make"
  - "meta"
  - "workflows"
---

# Resume Error Handler Explained (With A Real-Life Example)

in this video I'm going to show you how the resume error Handler Works in make.com error handlers and make are a little bit confusing so I find the best way to explain it is through an example and I've got a great example here for you so this is an automation that generates Instagram viral reels if you like you can watch the full build of this automation here and I'll provide a link in the card above but in a nutshell what's happening is we have a Google sheet where you list your Instagram competitors and then we have a scenario that scrapes those competitors on appify it Imports all of their reels and posts into this sheet and then you can kind of crunch the numbers figure out which reel is performing well and then you can drop it into this sheet to basically create a variation of that reel for your own profile and that's what I've done here and by typing go here it triggers this automation which fetches The Reel and then it goes through this stream where it extracts the audio from the video and then it transcribes that audio so in other words it's trying to figure out what's in the real it analyzes the image and then it goes to gp40 to create a variation of that Viral reel it creates an image or an AI image on flux one and then it saves it all to Google Sheets where it can then be published to Instagram so all of that works very well one of the members on our community left a message though saying that the scenario encounters an error when a real doesn't have audio and you give an example here where this reel if you press the audio button the video has no sound so what's happening here then let's actually I have this setup here so let's run the scenario wait for new data and now if I type in go and come back to here you'll see that that has come through from Google Sheets it's now going to this Cloud convert service to basically extract the audio from the video but because there isn't any audio in the video this is going to result in an error and there you go so that's what the member in our community had posted so then the question is how do you get around that and you can see the error there the stream is missing because there's no audio in the video so this scenario would just stop because it has encountered an error now and if it wasn't abled would now be disabled which is a bit of a pain so there's a need then to go in and try to kind of handle this situation so yeah I've right clicked it and I've added an error Handler you see that you get different options for error handlers and I've chosen the resume error Handler here and that's what we're talking through so then to come through it so the problem then is this module is encountering an error it needs to be handled so then it's coming up here and then I have no audio in real error is what we're getting and I'm specifically handling this error where there's actually no audio in the real this filter can only pass if this message is in the error message you know that the input file doesn't contain any audio and if you look at the document ation for this the first sentence explains it all so the resume error Handler it replaces the module output with the substitute output when an error happens so if we kind of come back down this track the module directly after this conversion module if we open it up you can see that it's looking for a file from this module or even if you click map you can see it's a file name and it's looking for data so the resume ER Handler replaces or substitutes what you're going to get from this but then the question is what does a substitute with and because this is kind of a complicated scenario that requires a file what I've done is here I've actually uploaded audio of myself to a Cloud Server of me just saying no audio and then in the resume error Handler this is the output of this module so we're substituting what we would have been getting from there with now what I have uploaded to the Cloud Server here so no audio. np3 and then it's just the the data from that so then by pressing okay to this and then if we save this and now let's run this again and we'll type go again now you can see it's comes down this track it's still going to Cloud convert to strip out the audio from the video but it's going to encounter an error because there's no audio so once the error fires it goes down this track it fetches the audio file that I uploaded to the server and then it loads it into the resume module it's able to continue on the stream and then if we jump in here you can see that the file name is no audio. mpp3 and the file data is what was actually fetched in this module so whatever dependencies you have on the outputs of this module you're able to substitute it in the resume module and it then means that you're able to progress through the scenario so it's a really nice kind of module to use in cases like this I'll leave a link to the resume error Handler documentation in the description below and if you're interested in these types of automations then check out the link in the description to our community the AI automator where we have lots of system templates and micro templates to get you started and we also have a make.com master class where you'll learn kind of advanced scenario building tips and tricks like this thanks for watching and I'll see you in the next one
