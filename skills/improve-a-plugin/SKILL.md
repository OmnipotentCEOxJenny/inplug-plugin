---
name: improve-a-plugin
description: Test, fix and release a better version of an existing plugin with sequential versions, honest limits and translations. Use when a user wants to review, upgrade, version or translate a plugin.
---

# Improve a plugin

Follow `rules/scope.mdc`. Answer in the user's language; keep commands, file names and status labels unchanged.

1. **Test for real:** manifest parses as JSON; every skill and rule has valid front-matter; every path in the manifest exists; the logo is square and its public URL returns HTTP 200; form texts are length-checked with code; run one worked example of each skill.
2. **Fix and version:** bump the version in sequence (1.0.0 to 1.0.1 for fixes, 1.1.0 for features). Add a CHANGELOG entry. Create a new tag; never move, delete or rewrite a published tag, and never back-fill skipped versions.
3. **Honest limits:** keep a "what this plugin cannot do" section current. Remove any claim you cannot prove.
4. **Translations:** translate the title, description and limits; label them as machine translations until a native speaker reviews them; keep commands, paths and status labels untranslated.
5. **Marketplace updates:** on Cursor, request a re-index after an update instead of a new application (publisher terms 2.1). On Grok Bot, UNVERIFIED: the form does not describe updates; do not resubmit without the owner's decision.

Output: test results (pass/fail per check), the proposed version and CHANGELOG line, and open issues.
