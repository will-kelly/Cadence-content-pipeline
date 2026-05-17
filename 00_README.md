# Cadence — Agentalent.ai submission package

A multichannel content marketing production agent designed for submission to the Agentalent.ai marketplace. Cadence takes a single content brief and produces a complete multichannel marketing package, calibrated to the hiring company's brand voice and filtered for obvious AI-writing tells.

This folder contains everything required to submit Cadence as a verified agent on Agentalent.ai under the Marketing role category.

---

## What's in this folder

| File | Purpose | Where it goes |
|------|---------|---------------|
| `00_README.md` | This file — submission packet overview | Reference only |
| `01_AGENT_PROFILE.md` | Agent identity, role definition, capabilities, pricing | Internal reference + source for marketplace listing |
| `02_SYSTEM_PROMPT.md` | The operational system prompt that runs Cadence | Loaded into the agent runtime |
| `03_INTAKE_TEMPLATE.md` | Stage 1 — structured brief intake | Knowledge file loaded by the agent |
| `04_VOICE_LIBRARY.md` | Three preset voices + custom voice loader | Knowledge file loaded by the agent |
| `05_AI_TELL_FILTER.md` | 15-pattern filter for AI-writing detection | Knowledge file loaded by the agent |
| `06_CHANNEL_SPECS.md` | Format and length specs per channel | Knowledge file loaded by the agent |
| `07_CALENDAR_TEMPLATE.md` | Content calendar block format and sequencing | Knowledge file loaded by the agent |
| `08_HANDLER_PLAYBOOK.md` | Escalation paths and human-in-the-loop protocols | Knowledge file loaded by the agent + handler reference |
| `09_EXAMPLE_PACKAGE.md` | Full worked example with a generic B2B SaaS brand | Reference for Sensei evaluation testing |
| `10_MARKETPLACE_LISTING.md` | Buyer-facing copy for the Agentalent.ai profile | Paste into platform's agent listing form |

---

## Submission workflow

### 1. Register as an agent builder on Agentalent.ai

Go to `agentalent.ai/agent/login` and create a builder account. You'll need:
- A business identity (LLC, sole proprietorship, or registered consultancy)
- A named human handler who can be the accountable party for Cadence's output
- A backup handler designated at registration
- A communication channel (Slack workspace, email address, or dedicated handler dashboard)

### 2. Create the agent listing

Paste content from `10_MARKETPLACE_LISTING.md` into the platform's listing form, section by section. The platform's intake assistant (Chloe) can help convert this into the platform's required schema.

### 3. Configure the agent runtime

Load the system prompt from `02_SYSTEM_PROMPT.md` and the knowledge files from `03_INTAKE_TEMPLATE.md` through `08_HANDLER_PLAYBOOK.md` into your chosen agent runtime (Claude Project, custom Anthropic API integration, or other framework supported by Agentalent.ai).

The agent expects all knowledge files to be loaded at startup. The system prompt references them by filename.

### 4. Submit for Sensei verification

Sensei is Agentalent.ai's open-source evaluation engine. Cadence is designed to be tested on five tasks documented in `01_AGENT_PROFILE.md` under "Verification readiness":

1. Brief-to-package run
2. Voice match test
3. AI-tell removal test
4. Ambiguity handling
5. Feedback loop

The worked example in `09_EXAMPLE_PACKAGE.md` is intended as the reference output shape for Sensei evaluators. Submit it as part of the verification packet.

### 5. Configure pricing and contract terms

Pricing tiers and engagement structure are documented in `01_AGENT_PROFILE.md` and `10_MARKETPLACE_LISTING.md`. Configure the platform's pricing fields to match:
- Standard retainer: $2,400 / month
- Pro retainer: $4,800 / month
- Gig pricing: $600 / package
- Enterprise: custom (handled outside platform)

All tiers include the 2-week money-back guarantee per Agentalent.ai's standard.

### 6. Set up handler routing

Configure the platform's handler routing rules per `08_HANDLER_PLAYBOOK.md`. Every escalation trigger should route to the named handler, with the backup handler covering unavailability windows.

---

## What makes Cadence verifiable as a hire (vs. a content generator)

Three structural differences:

**1. Four-stage pipeline discipline.** Every engagement runs through intake → core argument extraction → multichannel generation → AI-tell filter pass. The stages are visible to the buyer. The discipline is part of the deliverable.

**2. Named human handler with editorial accountability.** Every package gets a final handler review before delivery. The handler is named on the listing, available for escalations, and the responsible party for output quality. This satisfies Agentalent.ai's human-supervision requirement.

**3. AI-tell filter report ships with every package.** Buyers see exactly what got caught and removed. This audit trail is the differentiator from generic content generators that produce AI-flavored output at scale.

---

## Voice configuration model

Cadence supports both preset and custom voice modes:

**Preset voices** (configured in `04_VOICE_LIBRARY.md`):
- Executive — board-facing, business-impact framed
- Practitioner — pattern-recognition, anti-hype
- Marketer — punchy, story-driven

**Custom voice** — buyer completes a voice guide template at onboarding; handler verifies fit and calibrates with a sample package before the first paid engagement.

Voice mode is locked at onboarding and selectable per engagement. Multi-voice configuration (Pro tier) supports multiple brand voices within one engagement.

---

## Customization for other deployments

If deploying Cadence outside Agentalent.ai (e.g., as a Claude Project for a single client, as a licensed system for a consultancy, or as a Gumroad / Notion Marketplace template):

- The handler-playbook scope (`08_HANDLER_PLAYBOOK.md`) is Agentalent-specific. Other deployments may not require the same escalation model.
- The marketplace listing copy (`10_MARKETPLACE_LISTING.md`) is Agentalent-specific. Strip or rewrite for other platforms.
- The system prompt (`02_SYSTEM_PROMPT.md`) references "Agentalent.ai platform" and "human handler" in its operating context section. Adjust for other deployments.

The pipeline itself — intake, argument extraction, generation, filter — is portable.

---

## What this is NOT

- Not a content generator. The intake and filter stages are the deliverable's value.
- Not a substitute for editorial judgment. The handler reviews every package before delivery.
- Not a vendor blog factory. If the output reads like SaaS marketing, the filter has failed and the package goes back.
- Not an autonomous publishing system. The human team ships; Cadence delivers drafts.
