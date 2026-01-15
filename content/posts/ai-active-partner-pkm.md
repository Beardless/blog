---
title: 'AI as an Active Partner in PKM: How Claude Runs My Daily Journal'
date: 2026-01-15
draft: true
tags: ['ai', 'pkm', 'obsidian', 'productivity']
---

Most daily journaling systems fail within two weeks. Not because the concept is flawed, but because staring at a blank template every evening requires discipline most of us don't have. What if we flipped the model entirely?

## The Empty Template Problem

You know the drill. You set up a beautiful Obsidian vault, create the perfect daily note template with sections for gratitude, wins, reflections, and habits. Day one feels great. Day three, you're rushing through it. By day fourteen, the template mocks you with its emptiness.

The friction isn't in the writing—it's in the starting. A blank page demands you remember what happened, categorize it, and articulate it coherently. That's a lot of cognitive load at the end of a long day.

Traditional solutions involve reducing the template, making it "frictionless." But then you lose the depth that makes journaling valuable in the first place. There's a better way.

## Flipping the Paradigm: AI Asks, You Answer

What if instead of writing to a template, you had a conversation?

Here's my setup: I type `/daily` in Claude, and instead of generating a note immediately, it asks me one simple question:

> "How was your day? What happened, what went well, what was difficult?"

That's it. One open question. I respond naturally, rambling about my day like I'm talking to a friend. No structure required on my end.

Then it follows up about habits—did I do my mobility routine? Close my activity rings? Get enough protein? A quick yes/no for each.

From this conversation, Claude extracts the structure I never had to think about: events, wins, challenges, reflections. It formats everything into my Obsidian template and saves it to my vault.

The key insight: **the AI handles the structure, I provide the content**. The cognitive load of organizing thoughts disappears.

## Anatomy of My /daily Flow

Let me walk you through what actually happens:

**Step 1: The Opening Question**

Claude asks about my day. I respond with whatever comes to mind:

> "Woke up late at 9. Got the kids ready, had a quick standup at 10, worked until 10:30. Went to the barber, picked up my daughter's medical referral. After lunch I called about her holter results and managed to schedule her surgery consultation in Warsaw—that was a win. Worked more, played with my son, moved car seats around because tomorrow I'm driving to Warsaw. Had a meeting at 6 while walking on the treadmill. Evening was dinner, kitchen cleanup, putting my son to bed."

Raw, unstructured, stream of consciousness.

**Step 2: Habit Check**

Claude asks which habits I completed from my predefined list:
- Mobility routine
- Closed activity rings
- Diet on track
- 7h sleep
- Creatine
- Protein target

I give quick answers: "Mobility no, rings yes, diet yes, sleep yes, creatine yes, protein yes."

**Step 3: Context Aggregation**

Here's where it gets interesting. Claude uses its `recent_chats` tool to find all conversations I had with it that day. It summarizes the main topics automatically.

On this particular day, I had researched locations for a friend's bachelor party and analyzed my Apple Health export data. Claude adds this context without me having to remember or mention it.

**Step 4: Preview and Save**

Claude shows me the formatted note:

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
- Apple Health data analysis (weight, sleep, HR, workouts) + updated 
  weekly skill for manual CSV export
```

I confirm, it saves to my vault. Done in under 3 minutes.

## The Technical Setup (For the Curious)

This runs on:
- **Claude** with MCP (Model Context Protocol) integration
- **Obsidian** as the knowledge base
- A custom **skill file** that defines the workflow

The skill file is essentially a prompt that tells Claude:
1. What questions to ask
2. What format to use
3. Where to save the file
4. How to aggregate context from other conversations

The `recent_chats` tool is the secret sauce—it lets Claude see what else we discussed that day, creating automatic backlinks between my journal and my AI-assisted work.

You don't need to code anything. The skill file is plain markdown with instructions. Claude follows them like a checklist.

## Beyond Daily: The Bigger System

Daily notes are just one piece. The same pattern extends to:

**Weekly Reviews**: Claude walks me through a structured review—summarizing daily notes, checking goal progress, identifying patterns in my habits, and helping me set priorities for next week. Data from dailies flows into weeklies automatically.

**Morning Briefings**: A quick rundown of today's calendar, pending tasks, and relevant context from recent work. No more "what was I doing?" moments.

**Health Trend Analysis**: Claude reads my Apple Health exports and spots patterns I'd miss—sleep quality correlations, workout consistency, weight trends toward my goals.

The daily note becomes an input node in a larger knowledge system. Each conversation feeds forward.

## Is This For You?

**This works well if you:**
- Already use Obsidian or similar PKM tools
- Find blank templates demotivating
- Prefer talking/typing naturally over structured input
- Want your AI conversations to persist as knowledge
- Are comfortable with some technical setup

**This might not be for you if:**
- You prefer fully offline systems
- The idea of AI reading your journal feels uncomfortable
- You enjoy the meditative aspect of manual journaling
- You want zero setup—this requires Claude Pro + MCP configuration

**Alternatives without the full setup:**
- Use ChatGPT/Claude in conversation, manually copy the summary
- Voice-to-text apps that transcribe rambling into notes
- Templater + daily prompts in Obsidian (no AI, but reduces friction)

## The Shift That Matters

The real change isn't technical—it's conceptual. We've been treating AI as a generator: give it a prompt, get an output. But AI works better as an **interviewer**: it asks questions, you provide raw material, it handles synthesis.

This inverts the effort. Instead of you doing the cognitive work of structuring thoughts, the AI does it. Your job is just to show up and talk.

Fifteen days ago, I would have skipped journaling because I was tired. Yesterday, I typed `/daily`, answered a few questions, and had a complete record of my day in three minutes.

The best productivity system is the one you actually use. Sometimes that means letting the AI do the boring parts.

---

*Want to build something similar? The skill file and setup instructions are on [GitHub](https://github.com/Beardless/blog). Questions? Find me there.*
