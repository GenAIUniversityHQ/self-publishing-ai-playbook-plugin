# The Self Publishing AI Playbook

AI skills for publishing your book in 90 days, inspired by Chandler Bolt's bestselling book "Published".

Built by [Gen AI University](https://genaiuniversity.com).

---

## What This Is

The Self Publishing AI Playbook is a ZIP-installable skills package for Claude Code, Claude Cowork, and Markdown-friendly coding agents such as Codex. It gives you an AI publishing assistant for the full book journey:

- Find the right book idea
- Turn the idea into a clear outline
- Write the draft in a focused 30-day sprint
- Prepare for editing, title, and cover decisions
- Build a launch team
- Run a review campaign

No private connectors, API keys, paid companion repos, or Gen AI University internal systems are required.

## Philosophy

Most people do not fail to publish because they lack ideas. They fail because the path is fuzzy, the milestones are too loose, and the writing process turns into an identity test.

This playbook turns publishing into a sequence of decisions and reps. Your AI becomes the coach, checklist, and accountability partner for each stage of the 90-day journey.

It is not a push-button ghostwriter. It helps you clarify the idea, organize the material, draft with structure, prepare for editing, and build the launch system. The author's voice, expertise, stories, and final decisions still come from the author.

## Quick Start

See [QUICK-START.md](QUICK-START.md) for the two-minute install guide.

Short version:

1. Download this repository as a ZIP.
2. Unzip it somewhere memorable, such as `Documents/Self Publishing AI Playbook/`.
3. In Claude Code or Claude Cowork, install it from the folder.
4. Say: `Run Self Publishing AI Playbook setup`, or use `/run-self-publishing-ai-playbook-setup`.
5. Then say: `Run published author navigator`.

You can also paste this starter prompt into any Markdown-capable AI workspace:

```text
Read skills/self-publishing-ai-playbook-setup/SKILL.md and run the complete Self Publishing AI Playbook setup process. Ask where I am in my book project, collect the needed project context, create my project context block, and recommend the next skill to run.
```

## Skill Directory

### Setup And Orchestration

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `self-publishing-ai-playbook-setup` | Installs the playbook into your current book context and routes you to the right next skill | "run Self Publishing AI Playbook setup", "playbook setup", `/run-self-publishing-ai-playbook-setup` |
| `published-author-navigator` | Assesses your current phase and routes you to the next skill | "start my book publishing journey", "where am I in my book project" |

### Phase 1: Foundation

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `book-purpose-finder` | Finds the deeper reason this book is worth writing | "find my book purpose", "why should I write a book" |
| `limiting-belief-dismantler` | Converts common author blocks into action pledges | "I don't think I can write a book", "I'm not a writer" |
| `book-idea-validator` | Narrows many ideas into the book most likely to get finished | "what should my book be about", "help me find my book idea" |
| `mind-map-generator` | Runs the 15-minute brain-dump method | "create a mind map for my book", "brain dump my book ideas" |
| `book-outline-architect` | Converts raw ideas into a chapter outline | "create my book outline", "organize my book chapters" |

### Phase 2: Writing Sprint

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `30-day-writing-challenge` | Runs the daily writing protocol and checkpoints | "start my 30-day writing challenge", "writing accountability" |

### Phase 3: Editing And Polish

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `editor-hiring-assistant` | Helps scope editing needs and evaluate editors | "help me find an editor", "editing budget" |
| `title-creator` | Creates title and subtitle options after the manuscript takes shape | "help me create my book title", "title and subtitle" |

### Phase 4: Pre-Launch Marketing

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `launch-team-builder` | Builds a simple, committed launch team | "build my launch team", "how do I get book reviews" |
| `buzz-building-strategist` | Turns the author journey into pre-launch content | "build buzz for my book", "pre-launch content strategy" |

### Phase 5: Launch Week

| Skill | Purpose | Trigger Phrases |
| --- | --- | --- |
| `review-campaign-manager` | Drafts review requests, tracking, and follow-up rhythm | "get reviews for my book", "launch day review strategy" |

## How To Use The Skills

After installation, ask for the skill by name in natural language:

```text
Run Self Publishing AI Playbook setup
Run published author navigator
Run book outline architect
Run the 30-day writing challenge
```

The setup skill collects your current book context. The navigator then decides which specialist skill should run next based on where you are in the 90-day path.

You can also start setup with the slash command:

```text
/run-self-publishing-ai-playbook-setup
```

## The 90-Day Path

```text
WEEKS 1-2   Foundation: purpose, mindset, idea, mind map, outline
WEEKS 3-6   Writing sprint: 30 days of focused drafting
WEEKS 7-9   Editing and polish: read-through, editor, title, cover
WEEKS 10-11 Pre-launch: launch team and buzz building
WEEKS 12-13 Launch: release, review campaign, momentum
```

## Example Project

Use any nonfiction or story-driven book idea. For examples in the skills, we use a fictionalized SideHustle LIVE-style project: a book about turning a comedy business game show into a community-building engine for founders.

That example is only a sample. Replace it with your own topic, reader, and launch goal during setup.

## What Is Not Included

This public package intentionally does not include:

- Gen AI University private repositories
- Private connector workflows or internal automations
- Customer data, personal data, or email lists
- API keys, credentials, or environment files
- Done-for-you publishing services

It is a portable skill package. You bring the book idea and the audience. The skills bring the structure.

## Claude, Codex, And Other AI IDEs

This package is Claude-native today because it includes `.claude-plugin/` metadata and follows Claude's `skills/*/SKILL.md` format.

The core playbook is portable because each skill is plain Markdown. Codex and other AI IDEs can read and run the skills if you point the agent at the repo or copy the relevant `SKILL.md` files into that environment.

For a first-class Codex or multi-IDE release, add a separate adapter layer instead of changing the Claude package:

- `AGENTS.md` with routing instructions for Codex-style agents
- A `manifest.json` or `index.md` that lists each skill, purpose, and trigger
- A short install guide for copying the `skills/` folder into the target IDE's skill or instruction system
- Optional starter prompt: "Read `skills/self-publishing-ai-playbook-setup/SKILL.md` and run the setup process."

## License And Support

This project is released under the MIT License. See [LICENSE](LICENSE).

This repository is distributed as a standalone Gen AI University release. You may use, copy, modify, and adapt it under the MIT License.

Gen AI University maintains this canonical package. Use GitHub Issues for install problems, packaging problems, broken links, or security concerns. For support expectations, see [SUPPORT.md](SUPPORT.md), [SECURITY.md](SECURITY.md), and [NOTICE.md](NOTICE.md).

## Attribution

This project is inspired by concepts from Chandler Bolt's *Published: The Proven Path From Blank Page to 10,000 Copies Sold*. We encourage authors to read the book:

- [Published on Amazon](https://www.amazon.com/dp/1539412334)

Gen AI University is an affiliate partner of [Self Publishing School](https://selfpublishingschool.com/), which we refer clients to for world-class publishing guidance, coaching, accountability, and support. This package is an independent Gen AI University release, not an official Self Publishing School product.

The Self Publishing AI Playbook is an experimental Gen AI University project designed to help authors use AI responsibly during the planning, drafting, editing, and launch process. Gen AI University also architects custom [selfpublishing.ai](https://selfpublishing.ai) systems for first-draft and manuscript production workflows. AI can accelerate the work, but human guidance, judgment, voice, accountability, and care still matter. See [NOTICE.md](NOTICE.md).

## Learn More

For workshops, examples, and the broader Gen AI University operating system, visit [genaiuniversity.com](https://genaiuniversity.com).
