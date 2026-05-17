# AI-writing filter — Stage 4

This filter runs on every package before delivery. It catches the patterns that mark text as machine-generated and edits them out. The filter is mandatory. No package ships without a filter pass.

## How the filter works

After generating all assets, scan each one for the patterns below. For each match:

1. **Flag it** — note where it appeared
2. **Decide** — is this load-bearing or filler? Most matches are filler.
3. **Edit** — remove or rewrite. Default to removal.
4. **Re-read** — does the paragraph still work? Often it works better.

At the end, state to the user: "Filter pass complete. Flagged and removed: [list]."

---

## Pattern 1: The em-dash crutch

LLMs overuse em-dashes as a rhythm device. Will uses em-dashes too, but sparingly and load-bearingly. Cut em-dashes when:

- A period or colon would work as well
- The em-dash is being used to soften a claim ("This is broken — but there's a path forward")
- The sentence has two em-dashes within five words of each other

**Keep em-dashes when:**
- They set off a genuinely parenthetical aside
- They land a punchline that needs the pause

**Detection heuristic:** If a paragraph has three or more em-dashes, at least two are filler. Cut them.

---

## Pattern 2: "It's not just X — it's Y"

This construction is one of the most reliable AI tells in 2025. Other variants to catch:

- "This isn't just X. It's Y."
- "It's more than X — it's Y."
- "Not only X, but also Y."
- "This isn't about X. It's about Y."

**Rewrite move:** Drop the "not just" half. Lead with Y directly. If Y matters, it can stand on its own.

Bad: "Documentation debt isn't just a content problem — it's a governance problem."
Better: "Documentation debt is a governance problem. The content team gets blamed for it."

---

## Pattern 3: Setup openers

LLMs love to open paragraphs (and posts) with throat-clearing setups. Catch and cut:

- "In today's [fast-paced / rapidly evolving / AI-driven / complex] [landscape / world / environment]"
- "As organizations increasingly..."
- "With the rise of..."
- "In an era where..."
- "Imagine a world where..."
- "Picture this:"
- "We've all been there."

**Rewrite move:** Delete the setup. Whatever comes after it is the actual opening.

---

## Pattern 4: Hedge constructions

LLMs hedge to seem balanced. Will doesn't hedge. Cut:

- "Whether you're X or Y"
- "Regardless of your role"
- "No matter where you are in your journey"
- "Every organization is different, but..."
- "While there's no one-size-fits-all..."
- "It depends, of course"

**Rewrite move:** Pick a position. Address one reader, not "any" reader.

---

## Pattern 5: The tricolon

Three-adjective stacks are an AI fingerprint. Patterns to catch:

- "Strategic, scalable, and sustainable"
- "Fast, flexible, and future-proof"
- "Clear, concise, and compelling"
- Any three-adjective list joined by Oxford commas in marketing prose

**Rewrite move:** Pick the one adjective that's actually doing work. Drop the other two.

---

## Pattern 6: Conversational filler verbs

"Let's [dive / explore / unpack / dig into / break down]" is LLM-typical, especially in opening lines and section transitions. Other filler:

- "We'll start by..."
- "Now let's turn to..."
- "Before we dive in..."
- "First, let's take a step back."

**Rewrite move:** Cut the meta-narration. State the next thing directly.

---

## Pattern 7: Vendor-deck vocabulary

Words that signal you've been trained on too many SaaS landing pages. Hard ban list:

- Unlock / empower / accelerate / streamline / optimize (when used as marketing-verb filler)
- Leverage (as a verb)
- Robust / seamless / cutting-edge / best-in-class / world-class
- Game-changer / paradigm shift / sea change
- Mission-critical (only allowed when literally true)
- Drive value / drive outcomes / drive impact
- Navigate the complexities / navigate the [anything]
- Holistic (unless about literal systems thinking)
- Synergy / synergistic
- Move the needle

**Rewrite move:** Replace with the specific verb that says what the thing actually does.

---

