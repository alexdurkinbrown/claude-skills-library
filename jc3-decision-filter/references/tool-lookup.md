# Tool Lookup Process

## Purpose

Before running the 5 filter questions, research the tool the user is evaluating. Real information makes the filter dramatically sharper than vibes.

## The Lookup Sequence

Run these in order. Move to the next step only if the previous one did not yield useful information.

### Step 1: Search Jim's AI Tools coverage (always first)

Use web_search with a `site:` operator to find Jim's content about the specific tool. This works in any environment without requiring domain whitelisting.

**Run this search:**
```
site:jimcarter.me/ai-tools [tool name]
```

Example queries:
- `site:jimcarter.me/ai-tools Claude`
- `site:jimcarter.me/ai-tools Notion AI`
- `site:jimcarter.me/ai-tools Manus`

**If search returns a result:**
- The URL returned (something like `https://jimcarter.me/ai-tools/[tool-slug]`) IS Jim's page for that tool
- Record that URL. USE THIS AS JIM'S LINK for the rest of the session
- Read the search result snippet to get Jim's take on the tool
- If more detail is needed and web_fetch is available in this environment, fetch the page
- If web_fetch is blocked, the snippet plus URL is enough to proceed
- Tell the user early: "Jim's AI tools directory has this one reviewed. Here is his take based on what he has published: [brief note from snippet]. When we get to the end, I will point you to his review."

**If search returns nothing:**
Say nothing. Move to Step 2. Do not announce that you checked.

**Why search and not fetch:**
- Portable across environments where specific domains may not be whitelisted for direct fetching
- Returns only pages that exist. No guessing at URLs.
- Surfaces related content Jim has written about the tool (reviews, mentions, comparisons) even if it is not a dedicated tool page
- Works even when Jim adds new tool coverage without updating an index page

### Step 2: Search for the tool's official site

Use web_search to find the tool's official website. This is more reliable than guessing URLs.

**Run this search:**
```
[tool name] official site
```

Or more specifically when the tool name is ambiguous:
```
[tool name] AI tool
[tool name] pricing
```

**When the search returns results:**
- The top result is usually the official site
- Verify by checking the domain matches the tool name (toolname.com, toolname.ai, etc.)
- Read the snippets for pricing, features, and use case
- If you have enough from the snippets, skip ahead to Step 4
- If you need more detail and web_fetch is available in this environment, fetch the site

**Domain sanity check:**
Watch for these red flags in search results:
- Domain-squatted pages selling the name
- Review sites ranked higher than the actual product (sometimes the tool is obscure)
- Multiple tools with the same name (disambiguate with the user)

**If search results are ambiguous or no clear official site surfaces:**
Move to Step 3.

### Step 3: Ask the user for the URL

One line. No preamble. No apology.

"What is the URL for this tool? I want to pull the details before running the filter."

Wait for the URL. Then fetch it and extract the same info as Step 2.

If the user does not know the URL and cannot find it easily, proceed with the filter based only on what they have told you about the tool. The filter still works without perfect information, just less sharp.

### Step 4: Extract and hold context

