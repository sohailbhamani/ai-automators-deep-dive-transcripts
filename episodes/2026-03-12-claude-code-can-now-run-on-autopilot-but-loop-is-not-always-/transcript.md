---
title: "Claude Code Can Now Run On AUTOPILOT. But /loop Is Not Always The Best Way."
video_id: "G7u9_oocPmM"
youtube_url: "https://www.youtube.com/watch?v=G7u9_oocPmM"
publish_date: "2026-03-12"
duration: "unknown"
duration_seconds: 0
view_count: 0
author: "Deep Dive with The AI Automators"
description: |
  👉 Get ALL of our courses, systems and resources: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=c2_claude_loops
  
  Agentic RAG Series: https://www.youtube.com/watch?v=xgPWCuqLoek
  
  In this video, I break down the four main ways you can run recurring tasks inside Claude’s ecosystem and explain which one actually makes sense depending on what you’re trying to automate. We look at the new /loop feature in Claude Code, Desktop scheduled tasks, Claude Cowork scheduled tasks, and GitHub Actions, so you can quickly understand the trade-offs between speed, persistence, and technical complexity.
  
  You’ll see why Claude Code loops are the easiest place to start if you want something running in seconds with almost no setup. I explain how /loop lets you describe a recurring task in plain English, how one-time reminders work, and why it’s such a useful option for testing automations like inbox summaries, reminders, deployment checks, recurring research, and status updates. I also cover the important limitations, including session scope, the three-day expiry, the need to keep your terminal open, and the fact that missed runs do not catch up.
  
  From there, I compare loops with scheduled tasks in the Claude Code Desktop app, which are much better suited for daily or weekly automations that you want to keep running over time. I walk through how these tasks differ from loops, why they persist across restarts, how catch-up behaviour works after sleep or downtime, and the kinds of workflows they’re ideal for, such as morning briefings, weekly competitor research, file organisation, recurring finance summaries, and social content generation.
  
  I also touch on Claude Cowork as an alternative for less technical users, along with some of the current quirks worth being aware of. Then I explain where GitHub Actions fits into the picture, especially for developer-focused workflows that need to run in the cloud without relying on your own machine being awake. If you’re using Claude to support pull requests, repository updates, or shared engineering processes, this is where GitHub Actions becomes the better option.
  
  By the end of the video, you’ll know when to use /loop for quick temporary automation, when to promote a task into a persistent Desktop scheduled task, and when GitHub Actions is the better long-term choice for cloud-based development workflows.

yt_tags:
  []



# AI-enriched metadata
content_type: "News Roundup"
primary_topic: "AI Tools"
difficulty: "Intermediate"
audience:
  - "Engineers"
  - "Executives"
  - "Product Managers"
entities:
  companies:
    - "Slack"
    - "GitHub"
  people:
    []
  products:
    - "Claude"
    - "Claude Code"
    - "Opus"
  models:
    []
concepts:
  []
summary:
  - "# Unknown

A new feature just dropped within clawed code that allows you to run tasks on autopilot"
keywords:
  - "ai-news"
  - "ai-tools"
  - "anthropic"
  - "career"
  - "claude"
  - "claude-code"
  - "coding"
  - "frameworks"
  - "github"
  - "leadership"
  - "opus"
  - "product-management"
  - "prompting"
  - "slack"
  - "workflows"
---

# Unknown

