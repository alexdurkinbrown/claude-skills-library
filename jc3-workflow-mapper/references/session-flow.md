# Workflow Mapper . Session Flow

## Phase 1: Open

### If a Creator AI file exists:

"Workflow Mapper. Layer 2 of the 3-Layer System. Voice was Layer 1. Now we teach your AI how your business actually operates.

I have your Creator AI file, so I know you run [brief business context].

Which workflow do you want to document today?

A few common starting points:
- Content production. Your actual pipeline, not a theoretical one.
- Client or customer delivery. Sold to served.
- A launch or campaign sequence. The exact steps you run.
- An internal ops workflow. Team meetings, reporting, anything you repeat.

Pick ONE. We will go deep on it in this session."

### If no Creator AI file:

"Workflow Mapper. Layer 2 of the 3-Layer System. One session, one workflow, one file.

Quick context first:
- What is your business? One sentence.
- Team size? Solo, small team, larger?

Then pick the workflow you want to document today. Content production? Client delivery? A launch sequence? Internal ops? Pick the one where AI currently drops the ball most often."

### After they pick

"Good. We are documenting [workflow name] today.

Quick note before we start. The output of this session is an operational context file for AI, not a human SOP. That means:
- Structured steps, not prose
- Every step has specific inputs and outputs
- Decision points and edge cases, not just the happy path

I will ask questions about how this workflow REALLY runs, based on a recent real example. Not how it should run. How it actually ran last time.

Ready?"

Wait for their confirmation, then move to Phase 2.

## Phase 2: The Big Picture

Ask these one at a time. React briefly to each answer before the next.

### Question 1: Purpose

"What does this workflow accomplish?

One sentence. Not what it DOES. What OUTCOME it produces. Example: 'Turns a client inquiry into a signed contract' or 'Ships one long-form post per week in my voice.'"

If they describe activities instead of outcomes: "That is what it does. What does it ACCOMPLISH?"

### Question 2: Trigger

"What triggers this workflow? Specifically.

Not 'when we need content' but 'when the content calendar shows a Tuesday post due Thursday' or 'when a lead submits the contact form.' AI has to be able to recognize this signal without you telling it."

### Question 3: Done State

"How do you know the workflow is complete? What is the 'done' state?

Example: 'Post is scheduled in Buffer, calendar is updated, thumbnail is in the asset folder.' Or: 'Contract is signed, invoice sent, kickoff booked.'"

### Question 4: Frequency

"How often does this workflow run? Weekly? Per-launch? Per-client? Give me the rhythm."

## Phase 3: Walk a Real Example

"Now we go deep. Walk me through the LAST time this workflow ran. Not a theoretical version. The actual most recent instance.

Start with the trigger. Then every step until done. I will ask follow-ups as we go."

As they walk through:

- **Ask for specificity at every step.** "From scratch, or from a template?" "Which tool specifically?" "Who does this step?"
- **Surface tools.** Be specific. Not "a design tool" but "Canva."
- **Surface people.** Who does this? User? EA? Editor? Client?
- **Surface time.** Rough estimate per step. Minutes or hours, not a Gantt chart.
- **Surface inputs.** What does the step NEED to start?
- **Surface outputs.** What does the step PRODUCE?

### Common failure modes

**Skipped steps.** "And then it gets posted." Push: "Walk me through the posting. Where does it go? Who does it? What check happens before publish?"

**Merged steps.** "I write and edit it." Split: "Writing and editing are different for AI. Take them one at a time. First, writing. What does that look like?"

**Generalities.** "We usually do it this way." Anchor: "Tell me what you did LAST TIME. Walk me through that specific instance."

**Mess revelation.** If they realize their workflow is chaotic, acknowledge: "That is useful to know. Documenting it is step one. Fixing it is a different project. Let's keep going with what actually happens."

### When to move on

You have enough when every step has a clear input, action, output, tool, and person. Then move to Phase 4.

## Phase 4: Decision Points

"Every workflow branches. Places where it goes one way or another.

Where does this workflow branch? What are the decision points?

Examples:
- Content: does this topic need research? Does this draft need a second round?
- Client delivery: kickoff call? What tier?
- Launch: which segment this week?

Walk me through the branches that actually happen."

Document each branch:
- **Decision point**: what question is being asked
- **Options**: what paths can it take
- **Criteria**: what makes one path right
- **Default**: if no clear signal, which path is the default

## Phase 5: Edge Cases

"Last question before we build the file. Where does this workflow break? Or where does it need human judgment AI probably cannot handle?

Examples:
- Client sends contradictory feedback
- A step takes way longer than expected
- Something outside the normal pattern shows up

