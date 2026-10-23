# Changelog

## 1.0.3 (2026-10-23)
- Search keywords: 34 to 40 (added PluginScaffold, PublisherTerms, SubmitForm, ReleaseCheck, LocalPluginInstall, PluginReview), per Rob's keyword rules.
- Local tests re-run and passed. Not tested in-app. Not submitted to the marketplace.

## 1.0.2 (2026-10-21)
- Added `tests/check_frontmatter.py`: a strict YAML front-matter check (PyYAML `safe_load`) for every SKILL.md and rules .mdc file, plus a plugin.json JSON check. Run `python3 tests/check_frontmatter.py` from the repo root; it catches the unquoted-colon bug fixed in PluginPulse 1.0.2.
- No behavior changes to skills or rules.

## 1.0.1 (2026-10-20)
- Rule description now states InPlug Plugin's own scope (it wrongly said Creative Switchboard); pillars text unchanged.
- build-a-plugin: warns that YAML values containing ": " must be quoted (bug found while scaffolding hello-notes in the host test).
- build-a-plugin: documents the local install routes without marketplace approval (Cursor local folder; Grok Build CLI, marked UNVERIFIED for this manifest format) and that Grok Bot has none documented.
- README: project status with the host-AI test results and the honest limit that no in-app Cursor or Grok Bot load has been done yet.

## 1.0.0 (2026-10-20)
- First release: marketplace-guide, build-a-plugin and improve-a-plugin skills, pillars rule, worked example, logo, title/description/limits in 23 languages (machine-made, not native-reviewed).
