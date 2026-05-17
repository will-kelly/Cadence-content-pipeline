# Intake template — Stage 1

Use this when the buyer has not provided a structured brief. Ask in order. Do not skip ahead. After all answers captured, summarize back and request confirmation.

If the buyer opens with a structured brief, parse it, identify gaps, ask only for the gaps, and confirm. Do not re-interview when the work is done.

---

## Section A: The thing being said

**1. What's the topic or core thesis?**
   One sentence. If the buyer gives a vague topic ("AI in marketing"), push for the actual claim ("Most B2B marketing teams are running RAG pilots without owning the data layer").

**2. What pattern, dysfunction, or shift are you calling out?**
   This is what differentiates the piece from a generic vendor blog. Push for specificity. If the answer is "AI is changing things," the brief is not ready.

**3. What's the one concrete proof point that grounds this?**
   A stat, a named example, a pattern observed in market. If the buyer doesn't have one, flag it — the package will be weaker without it. Offer to source one during the engagement.

---

## Section B: The audience

**4. Who's the primary reader?**
   Job title, role, decision context. Examples: "CMOs at mid-market B2B SaaS firms," "Directors of engineering at federal IT contractors," "Marketing ops leads at enterprise insurance carriers."

**5. What's their current state on this topic?**
   Skeptical? Confused? Already convinced and looking for ammo? Worried they're behind? This shapes tone and entry point.

**6. What's the one action you want them to take after reading?**
   Subscribe, download the gated asset, book a consult, share the post, change their mind on something specific. Pick one. Multiple CTAs dilute the package.

---

## Section C: The campaign

**7. What's the campaign goal?**
   - Awareness (top of funnel, broad reach)
   - Lead-gen (gated asset, form-fill)
   - Nurture (existing list, deeper conviction)
   - Sales enablement (asset reps can hand to prospects)
   - Event drive (webinar, conference, launch)

**8. Which channel is the hero?**
   The "everything else supports this" asset. Common patterns: long-form post for thought leadership, gated asset for lead-gen, LinkedIn carousel for visibility plays, video for product launches.

**9. What's the publish window?**
   Hero asset publish date + any sequencing constraints (e.g., "carousel has to drop before the webinar on the 14th"). If unspecified, default to next Tuesday for hero asset.

---

## Section D: Source material

**10. What's the input?**
   - Existing draft to repurpose?
   - Voice memo, rough notes, transcript?
   - Internal research, analyst report, customer interview?
   - Raw observation or reaction to something in the market?
   - Competitor piece to push against?
   - Nothing — generating from scratch with intake answers only?

   Paste in or describe. The richer the input, the sharper the output.

---

## Section E: Voice configuration

**11. Which voice mode?**

   - **Preset voice:**
     - **Executive** — measured, board-facing, business-impact framing. For CIO/CFO/CEO audiences.
     - **Practitioner** — direct, pattern-recognition-forward, anti-hype. For engineering, IT ops, technical leadership.
     - **Marketer** — punchy, story-driven, emotionally resonant. For marketing, sales, customer-facing.
   - **Custom voice** — load the brand voice guide configured at onboarding.

   If the buyer is unsure, propose based on audience: executive audience → executive voice, technical audience → practitioner, marketing audience → marketer. Confirm before proceeding.

**12. Voice modifiers for this engagement?**
   - More confrontational or more measured than the default?
   - Specific phrases the brand wants emphasized or avoided?
   - Channel-specific tone shifts (e.g., warmer on email than on LinkedIn)?

---

## Section F: Constraints

**13. Any banned phrases or topics?**
   Default banned list comes from `AI_TELL_FILTER.md`. Buyer may add brand-specific guardrails — competitor names, regulated terms, controversial topics.

**14. Any required quotes, citations, or compliance language?**
   For regulated industries (finance, healthcare, federal), legal-required disclaimers, attribution to executives or customer references, or compliance-reviewed copy blocks.

**15. Any channel exclusions?**
   If the buyer doesn't publish on X / Twitter, doesn't run gated assets, or has paused email, mark those channels out of scope and rebalance the package.

---

## Confirmation step

After all answers captured, summarize back in this format:

```
BRIEF SUMMARY

Thesis: [one sentence]
Audience: [job title + state]
Goal: [campaign goal]
Hero channel: [channel]
Publish window: [date]
Source: [input type + key content]
Voice: [preset name or "custom brand voice"]
Modifiers: [any]
Constraints: [any]
Channel mix: [confirmed channels]

Proceed to Stage 2 (core argument extraction)? Y/N
```

Wait for explicit Y. If N or "wait" — loop back to the question they want to revise. Do not regenerate the brief from scratch.

---

## Quality gates before moving on

Do not advance to Stage 2 if:

- The thesis is a topic ("AI in healthcare") rather than a claim
- The audience is undefined or "everyone"
- The campaign goal is "all of the above"
- No source material AND no concrete proof point
- Voice mode is unconfirmed

Push back on the buyer in these cases. The pipeline produces weak output from weak briefs, and the human handler will reject it on review.
