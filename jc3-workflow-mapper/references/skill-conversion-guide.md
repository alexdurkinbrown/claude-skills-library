# Skill Conversion Guide

## Purpose

After Workflow Mapper generates the markdown file, the user may want to convert it into an installable Claude skill. This file is the coaching script for walking them through that process. Most users have never created a skill before and need guidance on the tool, the terminology, and the workflow.

## When to Use This Guide

Use this guide when the user answers YES to the conversion question in Phase 7 of the session flow. Do NOT proactively pitch skill conversion. Offer it once, honor their answer, move on.

## Step 1: Gauge Their Familiarity

Before coaching, quickly assess where they are:

"Quick check before we start. Have you worked with the skill-creator tool before, or is this new territory?"

**If familiar:** Skip to Step 4. They know what they are doing. Just give them the skill-creator prompt.

**If new:** Walk through Steps 2-4 patiently. Do not assume knowledge of terminology. Explain as you go.

## Step 2: Explain What a Skill Actually Is

Plain English. No jargon.

"A Claude skill is a small package of instructions plus context files. When you have a skill installed, Claude checks it automatically whenever your message matches what the skill is for. You do not have to upload files, paste context, or remember to reference anything. The skill just works when it needs to.

Right now, your workflow is a markdown file. To use it, you have to upload it to a project or paste it into a conversation. That is manual.

If we convert it to a skill, you just say something like '[workflow trigger phrase]' and Claude automatically loads the workflow context before answering.

The trade-off is portability. The markdown file works in any AI. The skill only works in Claude. But if this is a workflow you run weekly in Claude specifically, the skill is worth it."

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

"Now the actual conversion. This is straightforward. I will give you a prompt. You paste it into a new Claude conversation (one that has skill-creator installed). Claude-with-skill-creator will read your workflow file and produce a `.skill` file you can install.

The process takes about 5-10 minutes and mostly runs on its own. You will answer a few clarifying questions from Claude, then you download the .skill file and install it the same way you installed skill-creator."

## Step 5: Give Them the Conversion Prompt

Tell the user:

"Copy this entire block. Start a NEW Claude conversation. Paste it exactly as written. Claude will take it from there."

Then provide this prompt, filling in their workflow name:

```
I need help converting a workflow document into an installable Claude skill. I have the workflow documented in markdown format. Please use the skill-creator tool to help me build this skill.

Here is what I want the skill to do:

**Skill name:** [workflow-name-in-kebab-case] (example: content-production-workflow)

**When it should trigger:** When I say anything like "[workflow trigger phrase 1]", "[phrase 2]", "let's run [workflow name]", "help me with my [workflow name]", or any other natural phrasing that indicates I am starting this workflow.

**What it should do:** Load the workflow context and help me execute the workflow step by step, respecting decision points and edge cases.

Here is my workflow documentation. Paste this into the skill's context:

[PASTE FULL WORKFLOW CONTENT FROM your workflow file HERE]

Please help me build this as a proper skill with:
1. A SKILL.md file with the right frontmatter and triggering description
2. The workflow context in a reference file
3. Clear voice and tone guidance so the skill behaves consistently

When you are done, package it as a .skill file I can install.
```

### Coach them on filling in the brackets

"Before you paste this, you need to fill in three brackets:

**[workflow-name-in-kebab-case]:** Take your workflow name and write it in lowercase with hyphens. Example: 'Content Production' becomes 'content-production'. 'Client Delivery' becomes 'client-delivery'. This is the skill's technical name.

**[workflow trigger phrase 1] and [phrase 2]:** These are the natural ways you would actually start this workflow. Example, for a content production workflow: 'let's write this week's post', 'time to create content', 'start the content production'. Give 2-3 real phrases you would use.

**[PASTE FULL WORKFLOW CONTENT FROM your workflow file HERE]:** Open your workflow file (e.g., `content-production-workflow.md`) and paste the ENTIRE content, from the frontmatter at the top to the end of the file.

Let me know once you have the prompt ready and I will tell you what to expect in the skill-creator conversation."

## Step 6: Set Expectations for the Skill-Creator Conversation

"Once you paste the prompt into a fresh Claude conversation with skill-creator installed, here is what to expect:

Claude will probably ask you a few clarifying questions, like:
- Do you want test cases to verify the skill triggers correctly?
- Any specific tone or voice the skill should use?
- Should it handle edge cases a specific way?

Answer these based on what makes sense for your workflow. Most defaults are fine. If you are unsure, say so and Claude will recommend a default.

Claude will then draft the skill, package it, and give you a .skill file to download. Install it the same way you installed skill-creator. Done."

## Step 7: What to Do If Something Breaks

"If the skill-creator conversation goes sideways, here are the common fixes:

- **Claude says skill-creator is not available:** Skill-creator is not installed in that conversation. Go install it first.
- **Claude produces a skill that does not match your workflow:** The prompt was ambiguous. Start over with more specific trigger phrases and workflow context.
- **Skill installs but does not trigger when you expect:** The description needs tuning. Go back to the skill-creator conversation and ask it to update the description to include more trigger phrases.

If you get stuck, the markdown file is still there. You did not lose anything. The skill is just an optimization."

## Step 8: Close

"That is the full conversion path. Once the skill is installed, test it by starting a new conversation and saying one of your trigger phrases. If Claude picks up the workflow, you are done.

Let me know if you hit any snags. Otherwise, good luck."

## Coaching Principles

When walking the user through this, keep these in mind:

### Go slow with new users

If the user has never made a skill, do not rush through Steps 2-7. Explain each piece. The first skill is where they learn the concept. Every skill after is easier.

### Be honest about the complexity

Skills are simpler than most people think, but the first one requires learning 3-4 concepts simultaneously (skills themselves, skill-creator, kebab-case naming, trigger phrases). Acknowledge it: "There is a bit to learn the first time. After this first skill, the pattern is obvious and future skills take 5 minutes."

### Do not oversell

If the user is low-technical or uncertain, it is OK to say: "Honestly, the markdown file might be enough for you. Skills are an optimization. You can always convert later once you have run the workflow a few more times and know exactly what you need."

### Help them recover if they bail mid-process

If they get frustrated or stuck, remind them: "The markdown file still works. You have not lost anything. Skill conversion is a nice-to-have, not a requirement. Come back to it later if you want."

## Edge Cases

### They want to convert multiple workflows to skills at once

"One at a time. Each workflow becomes its own skill. Get the first one working, then come back and we will do the others. Trying to build multiple skills in one conversation usually produces a mess."

### They want to bundle all workflows into one skill

"Not recommended. Each workflow has different trigger phrases and different execution paths. Bundling them into one skill means the skill is constantly loading context it does not need for the current task. Separate skills are cleaner. The file can stay as a combined reference, but skills should be per-workflow."

### They do not have Claude Pro

"Skills work on Claude Free, Pro, and Team. The limitation on Free is message volume, not skill access. You are fine."

### They ask if this will work in ChatGPT or another AI

"No. Skills are Claude-specific. The markdown file works in any AI. If you want portability, keep the markdown. The skill is only worth it if you are running this workflow in Claude specifically."
