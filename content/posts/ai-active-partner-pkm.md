---
title: "AI as an Active Partner in PKM: How Claude Runs My Daily Journal"
date: 2026-01-15
draft: false
tags: ["ai", "pkm", "obsidian", "productivity"]
---

Most daily journaling systems fail within two weeks. Not because the concept is flawed, but because staring at a blank template every evening requires discipline most of us don't have. I tried probably five different setups before landing on something that actually stuck.

## The Empty Template Problem

You know the drill. You set up a beautiful Obsidian vault, create the perfect daily note template with sections for gratitude, wins, reflections, and habits. Day one feels great. Day three, you're rushing through it. By day fourteen, the template mocks you with its emptiness.

The friction isn't in the writing—it's in the starting. A blank page demands you remember what happened, categorize it, and articulate it coherently. That's a lot of cognitive load at the end of a long day when you just want to crash.

Traditional solutions involve reducing the template, making it "frictionless." But then you lose the depth that makes journaling valuable in the first place.

## What If AI Asked the Questions Instead?

My current setup flips things around. I type `/daily` in Claude, and instead of generating a note, it asks me one question:

> "How was your day? What happened, what went well, what was difficult?"

I respond like I'm texting a friend. No structure, no categories, just whatever comes out:

> "Woke up late at 9. Got the kids ready, had a quick standup at 10, worked until 10:30. Went to the barber, picked up my daughter's medical referral. After lunch I called about her holter results and managed to schedule her surgery consultation in Warsaw—that was a win. Worked more, played with my son, moved car seats around because tomorrow I'm driving to Warsaw. Had a meeting at 6 while walking on the treadmill. Evening was dinner, kitchen cleanup, putting my son to bed."

Then Claude asks about habits—mobility routine? activity rings? protein? I just fire off quick answers.

From this mess, Claude extracts structure: events, wins, challenges. It formats everything into my Obsidian template and saves it. The AI handles the organizing, I just talk.

## The Part That Surprised Me

Claude can pull up all the conversations I had with it that day using `recent_chats`. So if I spent the morning researching bachelor party locations and the afternoon analyzing my Apple Health data, that context shows up in my daily note automatically.

I don't have to remember what I worked on. The note documents both my life and my AI-assisted work in one place.

## What the Output Looks Like

After our conversation, Claude shows me this:

```markdown
# 📅 2026-01-15 (Thursday)

## What happened today?

Late start (9:00). Standup at 10, work until 10:30, then barber in
Biała. Picked up Jaśmina's referral. After lunch—called about her
holter results and scheduled surgery consultation in Warsaw ✅

Work until 16:30. Played with Leon, dinner, moved car seats to Mazda
(Volvo goes to Warsaw tomorrow). Meeting at 18 + treadmill. Evening:
Leon, dinner, kitchen cleanup. Bedtime routine at 21.

## Habits

- habit:: Mobility ❌
- habit:: Closed rings ✅
- habit:: Diet ✅
- habit:: Sleep 7h ✅
- habit:: Creatine ✅
- habit:: Protein ✅

## Notes

**Work with Claude:**

- Bachelor party research—attractions near Szydłówko and Osieczek,
  house rentals ~30 min from Warsaw
- Apple Health data analysis (weight, sleep, HR, workouts)
```

I confirm, it saves. Three minutes, done.

## How It Actually Works

The setup is Claude with MCP (Model Context Protocol) connected to my filesystem, plus a "skill file"—basically a markdown document with instructions for Claude: what questions to ask, what format to use, where to save.

No coding required. The skill file is just text. Claude reads it and follows the steps like a checklist.

If you want to dig into the technical details, I'll share the skill file in a follow-up post.

## This Is Part of a Bigger System

Daily notes feed into other workflows I've built:

Weekly reviews aggregate the dailies, check habit streaks, and help me plan next week. Morning briefings pull from my calendar and recent context so I don't start the day confused. Health analysis spots patterns in my Apple Health exports—sleep correlations, workout consistency, weight trends.

Each piece connects. The daily note isn't just a record, it's an input for everything else.

## Would This Work for You?

Probably yes if you already use Obsidian, hate blank templates, and don't mind some initial setup.

Probably no if you want everything offline, feel weird about AI reading your journal, or enjoy the meditative ritual of writing by hand.

The setup requires Claude Pro and MCP configuration. It's not plug-and-play. But once it's running, the friction basically disappears.

## The Honest Takeaway

I've tried a lot of productivity systems. Most didn't survive contact with real life—two kids, demanding job, limited energy. This one works because it asks almost nothing of me. I show up, ramble for two minutes, and get a structured record of my day.

Is it perfect? No. Sometimes Claude's summaries miss nuance. Sometimes I want to write more but don't because the conversation is already done. But I have 15 consecutive daily notes now, which is about 14 more than my previous attempts.

The best system is the one you actually use. For me, that meant outsourcing the boring parts to AI.

---

_Skill file and setup instructions coming in a future post. In the meantime, questions → [GitHub](https://github.com/Beardless)._
