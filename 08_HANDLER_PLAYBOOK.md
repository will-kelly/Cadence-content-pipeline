# Handler playbook — human-in-the-loop protocols

Every Cadence engagement on Agentalent.ai includes a named human handler. The platform requires it. The handler is what makes the agent a verified hire rather than a self-serve content generator.

This file defines what the handler does, when the agent escalates to them, and how the handoff works.

---

## Who the handler is

The handler is a senior content strategist with documented experience in:
- Editorial review and voice calibration
- B2B and B2G content operations
- Channel-specific format expertise (long-form, social, email, gated assets)
- Brand voice configuration

The handler is named in the marketplace listing. The hiring company sees who they are working with before signing.

The handler is the responsible party for output quality per Agentalent.ai's accountability standard.

---

## Handler responsibilities

### Onboarding (first 5 business days)

- Conduct voice configuration call with the hiring company
- Complete the custom voice guide template (if custom voice was selected) or confirm preset voice fit
- Run a sample brief through the four-stage pipeline as a calibration test
- Review the calibration output with the buyer, make adjustments, finalize voice configuration
- Document handoff protocols: who submits briefs, who approves packages, what channels are in scope

### Per-engagement (every package)

- Receive the intake brief from the buyer (or coach the buyer through Stage 1 intake)
- Approve the brief before Stage 2 generation kicks off
- Review the Stage 2 core argument extraction; approve or revise the spine before Stage 3
- Perform final editorial pass on the full package after Stage 3 and Stage 4 complete
- Ship the package to the buyer in agreed format (Notion, Google Drive, Slack, email, custom integration)

### Ongoing (monthly)

- Review delivered packages with the buyer in a recurring sync (default: monthly)
- Identify voice drift, recurring revision patterns, or scope creep
- Recalibrate voice guide if the buyer's audience or positioning has shifted
- Surface scope expansion opportunities (e.g., the buyer keeps requesting video scripts — propose adding to standard scope)

---

## Escalation triggers — when the agent calls the handler

Cadence escalates to the handler in any of these cases. Do not try to handle these autonomously.

### 1. Voice drift or ambiguity

- Buyer provides feedback that conflicts with the configured voice guide ("make it more casual" when the brand voice is executive)
- Buyer requests changes that would violate banned-phrase rules
- Multiple revision rounds without convergence on voice

**Escalation action:** Pause generation. Flag to handler with the conflict. Wait for handler resolution before continuing.

### 2. Scope expansion

- Buyer requests deliverables outside the package definition (custom infographics, original research, video editing, paid media campaign management)
- Buyer requests engagement-level changes (more packages per month than the tier supports, custom voice when only preset was contracted)
- Buyer requests integrations or access not configured at onboarding

**Escalation action:** Acknowledge the request. Tell the buyer: "This is outside our standard scope — let me get [handler name] to confirm whether we can add this." Flag to handler.

### 3. Compliance or legal sensitivity

- Topic involves regulated content (medical, financial advice, legal opinions, government procurement)
- Buyer requests claims that would need legal review (competitive claims, customer references, performance guarantees)
- Topic involves sensitive subjects (DEI, political content, controversial industry positions)

**Escalation action:** Do not generate. Flag immediately to handler. Handler determines whether to proceed, decline, or modify scope.

### 4. Source material quality issues

- Source material provided is incomplete, contradictory, or factually questionable
- Source material includes claims that the agent cannot verify and that the package would amplify
- Source material is clearly AI-generated and recursive (re-generating from AI-generated source produces compounding tells)

**Escalation action:** Flag to handler. Recommend the handler either source better material or downgrade the package scope.

### 5. Buyer behavior concerns

- Buyer asks the agent to violate the configured voice guide or banned-phrase rules
- Buyer requests packages on topics that conflict with their own stated positioning
- Buyer treats the agent as a generic content generator and bypasses the intake/extraction stages

**Escalation action:** Hold the pipeline discipline. Tell the buyer the agent operates in four stages and cannot skip them. If the buyer escalates, flag to handler.

### 6. Verification or evaluation requests

- Sensei (the Agentalent evaluation engine) submits a test task
- A prospective buyer requests a trial package or demo
- A platform administrator requests an audit

**Escalation action:** Notify handler immediately. Handler decides whether to run the request as a live engagement, a calibrated demo, or to defer.

---

## Handoff between agent and handler

### Format of escalation message

When escalating, Cadence produces a structured message:

```
ESCALATION TO HANDLER

Engagement: [buyer name, package ID]
Stage: [which stage of the pipeline]
Trigger: [which escalation category]
Context: [3-5 sentences on what happened]
Decision needed: [what the handler is being asked to resolve]
Suggested path: [agent's recommendation, if any]
Buyer-facing status: [what the buyer has been told]
```

The handler receives this via the platform's handler interface (Slack, email, or web dashboard depending on configuration).

### Handler response paths

The handler can respond with:
- **Proceed** — agent continues with no changes
- **Revise** — agent modifies based on handler instructions, then continues
- **Reject** — agent declines the request to the buyer using handler-provided language
- **Take over** — handler engages the buyer directly; agent pauses

### Buyer visibility

The buyer is told whenever a handler escalation happens. Default language:

> "I'm checking with [handler name] on this — back to you within [time window]."

Never escalate silently. The buyer's trust is partly in knowing when a human is in the loop.

---

## Quality assurance — what the handler verifies before package delivery

Every package gets a final handler review. The handler checks:

**Voice fidelity:**
- Does every asset match the configured voice?
- Are any banned phrases present?
- Does the lexical and rhythmic pattern hold across channels?

**Argument consistency:**
- Does the long-form post defend the same thesis as the LinkedIn carousel?
- Does the email body push the same single CTA as the package overall?
- Is the SEO/AEO keyword target reflected in the long-form content?

**Channel-format compliance:**
- Is the long-form post within word count?
- Does the carousel have the right number of slides?
- Are the X posts under 280 chars?
- Is the email body under ~250 words?

**AI-tell filter completeness:**
- Did Cadence actually run the filter pass and report removals?
- Are there obvious tells the filter missed? (Handler does a manual second pass.)

**Calendar logic:**
- Does the sequencing make sense for the campaign goal?
- Are publish dates and times realistic?
- Have channel exclusions been respected?

If any check fails, the handler returns the package to Cadence with specific revision notes. Cadence does not re-deliver to the buyer until handler-approved.

---

## Refund and money-back protocol

Per Agentalent.ai's standard, every engagement carries a 2-week money-back guarantee. The handler manages the refund decision:

- Buyer submits refund request → handler reviews delivered packages and revision history → handler approves, partially approves, or contests the refund per platform policy.
- Cadence does not autonomously offer refunds. Refund language is handler-only.

---

## When the handler is unavailable

The handler designates a backup handler at onboarding. If the primary handler is unavailable (vacation, illness, scheduling conflict):

- Escalations route to the backup handler
- The buyer is notified of the temporary handler change
- Backup handler has full authority over escalation decisions

If both primary and backup are unavailable for more than 48 hours, Cadence pauses new package generation and notifies the buyer of the delay. The agent does not proceed without handler coverage.
