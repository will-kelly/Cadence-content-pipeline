# Voice library

Cadence operates in one of two voice modes per engagement: a preset voice from the library below, or a custom brand voice configured at onboarding. The voice mode is locked during Stage 1 intake and applied across all assets in the package.

---

## Preset 1: Executive

**For audiences:** CIOs, CFOs, CEOs, board members, senior executives at enterprise organizations.

**Tone:** Measured, authoritative, business-impact-framed. Sounds like a senior peer briefing the C-suite, not a vendor selling to them.

**Signature moves:**
- Lead with business outcome, not technology
- Frame technical concepts in terms of risk, cost, or competitive position
- Use precise quantification where defensible ("18% margin compression" beats "significant margin pressure")
- Reference market dynamics, not feature comparisons
- Close with implication for capital allocation or strategic priority

**Sentence rhythm:**
- Medium-length sentences. Few short ones for emphasis.
- Subordinate clauses are fine — executive readers tolerate complexity.
- Avoid em-dashes used for casual rhythm; use them for genuinely parenthetical asides only.

**Banned phrases (in addition to global AI-tell filter):**
- "Disruptive" (overused, hollow)
- "Synergy" / "synergistic"
- "Best practices" (without naming the practice)
- "Industry-leading" (without proof)
- "Future-proof" (almost always meaningless)
- "Holistic" (unless about literal systems thinking)

**Example sentence in executive voice:**
> "The cost of unmanaged AI experimentation across business units now exceeds the operating budget of most internal tools functions, and the board-level question is no longer whether to centralize AI governance but who owns the P&L when it's centralized."

---

## Preset 2: Practitioner

**For audiences:** Engineers, IT ops, technical leadership, security architects, SREs, anyone who builds or operates systems.

**Tone:** Direct, pattern-recognition-forward, anti-hype, peer-to-peer. Sounds like someone who has actually shipped the thing, not someone marketing the thing.

**Signature moves:**
- Name the pattern before naming the symptom
- Lead with the diagnosis, not the setup
- Reference specific tools, vendors, frameworks by name
- Push against vendor-deck conventional wisdom
- Use practitioner asides ("In production, what actually happens is...")
- End paragraphs on a sharp line, not a transition

**Sentence rhythm:**
- Vary length aggressively. Short. Then a longer sentence that does the actual work. Then short again.
- Hard periods, not "however / that said" pivots.
- Em-dashes only when load-bearing.

**Banned phrases (in addition to global AI-tell filter):**
- "Best-in-class"
- "Robust" / "seamless"
- "Cutting-edge" / "next-generation"
- "Game-changer"
- "Unlock" / "empower" / "navigate the complexities"
- "Mission-critical" (unless literally true)

**Example sentence in practitioner voice:**
> "Most enterprise RAG pilots fail because the team building the retrieval layer reports to a different VP than the team owning the source-of-truth systems, and nobody noticed the org chart problem until the model started returning stale data three months into production."

---

## Preset 3: Marketer

**For audiences:** Marketing teams, sales orgs, customer success, growth roles, creative leadership.

**Tone:** Punchy, story-driven, emotionally resonant. Sounds like a confident marketing leader who knows what makes content move, not a B2B blogger churning out thought leadership posts.

**Signature moves:**
- Open with the hook, not the context
- Use concrete imagery — name the moment, the email, the campaign
- Embrace short paragraphs and white space
- Reference specific results and named campaigns (own work or industry examples)
- Close with a specific action, not a general principle
- Allow yourself one rhetorical flourish per piece — but only one

**Sentence rhythm:**
- Short paragraphs. One- and two-sentence paragraphs are normal.
- Fragments are fine when they punch.
- Vary opener structure — don't start three paragraphs with "And" or "But."

**Banned phrases (in addition to global AI-tell filter):**
- "Move the needle"
- "Drive engagement"
- "Crush it" / "killing it"
- "Authentic" (overused — show, don't claim)
- "Storytelling" (used as a verb-noun in marketing-speak)
- "At scale" (when it's filler)

**Example sentence in marketer voice:**
> "The campaign worked because we cut the third paragraph. The first two paragraphs did all the work, and the third was the part the legal team made us add for no reason anyone could remember."

---

## Custom voice loader

When the hiring company has completed the voice guide template at onboarding, load the custom voice as default. The custom voice guide should contain:

**1. Tone descriptor** (one paragraph)
The company's own description of how they sound. Often pulled from existing brand guidelines.

**2. Audience definition**
Who the voice speaks to. Specific job titles, decision contexts, urgency level.

**3. Signature moves** (5–10 bulleted)
Specific rhetorical patterns the brand uses. Examples: "We always lead with the customer's job-to-be-done, not the feature." "We end pieces with a concrete next step, not a summary."

**4. Banned phrases** (specific to the brand)
On top of the global AI-tell filter. Common additions: competitor names, deprecated product names, regulated terms, executive-banned clichés.

**5. Required phrases or framings** (optional)
Brand-mandated language: tagline placements, executive titles, customer reference attribution, compliance-required disclaimers.

**6. Sentence rhythm preferences**
Average sentence length, paragraph length, header style (sentence case vs. title case), use of bullets vs. prose.

**7. Channel-specific calibration**
How the voice shifts per channel. Example: "More direct on LinkedIn, more measured in the blog, conversational in email."

**8. Example samples**
Three sample pieces (paragraphs or full posts) that exemplify the voice. The model uses these as ground truth for lexical and rhythmic fidelity.

---

## How voice gets selected

In Stage 1 intake, ask the buyer which voice mode applies. If the buyer is unsure:

- Audience is C-suite / board → propose Executive
- Audience is technical / operational → propose Practitioner
- Audience is marketing / sales / customer-facing → propose Marketer
- Audience is mixed → ask the buyer to pick the dominant audience and configure for them

If a custom voice guide exists for the hiring company, default to custom and offer the presets only as alternates.

---

## Voice consistency across channels

The voice register is consistent across all channel assets in a package. Channel format changes (carousel slides are shorter than long-form paragraphs), but voice doesn't.

The one exception: email body voice is typically softened by one notch toward direct address. Practitioner voice in long-form becomes practitioner-warm in email. This is a calibration shift, not a voice change.

If a hiring company specifies different voices per channel (rare but valid), apply per-channel routing during Stage 3 generation and note the voice for each asset in the deliverable.
