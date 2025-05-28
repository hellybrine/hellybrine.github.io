---
layout:     post
title:      "Building Honeygotchi"
subtitle:   "When Honeypots Meet AI"
date:       2025-05-28 11:45:00
author:     "Mac"
header-img: "img/in-post/honeypot.jpg"
catalog: true
tags:
    - Machine Learning
    - Honeypot
    - Cybersecurity
---

> "A personal journey through reinforcement learning, sleepless nights, and teaching machines to trash-talk hackers"

## The "Aha!" Moment That Started It All

Picture this: It's 2 AM, I'm drowning in cybersecurity research papers for my mini-project, and I stumble across this mind-blowing realization. Why are all honeypots so... dumb? 

Here we are in 2025, with AI revolutionizing everything from coffee makers to space exploration, yet honeypots are still using the same boring, predictable responses they've had since the early 2000s. It was like watching someone try to catch fish with a fishing rod made of spaghetti. Technically possible, but painfully inefficient.

That's when Honeygotchi was born. Not just another SSH honeypot, but one that could **learn, adapt, and yes, even insult attackers back**. More on that delightful feature later.

## Chapter 1: The Honeymoon Phase (Spoiler: It Didn't Last)

The initial excitement was intoxicating. "I'll build an adaptive honeypot using reinforcement learning!" I declared confidently to my supervisor, probably sounding like every over-ambitious computer science student ever.

The plan was elegant in its simplicity:
- **SSH honeypot** that attracts attackers
- **Reinforcement learning agent** that learns optimal responses
- **Fake file system** that's convincing enough to fool seasoned hackers
- **Real-time monitoring** because what's the point without cool dashboards?

What could go wrong? 

*Famous last words.*

Little did I know, I was about to enter what I now fondly call "Dependency Hell" - a special place where nothing works and everything is broken for mysterious reasons.

## Chapter 2: Docker, Dependencies, and Digital Despair

### The Great Dependency Hell of March 2025

If you've never experienced true frustration, try getting AsyncSSH, Prometheus, Grafana, and Loki to play nicely together while your reinforcement learning agent throws random errors that Google has never heard of.

I spent **three entire days** debugging what turned out to be a single missing environment variable. THREE DAYS. I questioned my life choices, my career path, and whether I should have just become a barista instead.

But then came the breakthrough! The moment when all components finally connected and I saw my first attacker session in the Grafana dashboard was like watching your child take their first steps. Except this child was designed to deceive cybercriminals, which makes me question my metaphor choices.

### The Permission Nightmare

Just when I thought I was making progress, Docker permissions became my arch-nemesis. The classic `EACCES: permission denied` error haunted my dreams. I learned more about UIDs, GIDs, and file ownership than any sane person should know.

**Pro tip for future me**: Always, ALWAYS run `sudo chown -R 1000:1000` on your data directories before crying into your coffee for two hours.

Once I conquered the technical hurdles, it was time for the really fun part: teaching my AI to have some personality.

## Chapter 3: Teaching Machines to Be Sassy

Here's where things got interesting. My RL agent needed five strategic responses:
- **ALLOW**: "Sure, run that command, let's see what you're up to"
- **BLOCK**: "Nope, not today, Satan"  
- **DELAY**: "Let me think about this... for 3 agonizing seconds"
- **FAKE**: "Here's some totally real and definitely not fabricated data"
- **INSULT**: And my personal favorite...

### The INSULT Action: A Love Story

The INSULT action was born during a particularly stressful debugging session. I thought, "You know what? If I have to deal with automated bots hammering my system, the least I can do is program it to fight back with sass."

Some of my favorite responses the system learned to generate:
- *"Your attack patterns are so predictable, 10.19.0.13. Try something original."*
- *"Command #15 and still failing? Time to give up, 10.19.0.13."*

Watching my honeypot develop its own personality through reinforcement learning was unexpectedly delightful. It started conservative, but as it learned what kept attackers engaged longer, it got bolder. My honeypot was developing **attitude**, and I was absolutely here for it.

The real magic, though, was in how it learned these behaviors. That's where the epsilon-greedy algorithm came into play.

## Chapter 4: The ε-Greedy Breakthrough

Implementing the epsilon-greedy algorithm was like teaching a toddler to make decisions. 

Start with high exploration (ε = 0.3): "I have no idea what I'm doing, so let me try everything!"

Gradually reduce to exploitation (ε = 0.1): "I've learned some things, let me use that knowledge, but still surprise myself occasionally."

The beautiful part was watching the action distribution graphs in Grafana. Over time, you could literally see the system learning:
- Week 1: Random chaos across all actions
- Week 3: Clear preferences emerging 
- Week 6: Sophisticated response patterns that actually kept attackers engaged 300% longer than static responses

**That 300% improvement wasn't just a number. It was validation that this crazy idea actually worked.**

Of course, having smart responses meant nothing if the environment itself wasn't convincing. Time to build a digital movie set.

## Chapter 5: The Fake File System Chronicles

Creating a convincing Linux environment is harder than it sounds. It's not enough to just create `/home/user` and call it a day. Attackers are smart. They probe for inconsistencies like digital detectives.

### The Devil's in the Details

I spent weeks crafting the perfect fake environment:
- **SSH keys that looked legitimate but were totally fabricated**
- **A `.bash_history` that told the story of a slightly paranoid sysadmin**
- **System files with just the right amount of wear and tear**
- **Honeytokens sprinkled throughout to track information theft**

My favorite touch? A fake cryptocurrency wallet recovery phrase hidden in a "secret" directory. The number of attackers who spent hours trying to crack that worthless seed phrase brought me way too much joy.

With my digital theater complete, I needed a way to watch the show unfold in real-time.

## Chapter 6: Late Nights and Monitoring Magic

The monitoring stack (Prometheus + Grafana + Loki) became my mission control. There's something deeply satisfying about watching real-time attack patterns flowing across colorful dashboards at 3 AM.

### The Eureka Moment

The real breakthrough came when I saw my first sophisticated human attacker spend **over 2 hours** in the honeypot, completely fooled by the adaptive responses. They even tried to download "malware" from my fake file system and got increasingly frustrated when their tools wouldn't work properly.

Watching someone getting outsmarted by my AI-powered deception system was better than any Netflix series.

### The Unexpected Joy:
Building Honeygotchi taught me that cybersecurity doesn't have to be all doom and gloom. There's genuine fun in outwitting attackers, creativity in designing deception, and satisfaction in watching AI learn and adapt in real-time.

## The Road Ahead

Honeygotchi is open-source now, living on [GitHub](https://github.com/hellybrine/honeygotchi) where other developers can build upon it. There's talk of adding large language models for even more sophisticated responses, multi-protocol support, and collaborative learning between distributed honeypots.

But honestly? The best part isn't the future plans. It's knowing that somewhere out there, automated attack tools are getting confused by an AI that learned to be strategically unhelpful, and human attackers are wasting hours in beautifully crafted digital rabbit holes.

## Final Thoughts: From Frustration to Success

Six months ago, I was just another student with an overly ambitious idea and a caffeinated determination to make it work. Today, I have a functioning adaptive honeypot that's smarter than most static security tools and sassier than a Twitter troll.

**To anyone building their own impossible project**: Yes, you'll question your sanity. Yes, you'll spend entire nights debugging seemingly simple problems. Yes, you'll consider giving up approximately 47 times.

But that moment when your code finally works, when your AI starts learning, when your idea transforms from concept to reality? That moment makes everything worth it.

Plus, you get to tell people you built an AI that learned to insult hackers. And honestly, how cool is that?