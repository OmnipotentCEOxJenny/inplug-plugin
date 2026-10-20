---
name: marketplace-guide
description: Explain how plugin marketplaces work and prepare a submission, covering the Grok Bot marketplace submit form (x.ai/bot/marketplace) and the Cursor Marketplace publisher terms. Use when a user asks how to list, submit or publish a plugin, or what a marketplace form requires.
---

# Marketplace guide

Follow `rules/pillars-and-scope.mdc`. Answer in the user's language; keep commands, file names and status labels unchanged. Facts below were read from the official pages on 2026-10-20; tell the user to re-check the live page before submitting, because forms and terms change.

## Grok Bot marketplace (https://x.ai/bot/marketplace/submit-a-plugin)
Fields seen on the form (2026-10-20): First Name and Last Name (max 40 each), Work Email, Organization Name (max 100), Organization Handle (max 40, no spaces or capitals), Website URL (optional), Logotype URL (1:1 SVG or PNG with a background plate, public URL), where to be listed (Grok (coming soon), Grok Bot, Cursor), MCP Server URL or Public GitHub Repository, Brief Description (max 600 characters), Testing Instructions (max 600 characters), and the checkbox "I've tested this plugin locally and in-app and confirmed it works as expected".
- House rule (not an xAI rule): keep the brief description under 200 characters and testing instructions under 580, counted with code, so nothing is cut off.
- Only tick the tested checkbox after real tests pass. Submitting means agreeing to the publisher terms, so the owner must read them and approve the submission.
- UNVERIFIED: how long review takes and how Grok Bot listings rank. The form page does not say.

## Cursor Marketplace (https://cursor.com/marketplace-publisher-terms, last updated May 6, 2026)
- Plugins must be free to users (3.1). Open-source parts must use permissive licenses such as MIT, BSD or Apache 2.0; GPL, AGPL and LGPL are not allowed (3.3).
- Descriptions and metadata must be accurate, complete and not misleading (4.5).
- Call the product "Cursor", never "Cursor AI" or "Cursor Code" (4.6).
- Do not collect Plugin Data beyond what the disclosed function needs, and never sell it (4.7); do not train models on it (6.3).
- After an update, the publisher requests a re-index instead of a new application (2.1). Cursor's docs say every plugin and update is manually reviewed and plugins must be open source (https://cursor.com/docs/plugins).

## Output
A checklist with each field, the draft text, its character count, and anything still UNVERIFIED. Never submit a form yourself unless the owner explicitly approves that exact submission.
