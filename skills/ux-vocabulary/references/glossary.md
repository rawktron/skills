# UX Vocabulary Glossary

~40 words. Each means exactly one thing. Use them in plain English when you
need precision. Everything else stays conversational.

---

## How does the user get there?

These describe what the user SEES when one view becomes another.

| Word | Means exactly |
|------|---------------|
| **morph** | A reshapes into B. The source element becomes the destination. A card morphs into a page -- the card IS the page now. |
| **slide** | B enters from an edge. A stays where it is, possibly dimmed or partially hidden. Direction: slide-left, slide-right, slide-up, slide-down. |
| **push** | B enters from an edge and A exits the opposite edge. The whole canvas moves. |
| **overlay** | B appears floating above A. A dims but remains underneath. Dismissing B reveals A unchanged. |
| **replace** | Instant swap. No animation. A is gone, B is there. |
| **drill** | Navigate deeper into a hierarchy. Implies a back path exists. |
| **surface** | The reverse of drill. Come back up. |

---

## Where are things?

These describe the spatial structure of a screen. Just say where things are
relative to each other using these words.

| Word | Means exactly |
|------|---------------|
| **beside** | Two things, side by side. Left and right. "Tasks beside preview." |
| **stacked** | Two things, top and bottom. "Tasks stacked above sessions." |
| **across** | Three or more things, horizontal. "Nav, list, and detail across the screen." |
| **down** | Three or more things, vertical. "Header, content, and footer down the page." |
| **rail** | A thin fixed strip, usually for navigation. Doesn't scroll with content. |
| **main** | The primary workspace. The thing the user is here to look at. |
| **stage** | A large focal area. One thing at a time gets the user's full attention here. |
| **drawer** | A panel that slides in from an edge, overlaying content. Temporary -- open it, use it, close it. |
| **tray** | Like a drawer but from the bottom. Usually for actions or secondary input. |
| **bar** | A horizontal strip. Top-bar, bottom-bar. For status, actions, or context. |
| **float** | An element positioned near something else, not in the normal flow. "Float near cursor", "float near selection". |

---

## What is this thing?

These describe the shape of content, not what it looks like.

| Word | Means exactly |
|------|---------------|
| **list** | Vertical sequence of items. Ordered. One column. |
| **grid** | Items in a multi-column layout. "Grid(3)" = three columns. |
| **group** | Items that share a label or header. A cluster. |
| **item** | One thing in a list or grid. A card, a row, a tile -- you decide what it looks like. |
| **slot** | A named piece inside something. An item might have slots: title, meta, status, actions. Define these once, refer to them later. |

---

## What can the user do with it?

These are behaviors. Attach them to things. "A selectable list." "Editable title slot."

| Word | Means exactly |
|------|---------------|
| **selectable** | User picks one from the set. Picking a new one deselects the old. Radio-button logic. |
| **multi-select** | User toggles items on/off independently. Checkbox logic. |
| **expandable** | Activating it reveals hidden content inside it. Collapsing hides it again. |
| **editable** | The content becomes an input when activated. Looks like content until you interact. |
| **draggable** | User can reorder it within its parent by dragging. |
| **dismissable** | User can remove it. It goes away. |
| **focusable** | User can make this the active/attended thing. Implies other things become secondary. |

---

## How do things relate to each other?

These describe how interaction in one area affects another.

| Word | Means exactly |
|------|---------------|
| **feeds** | Selection in A populates/filters B. Directional. "Tasks feeds sessions" means picking a task constrains what sessions you see. The fed list updates immediately. |
| **mirrors** | A and B show the same thing from different angles. Changing in one reflects in the other. |
| **independent** | A and B have nothing to do with each other. Stating this prevents assumptions. |

---

## What happens to the space?

These describe how the layout rearranges in response to interaction.

| Word | Means exactly |
|------|---------------|
| **grow** | Expand to fill a larger region. "Sidebar item grows into main." It gets bigger, physically, taking more screen space. |
| **shrink** | The reverse of grow. Contract back to original size. |
| **collapse** | Minimize to a sliver, a handle, or an icon. Still present but taking almost no space. |
| **yield** | Make room for a sibling that's growing. Passively get smaller. |
| **fill** | Take all available space in your container. |

---

## How does it appear/disappear?

These describe conditional visibility -- when things show up and when they leave.

| Word | Means exactly |
|------|---------------|
| **pinned** | Always visible. Never hides. |
| **on-hover** | Visible when the user hovers over a related element. |
| **on-select** | Visible when a related item is selected. |
| **on-focus** | Visible when the user is focused on / attending to a related area. |
| **timed** | Appears, then disappears after N seconds. "Timed(5s)." |

---

## How does it load?

| Word | Means exactly |
|------|---------------|
| **skeleton** | Show the shape of the content as a placeholder while loading. Grey boxes. |
| **stream** | Content appears incrementally as it becomes available. |
| **eager** | Fetch before the user needs it. Pre-load. No waiting. |
| **lazy** | Don't fetch until the user actually goes there. |

---

## How does it handle destructive actions?

| Word | Means exactly |
|------|---------------|
| **mark-and-undo** | Flag the item visually. Provide an undo window (specify seconds). If they don't undo, execute. No confirmation dialog. |
| **confirm** | Show a modal. Make them explicitly say yes. Blocking. |
| **quiet** | Just do it. No ceremony. For low-stakes things. |

---

## What's the overall vibe?

These set global tone. Use at the top of a description.

| Word | Means exactly |
|------|---------------|
| **snappy** | Transitions under 200ms. Everything responds instantly. |
| **patient** | Slower, deliberate transitions. Eased. Things breathe. |
| **physical** | Things move spatially -- slide, scale, fold. Not opacity fades. |
| **dense** | Lots of information, compact spacing. Power-user feel. |
| **airy** | Generous whitespace. Calm. One thing at a time. |

---

## Combining Words

These words compose naturally in English:

> "Tasks and sessions stacked on the left, preview stage beside them on
> the right. Both lists selectable. Tasks feeds sessions. On-focus, the
> focused list grows and the other yields. Feels dense and snappy."

Every word with a definition above is precise. Everything else ("on the left",
"on the right", "both", "the other") is plain English interpreted normally.

---

## Full Example: Agent Harness

> Tasks and sessions stacked on the left. Stage beside them, pinned width.
> Tasks is a selectable list with "Ad-Hoc" pinned to the top. Tasks feeds
> sessions. Sessions is a selectable list.
>
> On-focus (TAB between lists), the focused list grows and the sibling yields.
> Stage doesn't move. Stage previews whatever's selected in the focused list --
> task details or session worktree status.
>
> ENTER on a task resumes its session if one exists, starts a new one otherwise.
> ENTER on a session reattaches. Sessions are tmux windows -- this app is just
> the control plane. Snappy TUI.

---

## What's NOT In This Glossary

- **Colors, fonts, spacing** -- say "use shadcn" or "make it brutalist" or describe the aesthetic separately
- **Specific components** -- I figure out if it's a dropdown vs. combobox vs. popover. You tell me the behavior.
- **Data/state** -- use curly braces for bindings if you want: {user.name}, {project.status}. Or just say "show the user's name."
- **Exact pixel values** -- unless you care, I pick. If you care, just say the number.
