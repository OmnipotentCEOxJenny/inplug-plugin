# InPlug Plugin

InPlug Plugin is a free guide for people who want to build, improve and publish plugins. It explains how the Grok Bot marketplace (x.ai/bot/marketplace) and the Cursor Marketplace work, what their submit forms and publisher terms ask for, how to build a plugin in the Cursor plugin format (manifest, skills, rules, MCP servers), and how to test, version and translate it honestly. Every fact cites the official page it came from, with the date it was read; anything not confirmed is marked UNVERIFIED.

Invented by Rob Domaine / Omnipotent Media LLC.

![InPlug Plugin logo](assets/logo.png)

## Project status: done, pending, uncertain
**Done**
- 2026-10-20: v1.0.1 host-AI test from a fresh clone: the three reviewer prompts answered with the skills loaded, checked against the official sources (11/11 checks PASS), and the hello-notes scaffold created and validated (8/8 PASS).

**Pending**
- In-app load test in Cursor (`~/.cursor/plugins/local`) or Grok Build: not done; the build computer has neither app.
- Marketplace review: submitted 2026-10-20, pending, no approval yet. (This line previously said "not submitted"; that was wrong and is corrected in 1.0.5.)

**Uncertain**
- Whether Grok Build reads the `.cursor-plugin/plugin.json` manifest format (UNVERIFIED).

## Testing status (corrected 2026-10-23)
- Local automated tests: PASS on 2026-10-23 (`python3 tests/check_frontmatter.py`: plugin.json is valid JSON and every SKILL.md and rules file has valid front matter). Earlier local tests are listed under Project status above.
- In-app testing (loading the plugin inside the Cursor app or Grok Build): **not yet completed**. It is pending.
- Correction: when this plugin was submitted to the Grok Bot marketplace (2026-10-20), the submit form's "I have tested this plugin locally and in-app" confirmation was checked in error. Only local testing had been done. This was a mistake by Jenny Echo, the AI assistant that built and submitted the plugin, not a choice by the publisher, Rob Domaine. This plugin should not be described as tested in-app until that test has actually been done and recorded here.

## Quick start
1. Install from https://github.com/OmnipotentCEOxJenny/inplug-plugin (copy to `~/.cursor/plugins/local/inplug-plugin` and reload).
2. Ask: "What does the Grok Bot marketplace submit form need, and how long can my description be?"
3. Or: "Scaffold a plugin called hello-notes" or "Check my plugin before I release 1.0.1."

## Testing
1. Ask the marketplace-guide skill for the Grok Bot form fields.
2. Expected: Brief Description and Testing Instructions max 600 characters each, Logotype URL as 1:1 SVG or PNG with a background plate, the tested checkbox, and a reminder that it never submits for you.
3. Compare with `examples/submission-checklist.md`.

## Credits
- Inventor and publisher: Rob Domaine / Omnipotent Media LLC
- Builder: Jenny Echo
- InPlug Plugin is independent and not endorsed by xAI or Anysphere (Cursor).

## Rob Domaine's four pillars
1. Trustworthy, honest, real data, truthful: never invent; anything unchecked is marked UNVERIFIED.
2. Use only legitimate means: legitimate, proven sources and methods; unreliable sources rejected.
3. Double-check everything: every finding is confirmed by two independent checks, and the report shows both.
4. Stay within the law and rules always: local, county, state, federal and platform rules.

## Components
- `skills/marketplace-guide`: marketplace forms, limits and publisher terms.
- `skills/build-a-plugin`: plugin layout, manifest, skills, rules, MCP (SDK 2.x note).
- `skills/improve-a-plugin`: tests, sequential versions, tags, honest limits, translations.
- `rules/pillars-and-scope.mdc`: Rob Domaine's four pillars and language rules.
- `examples/submission-checklist.md`: a worked example run.
- `TRANSLATIONS.md`: title, description and honest assessment in 23 languages (machine-made).

## Sources (read 2026-10-20)
- Grok Bot submit form: https://x.ai/bot/marketplace/submit-a-plugin
- Cursor Marketplace Publisher Terms (last updated May 6, 2026): https://cursor.com/marketplace-publisher-terms
- Cursor plugin docs: https://cursor.com/docs/plugins
- MCP Python SDK 2.3.0 on PyPI: https://pypi.org/project/mcp/2.3.0/

## Languages
The AI answers in the user's language and keeps commands, file names and status labels unchanged. Title, description and honest-assessment summaries in 23 languages are in TRANSLATIONS.md: Español, Français, Português, Deutsch, Italiano, Nederlands, Polski, Русский, Українська, Türkçe, العربية, עברית, فارسی, हिन्दी, বাংলা, اردو, 简体中文, 日本語, 한국어, Bahasa Indonesia, Tiếng Việt, Kiswahili, Tagalog / Filipino. They are machine translations, not yet reviewed by native speakers; the English text is authoritative. Each language section in TRANSLATIONS.md also starts with a one-line machine-translation notice in that language.

## License
MIT. See `LICENSE`.

## Honest assessment: what this plugin cannot do
Written to be fully transparent. If something here is wrong or out of date, please open an issue.

- It does not submit, publish or re-index anything for you, and it cannot guarantee approval on any marketplace.
- Its facts about forms, limits and terms were read from the official pages on 2026-10-20 and can go out of date; always re-check the live page before submitting.
- It does not run code, host an MCP server, or test your plugin inside a host app; you run the tests. Submitting needs your own accounts and sign-in.
- Review times, ranking and how Grok Bot handles updates are not published, so they are marked UNVERIFIED.
- It has been tested by an AI reading its skills and on the build computer, but not yet loaded inside the Cursor app or Grok Build.
- Marketplace status: not submitted yet; once submitted it stays pending until approved.
- It collects no data, needs no account or API key, and costs nothing.
- Translations: the 23 translated summaries in TRANSLATIONS.md are machine-made and have not been reviewed by native speakers. The English text is authoritative.
- It is not legal advice and cannot guarantee that any particular use is lawful; you remain responsible for how you use it.
- Rules and compliance: it is built to follow all local, county, state and federal laws and every platform's rules. It uses no paid services, never bypasses logins, paywalls, CAPTCHAs or access controls, and never claims a feature it does not have.
