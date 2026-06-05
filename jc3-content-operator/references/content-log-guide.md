# Content Log Guide

## Purpose

Some users want a record of the content they produce via Content Operator. This guide handles the optional `my-content-log.md` file . a running archive of pieces the skill has produced, with their briefs.

Use this guide only when the user says yes to the "want to log this piece?" offer at the end of a session.

## What the Log Does

The content log is a growing file that captures:
- What content was produced
- When it was produced
- The brief behind it (topic, audience, angle, outcome)
- The final shipped version of the content

Why this matters:
- **Reference archive**: users can search past content for ideas, reuse, or remixing
- **Pattern recognition**: over time, the log reveals what topics/angles/formats the user produces most
- **Continuity for AI**: if the user loads the log file into future Content Operator sessions, the skill can reference past pieces ("last month you wrote about X, want to build on that?")

The log is optional. Not every user wants this level of tracking. Offer once, honor their answer.

## How to Handle the Log

### First time (file doesn't exist yet)

Create a new file called `my-content-log.md` with this structure:

```markdown
---
name: my-content-log
description: Running archive of content produced via Content Operator (Creator AI Skills Stack by Jim Carter III). Each entry contains the brief, production date, and final version of a piece of content. Reference this file when producing new content to maintain continuity with past pieces or to identify recurring topics and angles.
---

# Content Log . [USER'S NAME OR BUSINESS NAME]

This log tracks content produced via the JC3 Content Operator skill. Each entry is a snapshot of one production session.

## Entries

---

## [DATE] . [CONTENT FORMAT] . [SHORT TITLE OR HEADLINE]

**Brief:**
- **Topic:** [Specific topic from session]
- **Audience:** [Specific audience from session]
- **Angle:** [Hook or angle used]
- **Outcome:** [What the content was designed to drive]

**Final Content:**

[PASTE FULL FINAL CONTENT HERE]

---
```

### Subsequent times (file already exists)

Read the existing file. Append a new entry to the bottom:
- Keep existing entries intact
- Add a new `---` separator
- Add the new entry using the same structure
- Don't modify anything above the new entry

### Handling titles

If the content has a headline (like a newsletter or article), use the headline as the short title.
If the content doesn't have a clear title (like a LinkedIn post), generate a 4-7 word descriptor based on the topic:

Examples:
- "Why coaches burn out clients"
- "The meeting I cut"
- "Q3 launch retrospective"
- "My worst hire story"

Keep it short and scannable.

### Handling dates

Use ISO format: YYYY-MM-DD (e.g., 2026-04-16). This makes sorting easy and works across timezones.

## Deliver the Log File

After generating or appending to the log:

"Logged. Your content archive is at `my-content-log.md`.

You now have a running record of what you produced, when, and the brief behind it. Upload the file to your Claude Project if you want Claude to reference past content in future sessions. Useful for continuity, pattern recognition, and avoiding accidental repeats.

The log grows each time you run Content Operator and ask to log the piece. You can also edit it manually if you want to add pieces that were produced outside this skill."

## Rules for the Log

### Don't log automatically

Only log when the user explicitly says yes. Some users don't want tracking. Others will want to log every piece. Honor the per-session choice.

### Don't duplicate entries

If somehow the user asks to log a piece that's already in the log (same date, same brief), ask: "This looks like a duplicate of an entry from [date]. Replace the existing one, add as a new entry, or skip?"

### Don't modify past entries

Once logged, a piece stays as-is. If the user wants to update a past entry (added context, corrected something), point them to edit the file manually. The log is an archive, not a working document.

### Keep it clean

The log should stay readable even after 50+ entries. Maintain:
- Consistent separator format (`---` between entries)
- Consistent heading structure (date, format, title)
- No meta-commentary between entries
- No summaries or indexes (the user can use find/search)

If the user asks to add a table of contents or index as the log grows, offer: "Sure, but once added, you'll want to maintain it yourself or re-run a consolidation periodically. Alternatively, your editor's find-in-file (cmd+F) works well for these kinds of logs."

## Edge Cases

### User wants to log but the session produced an editing revision, not new content

"We were editing existing content, not producing new. The log is for pieces produced from scratch in Content Operator. If you want to log the edited version as a new entry (noting it was an edit of an earlier piece), we can. Want that?"

### User wants multiple entries from one session

Content Operator produces one piece per session by design. If somehow multiple deliverables came out of one session, confirm: "We produced [N] pieces. Log each one as a separate entry?"

### User wants to log a piece from before they started using Content Operator

"The log works for pieces we produce together in this skill. If you want to add historical pieces manually, you can edit the file directly using the entry template. Copy an existing entry and update the fields."

## After Logging

Return to Phase 6 (or 7 if Upgrade 2 doesn't apply) of the session flow. Close cleanly as normal.
