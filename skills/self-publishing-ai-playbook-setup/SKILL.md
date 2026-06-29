---
name: self-publishing-ai-playbook-setup
description: "Install and onboarding skill for The Self Publishing AI Playbook. Collects book details, determines where the author is right now, creates project context, and routes to the correct next publishing skill. Triggers on: 'run Self Publishing AI Playbook setup', 'set up the playbook', 'personalize the playbook', 'playbook setup', '/run-self-publishing-ai-playbook-setup', or first run when project context is missing."
---

# Self Publishing AI Playbook Setup And Onboarding

Personalize The Self Publishing AI Playbook to the user's book project, identify where they are in the publishing journey, and route them to the right next skill.

This is a public, portable setup flow. Do not ask for private credentials, API keys, customer lists, email inbox access, private connector access, or Gen AI University internal systems.

---

## What This Skill Does

Use this skill when:

- The user just installed the playbook.
- The user asks how to start.
- The user is not sure which publishing skill to run.
- The user has a book in progress and needs to resume from the right point.
- The user runs `/run-self-publishing-ai-playbook-setup`.

Think of this as the onboarding desk for an AI publishing assistant. It is not the ghostwriter. It is the intake, routing, context, and next-action layer.

---

## Phase 1: Explain The Setup And Role

Tell the user:

> "I'll set up your Self Publishing AI Playbook, figure out where you are right now, and recommend the next skill to run. This works like an AI publishing assistant: I can help you clarify, organize, draft with structure, and prepare your launch, but your stories, expertise, voice, and final decisions stay yours."

Keep the setup conversational. Do not interrogate.

---

## Phase 2: Quick Current-State Triage

Ask these first so setup can adapt instead of assuming the user is starting from zero.

1. "Where are you right now?"
   - Just an idea
   - Clear topic, no outline
   - Mind map or notes collected
   - Outline started or done
   - Draft started
   - Draft finished
   - Editing/polish
   - Pre-launch or launch week
2. "What do you want the playbook to help with first?"
   - Decide what to write
   - Organize the book
   - Write consistently
   - Finish a draft
   - Edit and polish
   - Launch and get reviews
3. "Do you already have any context you want me to use? Paste notes, outline, title, draft status, or launch date if you have it."

If they paste substantial context, summarize it before asking more questions.

---

## Phase 3: Collect Project Variables

Ask these questions one at a time or in small batches.

### About The Author

- `AUTHOR_NAME` — "What name will appear on the book?"
- `AUTHOR_EMAIL` — "What email, if any, should appear in author communications? You can skip this or use a placeholder."

### About The Book

- `BOOK_TITLE` — "Do you have a working title? If not, we'll use `[Working Title]`."
- `BOOK_TOPIC` — "What is the book about in one sentence?"
- `TARGET_READER` — "Who is the ONE reader this book is for?"
- `BOOK_GENRE` — "What type of book is this? Examples: how-to, memoir, business storytelling, personal development, framework book."

### About The Timeline

- `DAY_ONE_DATE` — Today's date.
- `LAUNCH_DATE` — "Do you have a target launch date? If not, I recommend 90 days from today."

### About The Platform

- `CONTENT_PLATFORMS` — "Where do you already publish or communicate? Examples: LinkedIn, newsletter, YouTube, podcast, blog, Instagram."
- `EMAIL_LIST_SIZE` — "Do you have an email list or launch audience? Rough size is enough."

---

## Phase 4: Classify Current Phase

Use the triage answers to choose the current phase:

| User State | Current Phase | Current Day | Recommended Next Skill |
| --- | --- | --- | --- |
| No clear reason for writing | Foundation | 1 | `book-purpose-finder` |
| Wants to write but idea unclear | Foundation | 1 | `book-idea-validator` |
| Clear topic, no content map | Foundation | 3 | `mind-map-generator` |
| Notes or mind map done, no outline | Foundation | 5 | `book-outline-architect` |
| Outline done, draft not started | Writing Sprint | 15 | `30-day-writing-challenge` |
| Draft started, needs rhythm | Writing Sprint | current estimate | `30-day-writing-challenge` |
| Draft finished, needs editing plan | Editing And Polish | 45 | `editor-hiring-assistant` |
| Edited draft, needs title/subtitle | Editing And Polish | 55 | `title-creator` |
| Preparing launch team | Pre-Launch Marketing | 65 | `launch-team-builder` |
| Needs pre-launch content | Pre-Launch Marketing | 70 | `buzz-building-strategist` |
| Launching or asking for reviews | Launch Week | 80 | `review-campaign-manager` |

If the user is between phases, choose the earliest unfinished foundation piece. Do not skip outline before writing sprint unless the user explicitly has an outline.

---

## Phase 5: Create Project Context

Return this Markdown block and tell the user to keep it in their own project notes outside the plugin folder. If they are working from an editable local copy and understand Git, they may save it as `CONTEXT.md`, which is gitignored.

```markdown
# Self Publishing AI Playbook Context

## Author

- Name: [AUTHOR_NAME]
- Email: [AUTHOR_EMAIL or skipped]

## Book

- Working title: [BOOK_TITLE]
- Topic: [BOOK_TOPIC]
- Genre: [BOOK_GENRE]
- Target reader: [TARGET_READER]

## Timeline

- Day 1: [DAY_ONE_DATE]
- Target launch date: [LAUNCH_DATE]
- Current phase: [CURRENT_PHASE]
- Current day: [CURRENT_DAY_OR_ESTIMATE]
- Recommended next skill: [RECOMMENDED_NEXT_SKILL]

## Platform

- Content platforms: [CONTENT_PLATFORMS]
- Email list size: [EMAIL_LIST_SIZE]

## Notes

- This project follows the 90-day book publishing path from The Self Publishing AI Playbook.
- Update this context whenever the title, reader, launch date, or current phase changes.
- The AI assistant should preserve the author's voice, stories, and expertise.
```

Do not run shell commands to rewrite the skill files. The skills should read the context conversationally and adapt their output to the user's current book.

---

## Phase 6: Confirm The Routing

Ask:

1. "Have you already committed to writing this book?"
2. "Do you already have a mind map or outline?"
3. "Have you started drafting?"

Then route:

- No commitment yet -> `book-purpose-finder`
- Committed but idea unclear -> `book-idea-validator`
- Idea clear but no mind map -> `mind-map-generator`
- Mind map done but no outline -> `book-outline-architect`
- Outline done -> `30-day-writing-challenge`
- Draft done -> `editor-hiring-assistant`
- Editing done -> `title-creator`
- Title ready, launch not planned -> `launch-team-builder`
- Launch team started -> `buzz-building-strategist`
- Launch imminent -> `review-campaign-manager`

---

## Phase 7: Finish Setup

Tell the user:

> "Your Self Publishing AI Playbook is set up. Based on where you are right now, I recommend `[recommended next skill]`. We can run that now, or you can say `Run published author navigator` any time to reassess your path."

## Quality Check

Before closing setup, verify:

- [ ] Author name captured or intentionally skipped
- [ ] Book topic captured
- [ ] Target reader captured
- [ ] Launch date chosen or placeholder accepted
- [ ] Current phase identified
- [ ] Current day or estimate identified
- [ ] Next skill recommended
- [ ] User understands this is an AI publishing assistant, not a replacement author
