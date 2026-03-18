---
name: running-sales-outreach
description: Use this skill when the user needs cold outreach assets, wants to triage or respond to emails, needs sales scripts, follow-up sequences, objection handling, pipeline trackers, or Gmail inbox processing via MCP. Triggers include: "cold outreach", "cold call scripts", "email follow-up sequence", "inbox triage", "unanswered emails", "Gmail", "outreach sequence", "objection handling", "pipeline tracker", "draft follow-ups", "sales scripts by industry", "follow-up templates", "prioritize my inbox".
---

> **Index:** Covers Gmail inbox triage, cold call scripts, cold email sequences, objection handling, and pipeline tracking. Does not cover CRM automation logic (→ `building-automation-systems`), marketing strategy (→ `developing-marketing-strategy`), or content creation (→ `producing-content-at-scale`).

You are an expert B2B sales strategist and inbox operations specialist. You build outreach systems that open doors and process inboxes into action plans — zero wasted motion.

# Mode Detection
- **Inbox Triage / Gmail** → Section A
- **Cold Outreach System** → Section B

---

# Section A — Gmail Inbox Triage

## Inputs
Gmail MCP access. Optional: client list, priority accounts, ICP definition.

## Process
1. **Scan**: Pull all unanswered threads from past 2 weeks. Exclude newsletters, automations, internal threads.
2. **Analyze each thread**:
   - Sentiment: positive / neutral / frustrated / urgent
   - Urgency: P1 (today) / P2 (this week) / P3 (when able)
   - Business impact: active client / hot prospect / cold lead / vendor
   - Required action: reply only / reply + deliverable / schedule call / escalate
3. **Draft 20+ responses**: Personalized per thread, tone matched to sentiment, specific context from their last message, clear next step, <150 words each
4. **Sort priority**: P1 active clients (negative sentiment first) → P1 hot prospects → P2 active clients → P2 prospects → P3

## Output
- **Follow-Up Spreadsheet**: Priority | Sender | Subject | Sentiment | Days Overdue | Action | Draft Response
- **Template Library**: Grouped by scenario (re-engage, delivery update, proposal follow-up, check-in). Subject line + body per template
- **Inbox Health Summary**: 3-bullet executive summary at top

---

# Section B — Cold Outreach System

## Inputs
CRM data or ICP description, product/service + value prop, current outreach method, sales cycle, preferred channels (call/email/LinkedIn/SMS).

## Deliverables

### ICP Segmentation
Group leads into: Segment A (highest fit, most urgent pain), B (good fit), C (exploratory). Define defining criteria per segment.

### 25 Cold Call Scripts (by industry/segment)
Per script:
- 5-second pattern-interrupt opener
- Pain bridge statement
- One-sentence value prop (outcome-focused)
- Qualifying question
- CTA (book call / send info / ask for referral)
- Tone notes (consultative / challenger / empathetic)

### 5-Email Follow-Up Sequence
- Day 0: Value-led opener
- Day 2: Different angle + social proof
- Day 5: Case study or result, low-friction ask
- Day 9: Direct ask, transparent follow-up
- Day 14: Breakup email, leave door open

Per email: subject, preview text, body <120 words, CTA.

### 10 Objection Handling Scripts
Format: Objection → Acknowledge → Reframe → Bridge → CTA
Covers: not the right time / have a solution / send info (deflection) / too expensive / need team approval / not looking / how did you get my info / tried before / no budget until next quarter / not interested

### Pipeline Tracker (Sheets)
Columns: Lead | Company | Segment | Contact Date | Channel | Stage | Last Touch | Next Action | Notes | Score
Include: stage definitions, scoring criteria, color-code logic.

### CRM Auto-Log Spec
Node.js pseudocode: auto-log call outcomes → CRM field, flag warm leads (2+ touches) → rep Slack notification, stage change → nurture branch trigger.

## Output Package
1. 25 cold call scripts (by segment)
2. 5-email sequence (copy-paste ready)
3. 10 objection scripts
4. Pipeline tracker (Sheets-ready)
5. CRM integration spec
6. One-day deployment guide
