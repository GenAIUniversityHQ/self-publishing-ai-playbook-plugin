# Contributing

Thanks for improving The Self Publishing AI Playbook.

## Project Shape

This repo is a portable Claude skills package. Keep contributions focused on:

- Clearer skill instructions
- Better setup and quick-start docs
- Safer publishing and review guidance
- More useful examples
- Metadata, YAML, and plugin packaging fixes

## Public-Repo Rules

Do not add:

- API keys, tokens, credentials, or environment values
- Customer data, email lists, private messages, or personal contact details
- Links to private Gen AI University repositories
- Private connector workflows or internal system assumptions
- Platform actions that send, publish, or modify real accounts without explicit user action

If an example needs a concrete business, use a fictionalized example. The default example is a SideHustle LIVE-style comedy business game show book, but it should stay generic enough for public use.

## Skill Format

Every skill lives at:

```text
skills/[skill-name]/SKILL.md
```

Each skill must start with YAML frontmatter:

```yaml
---
name: skill-name
description: Short trigger-focused description.
---
```

Keep descriptions concise and include the phrases a user is likely to say.

## Review Checklist

Before opening a PR:

- [ ] All Markdown files are free of PII and credentials
- [ ] No private repo links are included
- [ ] JSON files pass `python3 -m json.tool`
- [ ] Every `skills/*/SKILL.md` file has `name` and `description`
- [ ] README and QUICK-START still describe the ZIP install flow accurately
