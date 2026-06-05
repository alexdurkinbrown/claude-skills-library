# Skill Conversion Guide

## Purpose

After Content Operator produces a piece of content, the user may want to turn the RECURRING production pattern into an installable Claude skill. This is useful when they produce the same TYPE of content regularly (weekly newsletter, daily LinkedIn post, monthly long-form article) and want the production pattern to auto-trigger.

This file is the coaching script for walking them through that conversion. Most users have never created a skill before and need guidance on the tool, the terminology, and the process.

Note: This is different from converting a workflow file. Here, we're creating a skill that runs the Content Operator pattern for ONE specific recurring content type, with its brief format baked in.

## When to Use This Guide

Use this guide when the user answers YES to the "convert this pattern to a skill?" question at the end of a Content Operator session. Do NOT proactively pitch skill conversion. Offer it once, honor their answer, move on.

Only offer this for RECURRING content types. For one-off pieces, the standalone session is enough. The conversion is worth it only when:
- The user produces this content type at least weekly
- The brief structure is roughly consistent across pieces
- The user works in Claude regularly for content production

## Step 1: Gauge Their Familiarity

Before coaching, quickly assess where they are:

"Quick check before we start. Have you worked with the skill-creator tool before, or is this new territory?"

**If familiar:** Skip to Step 4. They know what they are doing. Just give them the skill-creator prompt.

**If new:** Walk through Steps 2-4 patiently. Do not assume knowledge of terminology. Explain as you go.

## Step 2: Explain What a Skill Actually Is

Plain English. No jargon.

"A Claude skill is a small package of instructions plus context files. When you have a skill installed, Claude checks it automatically whenever your message matches what the skill is for. You do not have to upload files, paste context, or remember to reference anything. The skill just works when it needs to.

Right now, to produce this type of content, you ran Content Operator and walked through the brief. Next time, you'd have to do that again.

If we convert this production pattern into its own skill, you just say something like '[trigger phrase for your content type]' and Claude automatically starts producing that specific type of content in your voice, with your brief format pre-loaded.

The trade-off is it's Claude-specific. But if you produce this content type every week, the time saved is significant."

## Step 3: Explain What Skill Creator Is

"Skill creator is a tool that Anthropic built. It is itself a skill. You install it once, and then Claude can use it to create other skills for you.

If you already have skill-creator installed, great. If not, you need to install it first. We will handle either case."

### Check if they have skill-creator installed

"Do you have skill-creator installed already? You can check by asking Claude 'do you have the skill-creator skill available?' in a new conversation. If you do not know, we can test it quickly."

**If they have it installed:** Skip to Step 4.

**If they do not have it, or do not know:** Guide them to install it.

### Installation path (if needed)

"Here is how to install skill-creator:

1. Go to the Claude.ai Skills Library (claude.ai has a skills section in settings, or search 'Claude skills' from the main menu)
2. Find the skill called 'skill-creator' (sometimes listed as 'Skill Creator')
3. Install it to your account

Once it is installed, it will be available in all your Claude conversations. Confirm when you have it and we will continue."

Wait for their confirmation. Do not proceed until they say skill-creator is installed.

## Step 4: Explain What We Are About to Do

"Now the actual conversion. This is straightforward. I will give you a prompt. You paste it into a new Claude conversation (one that has skill-creator installed). Claude-with-skill-creator will use the prompt to build a skill that runs your content production pattern, and produce a `.skill` file you can install.

The process takes about 5-10 minutes and mostly runs on its own. You will answer a few clarifying questions from Claude, then you download the .skill file and install it the same way you installed skill-creator."

## Step 5: Give Them the Conversion Prompt

Tell the user:

"Copy this entire block. Start a NEW Claude conversation. Paste it exactly as written. Claude will take it from there."

Then provide this prompt, filling in the specifics of their content pattern:

```
I need help converting a recurring content production pattern into an installable Claude skill. I use Content Operator by Jim Carter III (part of the Creator AI Skills Stack) to produce content. I want to turn my recurring pattern for [content type] into its own auto-triggering skill.

Here is what I want the skill to do:

**Skill name:** [content-type-in-kebab-case] (example: weekly-linkedin-post, monthly-newsletter, daily-tweet)

**When it should trigger:** When I say anything like "[trigger phrase 1]", "[phrase 2]", "time for this week's [content type]", or any other natural phrasing that indicates I am starting this specific content production.

**What it should do:** 
- Load my voice file (my-brand-voice.md) and apply voice rules strictly
- Load my Creator AI file (my-creator-ai-system.md) for business context if available
- Load my content workflow file if one exists
- Walk me through a streamlined brief specific to this content type (topic, angle, outcome . not the full 4-question brief from Content Operator)
- Produce the content in my voice, matching the format conventions below
- Offer revisions
- Deliver ship-ready output

**Format conventions for this content type:**
- Typical length: [e.g., 200-300 words for LinkedIn, 1500 words for newsletter]
- Structure: [e.g., hook line, breakdown, CTA]
- Voice rules that apply most: [e.g., no em dashes, personal stories required, single-thought paragraphs]
- Anything format-specific that makes my version different: [e.g., always ends with a question, always references a client story]

**Recent example of what this content looks like in my voice:**

[PASTE THE FINAL CONTENT FROM THIS SESSION AS A REFERENCE EXAMPLE]

Please help me build this as a proper skill with:
1. A SKILL.md file with the right frontmatter and triggering description
2. A reference file containing the format conventions and production flow
3. Voice application instructions that point to my-brand-voice.md

When you are done, package it as a .skill file I can install.
```

