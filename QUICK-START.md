# The Self Publishing AI Playbook Quick Start

Get the full skill package running in about two minutes.

## 1. Download The Package

1. Open the GitHub repository.
2. Click **Code**.
3. Click **Download ZIP**.
4. Unzip the file.
5. Put the folder somewhere easy to find, such as `Documents/Self Publishing AI Playbook/`.

## 2. Install In Claude

Use whichever Claude surface you work in:

| Tool | Install Path |
| --- | --- |
| Claude Code | Settings -> Plugins -> Install from folder |
| Claude Cowork | Settings -> Plugins -> Install from folder |

Choose the unzipped folder. The plugin metadata lives in `.claude-plugin/`, and the skills live in `skills/`.

## 3. Run Setup

Say this to Claude:

```text
Run Self Publishing AI Playbook setup
```

Or use:

```text
/run-self-publishing-ai-playbook-setup
```

The setup wizard collects:

- Author name
- Working book title
- Book topic
- Target reader
- Book genre
- Launch date
- Content platforms
- Email list size

If you do not know an answer yet, use a placeholder. The navigator will help refine it later.

## 4. Start The 90-Day Journey

Say:

```text
Run published author navigator
```

The navigator asks where you are, assigns your current phase, and routes you to the next skill.

## Skill Map

| Phase | Use These Skills |
| --- | --- |
| Foundation | `book-purpose-finder`, `limiting-belief-dismantler`, `book-idea-validator`, `mind-map-generator`, `book-outline-architect` |
| Writing | `30-day-writing-challenge` |
| Editing | `editor-hiring-assistant`, `title-creator` |
| Pre-launch | `launch-team-builder`, `buzz-building-strategist` |
| Launch | `review-campaign-manager` |

## Example

If you need a sample project while learning the flow, use:

```text
Author: Alex Morgan
Book title: The Founder Game Night
Topic: How a comedy business game show can help founders build community, creativity, and courage.
Target reader: Startup founders who want more playful, memorable ways to connect with their market.
Genre: Business storytelling / how-to
Launch date: 90 days from today
```

This example is inspired by the SideHustle LIVE concept, but it is fictionalized so the package stays clean and portable.

## What To Expect

You do not need private Gen AI University systems, private connectors, API keys, or customer data. Everything in this package is plain Markdown skill content.

The package is designed to work as:

- A Claude Code plugin
- A Claude Cowork plugin
- A readable skill bundle for Codex-style agents that can follow Markdown instructions