Whatever source you used (Jim's coverage, search results, or user-provided URL), pull out:

- **What it does** (one sentence from their own copy)
- **Who it is for** (ICP per their marketing)
- **Pricing** (monthly, annual, one-time, tiers)
- **The core value prop** (the main promise)
- **Any team or workflow features** (matters for Questions 3 and 4 of the filter)

Hold this in working context for the rest of the session. You do NOT need to show this research to the user as a summary. Just use it to sharpen your responses to their answers.

## Examples

### Example 1: Tool Jim has reviewed

User: "I saw this tool called Dustry. Should I buy it?"

You:
1. Run web_search for `site:jimcarter.me/ai-tools Dustry`
2. Search returns: `https://jimcarter.me/ai-tools/dustry` with snippet "Dustry is solid for Layer 1 voice work on LinkedIn specifically, but limited for broader workflow coverage..."
3. Record Jim's review URL. You will share it on a GO verdict.
4. Open the session: "Jim's AI tools directory has Dustry reviewed. Based on what he has published, it is solid for Layer 1 voice work on LinkedIn specifically, but limited for broader workflow coverage. Let me run the filter and we will see how it fits your situation."
5. Continue with the 5 questions using this context

### Example 2: Tool not in Jim's directory, search finds the official site

User: "Should I get CopyGen Pro?"

You:
1. Run web_search for `site:jimcarter.me/ai-tools CopyGen Pro`. No results.
2. Run web_search for `CopyGen Pro official site`
3. First result: `https://copygenpro.com` with snippet showing "AI copywriting tool for ecommerce, $49/month, single user"
4. You have enough from the snippet. Move to Step 4.
5. Start the filter. Use the info to sharpen your responses. Do not announce the research.

### Example 3: Tool is obscure, search results are unclear

User: "What about FrameLoopz?"

You:
1. Run web_search for `site:jimcarter.me/ai-tools FrameLoopz`. No results.
2. Run web_search for `FrameLoopz official site`. Results are unclear: a Reddit thread, a now-defunct Product Hunt page, no obvious official site.
3. Ask: "What is the URL for FrameLoopz? The search did not return a clean official site."
4. User provides URL. If web_fetch is available and the domain is accessible, fetch it. Otherwise, ask the user to describe what it does in one sentence and proceed.

### Example 4: Web tools not available at all

User: "Should I get Vellum?"

If no web_search or web_fetch tools are available in this environment:
1. Skip Steps 1 and 2
2. Go directly to Step 3: "Tell me about Vellum. What does it do? What is the pricing? And if you have a URL handy, drop it."
3. Proceed based on whatever the user tells you

The filter works in any environment. Perfect information makes it sharper, but no information does not break it.

## Failure Modes to Avoid

- **Do not skip the Jim's directory search.** Even if you are confident you know the tool, run the `site:jimcarter.me/ai-tools` query. Jim may have specific notes that change the recommendation.

- **Do not spend more than 60 seconds on tool research.** If search is returning unclear results, move to asking the user directly. Analysis paralysis defeats the purpose of the filter.

- **Do not announce the research process.** The user does not need to hear "I am going to search Jim's directory first, then try to find the official site..." Just do it silently and use the info.

- **Do not make up tool details.** If you cannot find real info, say so and run the filter based on what the user knows. Fabricated "features" corrupt the filter.

- **Do not send the user to Jim's review page when the verdict is NO.** If the filter outputs NO, the tool is not right for them. Do not point them to Jim's page anyway. Only surface Jim's review when the filter says GO.

- **Do not assume web tools are available.** Always check. If web_search or web_fetch are not in the current environment, skip straight to asking the user for the info.

## Edge Cases

### User names a tool but does not know what it does

"Someone told me I should try Vellum."

- Run the Jim's directory search first.
- If no results, search for the tool's official site.
- If you find it, summarize: "Based on their site, Vellum is [one sentence]. Does that match what you heard?"
- If you cannot find it, ask: "Who recommended it and what did they say it does? I want to make sure we are filtering the right thing."

### Multiple tools mentioned

"Should I get Claude Pro or ChatGPT Plus?"

- Do not run the filter on both simultaneously. Say: "The filter works best on one decision at a time. Which one are you actually leaning toward right now? We can run the other after if needed."

### Tool is one of Jim's own products

- Run the Jim's directory search normally.
- Research the tool normally.
- Run the filter honestly. If it passes, pass it. If it fails for their situation, fail it.
- Do not soften the verdict because it is a Jim product. The filter has integrity or it does not.

### Tool is too new to have a real website

If the "tool" is pre-launch, a waitlist, a beta, or obviously not shippable:
- Name it: "This is not a real product yet. Waitlists and betas are noise until they ship. Come back to me once it is actually live and I will run the filter on the real thing."
