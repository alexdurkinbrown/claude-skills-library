# Decision Filter . Scoring Rubric

## How to Score Their Answers

After asking all 5 questions, mentally grade each answer as GREEN, YELLOW, or RED. Do not share the grading with the user. It is for internal use to determine the verdict.

### Question 1: Layer Direction

- **GREEN**: Clear Layer 1, 2, or 3 move. They know what it does and it is upward.
- **YELLOW**: They can identify the layer but the case is weak. Or it moves them up marginally.
- **RED**: Layer 0 tool. Or they cannot tell you which layer it affects. Or "it makes AI smarter" type answers.

### Question 2: Compounding

- **GREEN**: Gets more valuable over time with a specific, plausible reason why.
- **YELLOW**: Could compound but depends on usage. Flat value for most buyers.
- **RED**: Static value. Or declines over time (like a prompt library that dates quickly).

### Question 3: Dependency

- **GREEN**: Works across their team. Or solo operator where team is not a factor.
- **YELLOW**: Starts with them, team can learn it later with effort.
- **RED**: Only they can use it. Creates a single point of failure. Makes them more of a bottleneck.

### Question 4: Tool or System

- **GREEN**: System. Something they own and take with them. Or a tool that enables a specific system build.
- **YELLOW**: Hybrid. Tool with some system features, but the system features are actually just product features.
- **RED**: Tool. Commodity. They are buying novelty or feature FOMO.

### Question 5: Real Cost

- **GREEN**: Realistic total cost. They factored in time, setup, learning, integration. Value is clearly worth the cost.
- **YELLOW**: Cost is reasonable but they have not fully accounted for the time drain.
- **RED**: Cheap tool they will never fully use. Or expensive tool whose total cost (time plus money) is disproportionate to the value.

## Verdict Logic

Count the grades across the 5 questions.

### GO verdict
- 4+ GREEN answers
- 0 RED answers
- If there is 1 RED, it has to be Q5 (real cost) and they have to demonstrate they are accepting the cost knowingly

### MAYBE verdict
- 2-3 GREEN answers and 2-3 YELLOW answers
- OR 1-2 RED answers that are not on Q1 or Q4

MAYBE means the decision is legitimately close. Explain the specific trade-off and give them the condition that would flip it to a GO.

### NO verdict
- 3+ RED answers
- OR RED on Q1 (Layer direction) regardless of other answers
- OR RED on Q4 (tool vs system) combined with any other RED

Q1 and Q4 are the two most important questions. If either comes back RED, the verdict is almost always NO. A tool that does not move them up a layer is noise. A tool disguised as a system is sales copy.

## How to Explain the Verdict

Name the specific answer that drove the verdict. Do not give a generic readout.

### GO example:

"This is a GO.

Why: You said it moves you from Layer 0 to Layer 1 (voice architecture), it compounds because every piece of content it generates reinforces the voice, and your whole team will use it. Total cost looks proportional to the value.

Next step: Block 30 minutes this week to actually set it up. The failure mode here is buying it and letting it sit. Do not let that happen."

### MAYBE example:

"This is a MAYBE.

Here is the trade-off. The tool itself is Layer 2 (workflow), which is a good move for you. But only you can use it right now, and you are already the bottleneck on your team's AI adoption.

The decision comes down to whether you will actually document what you learn and hand it off within 30 days. If you will, it is a GO. If 'someday' is more realistic, skip it. You have enough tools that only you can use."

### NO example:

"This is a NO.

Why: It is a Layer 0 tool. A commodity. You already have three AI tools that do roughly the same thing. This adds to the chaos, it does not reduce it. And the $29/month you would pay for this is $348 a year that could fund a real system build.

Instead: Save it. If you want to actually move up a layer, the work is voice architecture (Layer 1) or workflow memory (Layer 2). Neither of those is this tool."

## Tone Principles

- **Be direct.** "This is a NO" beats "I have some concerns about this."
- **Cite the specific answer.** Their own words should drive the verdict, not the framework.
- **Do not soften.** If the filter says NO, the user deserves to hear NO cleanly. Softening wastes their money.
- **Do not oversell when it is a GO.** The filter passed, not every purchase is transformational. Match the energy to the actual investment size.

## When the Decision Filter Itself Reveals a Bigger Gap

Sometimes the filter surfaces a problem bigger than the specific decision. Examples:

- They are evaluating Tool #7 in a chaotic stack. The real problem is the stack.
- They keep trying to buy their way out of a Layer 1 gap.
- They have been at Layer 0 for months and are still shopping for Layer 0 solutions.

In these cases, deliver the verdict on the specific decision first, THEN name the bigger pattern:

"Specific verdict: This is a NO on this tool.

But I want to name something bigger. This is the third AI tool you have evaluated in three months. The pattern is you are shopping for Layer 0 answers when your actual gap is Layer 1 or 2. More tools will not close that gap. A system will.

If that lands, the move is to stop tool-shopping and invest in a voice architecture or workflow system. Those are the layers that actually unlock leverage. Keep tool-shopping and the filter will keep saying no, because tools are not the answer to a system problem."

That is a fair observation to make. Not a reflex pitch. A genuine redirect based on what the filter surfaced.
