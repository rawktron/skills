# UXL Vocabulary

A ~45-word shared vocabulary for describing user interfaces in plain English -- precisely.

## The Problem

Describing UX to an AI (or anyone) in natural language is frustrating. "Put these side by side" tells you nothing about proportions. "The user can edit this" could mean six different things. You end up either writing a paragraph to describe one interaction, or giving up and writing code.

## The Solution

UXL is a glossary, not a language. ~45 words with exact, unambiguous definitions. You write in normal conversational English and reach for these words when precision matters. Everything else stays natural.

**Before:** "I want the sidebar to like, get smaller when you click on something in the main area, and the main area should take up more space"

**After:** "On-select, the rail collapses and main fills."

Same intent. One sentence. Zero ambiguity.

## Quick Example

> Tasks and sessions stacked on the left. Stage beside them, pinned width.
> Tasks feeds sessions. Both selectable. On-focus, the focused list grows,
> sibling yields. Snappy TUI.

That's a complete spec for a three-pane master-detail app with filtered navigation, focus-driven layout animation, and interaction behavior. Six sentences.

## The Vocabulary

Words are organized by the question you're trying to answer:

- **Transitions** -- how does the user get there? (morph, slide, push, overlay, replace, drill, surface)
- **Layout** -- where are things? (beside, stacked, across, down, rail, main, stage, drawer, tray, bar, float)
- **Containers** -- what is this thing? (list, grid, group, item, slot)
- **Behaviors** -- what can the user do? (selectable, multi-select, expandable, editable, draggable, dismissable, focusable)
- **Relationships** -- how do things affect each other? (feeds, mirrors, independent)
- **Spatial reactions** -- how does the space rearrange? (grow, shrink, collapse, yield, fill)
- **Visibility** -- when do things appear? (pinned, on-hover, on-select, on-focus, timed)
- **Loading** -- how does it load? (skeleton, stream, eager, lazy)
- **Destructive actions** -- how are dangerous things handled? (mark-and-undo, confirm, quiet)
- **Vibe** -- what's the overall feel? (snappy, patient, physical, dense, airy)

Full definitions are in [`references/glossary.md`](references/glossary.md).

## Usage

Install as a Claude skill. Then just talk normally and use UXL words when you need precision. Claude will interpret them as exact specs, not suggestions.

The glossary is deliberately small (~45 words). If you need a word that isn't there, define it in conversation and it becomes part of the working vocabulary for that session.

## License

MIT