## Pattern 8: The "important to note" qualifier

LLMs insert epistemic hedges. Cut:

- "It's important to note that..."
- "It's worth mentioning..."
- "Notably,"
- "Of course,"
- "That said,"
- "Having said that,"
- "With that in mind,"

**Rewrite move:** Just say the thing. The hedge adds nothing.

---

## Pattern 9: The closing summary

LLMs end posts by summarizing what they just said. Will doesn't. Cut:

- "In summary..."
- "To recap..."
- "The bottom line is..."
- "At the end of the day..."
- "Ultimately,"
- "In conclusion,"
- Any final paragraph that restates the post's argument in different words
- Any section header that says "Conclusion" or "Final thoughts" or "Key takeaways" (unless the asset format explicitly calls for a takeaways block)

**Rewrite move:** End on the last substantive line of argument. Trust the reader.

---

## Pattern 10: Listicle-voice flattening

LLMs default to bulleted lists even when the argument needs prose. Catch when:

- A claim that could be made in one strong sentence has been broken into a 5-bullet list
- Bullet items are all the same length and grammatical structure (parallelism done robotically)
- A post has three or more bullet lists in under 1,000 words

**Rewrite move:** Convert the strongest bullet list into prose. Keep bullets only where the format genuinely needs them (e.g., a checklist, a comparison, a numbered procedure).

---

## Pattern 11: The "journey" / "navigate" metaphor

LLMs reach for journey metaphors constantly. Cut:

- "Your AI journey"
- "The transformation journey"
- "Navigate the [AI / cloud / digital] landscape"
- "Embark on..."
- "Roadmap to..."
- "Path to..."

**Rewrite move:** Use the literal noun. "Your AI rollout." "The migration." "What to do next."

---

## Pattern 12: Bothsidesing

LLMs balance every claim with a counter-claim to seem neutral. Will is not neutral. Cut:

- "On one hand... on the other hand..."
- "While X has benefits, Y also has merits"
- "Both approaches have their place"
- Any sentence that takes a position and then immediately walks it back

**Rewrite move:** Pick one side. State it. Move on. If counter-arguments matter, address them explicitly in their own paragraph — don't dilute every claim.

---

## Pattern 13: Adjective-stacked AI flattery

LLMs over-praise. Cut:

- "Revolutionary"
- "Groundbreaking"
- "Transformative" (unless you can name the specific transformation)
- "Cutting-edge"
- "Next-generation"
- "State-of-the-art"
- "Innovative" (especially as a filler adjective in front of a noun)

**Rewrite move:** Replace with what the thing actually does or what makes it different.

---

## Pattern 14: Symmetric paragraph structure

A subtle but reliable tell: every paragraph in the post is roughly the same length. Every paragraph opens with a claim, gives an example, and closes with a transition. This rhythmic uniformity is machine-generated.

**Rewrite move:** Vary paragraph length deliberately. Some paragraphs should be one sentence. Some should be six. Break the rhythm.

---

## Pattern 15: Bracket-of-three section headers

LLMs structure long posts with three-word, parallel section headers. ("The Strategy. The Tactics. The Tools.") Catch and break the pattern. Real human writers don't structure that cleanly.

**Rewrite move:** Mix header styles. Use a question, a claim, a phrase. Don't make them parallel.

---

## Final filter pass — the read-aloud test

After running all 15 patterns, read the final draft aloud (mentally). Ask:

1. Does any sentence sound like a vendor wrote it?
2. Does any paragraph open with throat-clearing?
3. Are there three or more bullet lists?
4. Does the ending summarize what was said?
5. Could this run on three different SaaS blogs with the logo swapped?

If yes to any — keep editing.

---

## What to report to the user

After the filter pass, report:

```
FILTER PASS COMPLETE

Flagged and removed:
- [pattern type]: [count] instances in [asset name]
- [pattern type]: [count] instances in [asset name]
...

Total edits: [N]
```

Keep this short. The user wants to see that the filter ran, not a full audit report.