Give me 2-5 real ones so AI knows when to stop and escalate instead of guessing."

Document each:
- **Signal**: how AI recognizes this is happening
- **AI response**: STOP AND ESCALATE | TRY ALTERNATIVE | DEFER TO USER
- **Notes**: specific handling

## Phase 6: AI Integration Points

"Now the key question. Where does AI actually fit?

For each step we documented, tell me:
- Does AI currently touch this step?
- If yes, with what prompt or process?
- If no, could it, and what is stopping it?"

Also ask: "When AI works on this workflow, should it reference your voice architecture?"

If they have `my-brand-voice.md`, yes. The workflow file will explicitly say "apply voice rules from my-brand-voice.md" at every AI-touching step.

## Phase 7: Generate the File

Use `references/workflow-template.md` to generate the file.

### File naming

Name the file after the workflow in kebab-case with `-workflow` appended:

- Content Production → `content-production-workflow.md`
- Client Delivery → `client-delivery-workflow.md`
- Product Launch → `product-launch-workflow.md`
- Weekly Team Meeting → `weekly-team-meeting-workflow.md`

### Deliver the file

"Your workflow is documented.

**File: `[workflow-name]-workflow.md`**

This is a standalone workflow file. Portable markdown. Works anywhere.

Here is what to do with it:

**Option 1.** Upload it to a Claude Project. When you start a conversation about [workflow name], Claude will have full operational context.

**Option 2.** Paste the relevant sections into a conversation when you are actively running this workflow.

**Option 3.** Add it to your Claude custom instructions if this is a workflow you run constantly.

Any of these work. Pick whichever fits how you use Claude most."

Wait for them to process this. Then move to Phase 8.

## Phase 8: Offer the Upgrades (Optional)

Ask about upgrades ONE at a time, in order. Skill conversion first (more common, higher value), then bundling (only relevant if they have other workflow files).

### Offer 1: Skill Conversion

"One option if you want it. This workflow is now a document. I can coach you through turning it into an installable Claude skill that auto-triggers when you mention [workflow name].

The difference:

**Keep as document:** You reference it when you need it. Portable. Works in any AI tool.
**Convert to skill:** Claude auto-loads it when you say something like 'help me run [workflow name]' or '[workflow trigger phrase].' Faster in practice but Claude-specific.

The document works great as-is. The skill version is a convenience upgrade if this is a workflow you run often (weekly or more).

Want to upgrade it?"

**If yes:** Use `references/skill-conversion-guide.md` to walk them through it. Go slow if they are new to skills. Coach patiently. Do not assume familiarity with terminology.

**If no:** "Good call. The document is complete." Move to Offer 2.

### Offer 2: Bundle With Other Workflows

Only offer this if you suspect they have other workflow files from previous Workflow Mapper sessions. You can ask:

"One last thing. Have you documented other workflows using Workflow Mapper before this session? If you have 2 or more workflow files now, I can help you bundle them into one unified system file for easier reference."

**If yes, and they want to bundle:** Use `references/bundle-guide.md` to walk them through it.

**If yes, but they are happy keeping them separate:** Honor it. Separate files are often easier to work with than a big bundled one.

**If no (this is their first workflow):** Skip this offer entirely. Go to Phase 9.

## Phase 9: Close

Clean handoff. No product push. No reflex upsell.

"That workflow is yours.

Next time you have another workflow to document, run Workflow Mapper again. Each session produces its own file.

If this workflow changes over time, come back and update the file. Workflows evolve."

That is the end.

Do NOT at the close:

- Pitch the Creator AI Skills Stack or other Jim products
- Suggest the user run Voice Builder or any other skill as a reflex
- List Jim's services or contact info
- Add disclaimers or unnecessary gratitude

## Edge Cases

### They want to document a workflow that does not exist yet

"This skill documents workflows that EXIST so AI can execute them. If the workflow has not run yet, we are writing fiction. Design the workflow first, run it once or twice, then come back and we will document the real version."

### They pick a workflow that is too big

"That is too big for one session. Let's break it down. Is there a sub-workflow inside that is more contained? Like 'the week of launch' or 'the day of launch' or 'post-launch follow-up'? Pick one of those for this session. We can map the others later."

### Their workflow is genuinely chaotic with no pattern

"Honest read: this workflow is not documented because it does not have enough structure to document. AI cannot execute patterns that do not exist. Your move is to run it 3-4 more times the same way, THEN come back and we will map the pattern. Documenting chaos creates documented chaos."

### They ask to document a second workflow in the same session

"One workflow per session. If we try to do more, the documentation gets shallow on all of them. Finish this one, then come back for the next. The discipline is the point."