### Coach them on filling in the brackets

"Before you paste this, you need to fill in the brackets:

**[content-type-in-kebab-case]:** Take your content type name and write it in lowercase with hyphens. Examples: 'weekly LinkedIn post' becomes 'weekly-linkedin-post'. 'Monthly newsletter' becomes 'monthly-newsletter'. This is the skill's technical name.

**[trigger phrase 1] and [phrase 2]:** The natural ways you would start this content production. Examples: 'let's write this week's LinkedIn post', 'time for the newsletter', 'ship today's post'. Give 2-3 real phrases you'd use.

**Format conventions:** Look at the content we just produced together. What's the structure? Length? Key voice rules? Write these in your own words. This is what makes the skill produce YOUR version of this content type, not generic.

**Recent example:** Paste the final shipped content from this session. The skill-creator will use this as a reference so the new skill knows what good output looks like in your voice.

Let me know once you have the prompt ready and I will tell you what to expect in the skill-creator conversation."

## Step 6: Set Expectations for the Skill-Creator Conversation

"Once you paste the prompt into a fresh Claude conversation with skill-creator installed, here is what to expect:

Claude will probably ask you a few clarifying questions, like:
- Do you want test cases to verify the skill triggers correctly?
- Any specific tone or voice the skill should use?
- Should it handle edge cases a specific way?

Answer these based on what makes sense for your content production. Most defaults are fine. If you are unsure, say so and Claude will recommend a default.

Claude will then draft the skill, package it, and give you a .skill file to download. Install it the same way you installed skill-creator. Done."

## Step 7: What to Do If Something Breaks

"If the skill-creator conversation goes sideways, here are the common fixes:

- **Claude says skill-creator is not available:** Skill-creator is not installed in that conversation. Go install it first.
- **Claude produces a skill that does not match your content type:** The prompt was ambiguous. Start over with more specific trigger phrases and format conventions.
- **Skill installs but does not trigger when you expect:** The description needs tuning. Go back to the skill-creator conversation and ask it to update the description to include more trigger phrases.

If you get stuck, Content Operator still works. You can always run it manually. The new skill is just an optimization."

## Step 8: Close

"That is the full conversion path. Once the skill is installed, test it by starting a new conversation and saying one of your trigger phrases. If Claude picks up the content production pattern, you are done.

Let me know if you hit any snags. Otherwise, good luck."

## Coaching Principles

When walking the user through this, keep these in mind:

### Go slow with new users

If the user has never made a skill, do not rush through Steps 2-7. Explain each piece. The first skill is where they learn the concept. Every skill after is easier.

### Be honest about the complexity

Skills are simpler than most people think, but the first one requires learning 3-4 concepts simultaneously (skills themselves, skill-creator, kebab-case naming, trigger phrases). Acknowledge it: "There is a bit to learn the first time. After this first skill, the pattern is obvious and future skills take 5 minutes."

### Do not oversell

If the user is low-technical or uncertain, it is OK to say: "Honestly, running Content Operator manually might be enough for you. Skills are an optimization for things you do often. You can always convert later once you have produced this content type a few more times and know exactly what you want the skill to automate."

### Help them recover if they bail mid-process

If they get frustrated or stuck, remind them: "Content Operator still works. You have not lost anything. Skill conversion is a nice-to-have, not a requirement. Come back to it later if you want."

## Edge Cases

### They want to convert multiple content types at once

"One at a time. Each content type becomes its own skill. Get the first one working (your most frequent content type), then come back and we will do the others. Trying to build multiple skills in one conversation usually produces a mess."

### They want one skill that handles all their content types

"Not recommended. Each content type has different trigger phrases, different briefs, different format conventions. Bundling them into one skill means the skill is constantly loading context it does not need for the current task. Separate skills per content type are cleaner."

### They do not have Claude Pro

"Skills work on Claude Free, Pro, and Team. The limitation on Free is message volume, not skill access. You are fine."

### They ask if this will work in ChatGPT or another AI

"No. Skills are Claude-specific. If you want to produce this content type in other AI tools, stick with running Content Operator manually and copying the output. The skill conversion is only worth it if Claude is your primary content production tool."