A new feature just dropped within clawed code that allows you to run tasks on autopilot. All you do is type in for/loop, add in an interval like 1 minute or 1 day and then just tell it what to do such as say hi. And now it's going to run that every single minute. It's used chron create to schedule this and it's going to run every single minute. It will autoexpire after 3 days. And you can see here it's already run that the first time. It's a very straightforward process and there are a lot of different use cases you could use this for such as for checking your inbox and summarizing to doing research to setting yourself reminders and lots more. Claude Code can also pick up these requests without you using this command just using natural language. And you can also set one-time reminders such as remind me at 3 p.m. to push the release branch. Then it will just come back and run that prompt at that particular time. So, while this is quite a useful feature, there are some serious limitations that you need to know about, which I'm going to talk about in a minute. And it's also worth noting that there are now four different ways that you can run tasks on autopilot within clause ecosystem. So, I'll be explaining all of those and comparing those against this new loop feature. In my really trivial example here, it's run this eight times after 8 minutes. And this will just keep running every minute up to 3 days as long as this session stays open and while the computer stays on. If I close this session, then that schedule is then finished. And instead of just sending me a simple message like this, it can do real work in the process. It could scrape websites. It could interact with your browser. It could interact with your file system, use MCPS, and lots more. But there are some serious limitations. As I mentioned, it's session scoped, so once you close the terminal, the loops are gone. It also has a 3-day auto expiry. So, if you want to persist tasks that run every day or every week, for example, this really is not the best solution. Your computer must stay on and awake in the process and also if you miss a schedule then it's not going to catch up. As a mental model you can think of this loop command as quick, temporary and disposable. Think of it like a sticky note. Whereas if you want to get clawed code to run tasks over a longer term then it's better idea to use schedule tasks which I'll show you now. If you have the clawed desktop app, you can go to the code tab and then go to schedules to go to your schedule tasks window. From there, just click on new task and then you can add in the name of the task, the description, and then whatever prompt you need for that particular task. You can choose what model to use for it. So, Opus 4.6 for the more ambitious tasks and highQ 4.5 for quick tasks that do not use as much of your usage. You can select a folder for it to work from. And you can also define the frequency of hourly, daily, weekdays, or weekly. Or you can set it as a manual task that you can trigger directly from this schedule tasks window. And you can set the time you want to schedule it. When it's time to run that task, it creates a new session within this app. And you can open it up here. This is a simple task I've set up to get it to curate AI news on a daily basis and then send this to a Slack channel. It's using a new session for this. It has fresh context within connectors. Here you can see I've already connected Slack to my app. And you can see it's sent this message to the Slack channel. So there are some really clear differences between using the forward/loop command within cloud code and using the schedule tasks feature within the desktop app. When using forward/loop, it doesn't survive restarts of your computer. You can't catch up and miss tasks. The loops auto expire after 3 days and also everything is done within the same session. Whereas when using scheduled tasks by the desktop app, they survive restart. So you can restart your computer the next time the scheduled job is due to be hit. it will start a new session within cloud code in the claw desktop app. If you miss a run of the task, it will catch up the next time you have the app. And they don't have this three-day auto expire feature. And also, they run in an isolated session. So, every time a new schedule is hit, it's going to open up a new session like you see here. So, often isolated context will work quite well, especially for separate executions of tasks. And also, you can get clawed code to reference information between sessions by storing data within markdown files, for example. So isolated context is often a pretty good idea and also you limit the amount of tokens you're using. Shared context can actually still work quite well when you're using short-term loop commands because you know you may want to reference things that happened earlier on in the process. So it's not always a bad thing, but it's just something to keep in mind. So for scheduled tasks within clawed code, there are a huge amount of different use cases you can use over a longer time period such as competitor monitoring and research, organizing your files on your file system, creating reports, and also drafting social media and content for example. And as mentioned previously, if you're using cloud code scheduled tasks, if your computer is off, then it will catch up for missed tasks when the app is back open again. Also to mention, claude co-work also has very similar scheduled task features. Claude co-work is effectively cla dressed up for a non-technical audience. There are some limitations and it runs in a sandbox and it's also in a kind of an airy version of the app, but you can also schedule tasks directly from the co-work app. The easiest way is to just type in for/chedu and then just ask it what to do. Also, if you go to the schedule menu up here and you can set up these schedule tasks in almost exactly the same way as you can within the code tab within this app. If you already understand how to use clawed code, then it's best to run scheduled tasks through this. For anyone who's less technical, you can just run scheduled tasks directly within cla. Generally, I found these to work very well. Some people do have issues running the actual app itself. So, that's also something to keep in mind. It's still quite an early version of this particular app. And finally, we have GitHub actions, which are quite different to everything I've talked about so far and also a lot more advanced. These are used for development workflows. GitHub actions can run Claude directly on GitHub's infrastructure. And these can be triggered by events like somebody opening a pull request or mentioning Claude within an issue. And also, you can run tasks on a schedule. So, for example, you can generate a summary of yesterday's commits and open issues and then run that every single day. If you want to use claude working on your GitHub repo and especially if you have multiple team members all contributing to the same project, you can have this to create PRs, automate code implementation, do things like security audits, run reports, and things like that. I'm not going to be doing a deep dive into GitHub actions within this video. It's a much deeper topic and also it's made really for software development workflows. And if you're here for general automation and productivity, either using the loop command or using schedule tasks either via cloud code or co-work are probably the best bets for you. If you like this video, you're going to love our full series on building agentic rag systems linked in the description below.
