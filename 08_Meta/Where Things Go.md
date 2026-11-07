---
type: meta
tags: [meta]
---

# 🧭 Where things go — one rule, no overlaps

> **The folder says what a note IS. The `area:` link says what it's ABOUT. Links say how it RELATES.**
> A note has exactly one home folder. It never lives in a folder because of its topic.

That's why a book about health goes in `04_Resources/Books` (it *is* a book) with `area: [[Health and Fitness]]` (it's *about* health). It shows up on the Health page automatically, and it is never copied.

---

## The order to ask in (first "yes" wins)

| # | Ask | Yes → | Folder |
|---|---|---|---|
| 1 | Did it happen at a time, with people? | **Meeting** | `01_Journal/Meetings/<year>` |
| 2 | Is it about one person? | **Person** | `06_People` |
| 3 | Is it what *someone else* said (book, article, course, video)? | **Source** | `04_Resources/<Books…>` |
| 4 | Committed, with a finish line, and more than one step? | **Project** | `03_Projects/Active` |
| 4b | …but only one step? | **Task** | today's note (or TaskNotes) |
| 5 | A new part of life you'll maintain forever? (rare!) | **Area** | `02_Areas/<Area>` |
| 6 | Your own idea, stated as one sentence? | **Permanent** | `05_Notes/Permanent` |
| 7 | An open question? | **Question** | `05_Notes/Questions` |
| — | Anything else / not sure | **Fleeting / Inbox** | `05_Notes/Fleeting` / `00_Inbox` |

The plugin asks you these questions: **Ctrl+P → "SB Autopilot: Where does this go?"**

---

## The three confusing pairs, settled

**Area vs Project**: does it end? *Health* never ends, so it's an Area. *Run a half marathon by Dec* ends, so it's a Project, with `area: [[Health and Fitness]]`.

**Area vs Resource**: are you *responsible* for it? You're responsible for your money (Area). You're only *interested* in behavioural economics (Resource, linked to that area). **Area folders hold only the area's hub note.** Everything else links to it.

**Resource vs Notes**: whose words? `04_Resources` = what *others* said (one note per book/article). `05_Notes` = what *you* think. A great idea from a book becomes a Permanent note that links back to the book note.
- `05_Notes/Literature` is only for notes on *part* of a big source (one chapter, one lecture), linked to the source note.

## Meetings
Meetings are **events**, so they're filed by date in `01_Journal/Meetings/<year>`. You never have to choose between the project folder and the person folder. The meeting links to `project`, `area` and `attendees`, and each of those pages lists its meetings automatically. Today's daily note gets a log line for it too.

## Books
`04_Resources/Books/Book - Title - Author.md`, with `status: to-read | reading | finished | abandoned`, `format`, `rating` (1–5), `area:` and `project:`. The template follows your reading: *before* (why read it) → *during* (reading log, highlights, quotes) → *after* (3 sentences, verdict, what you'll DO). The Reading dashboard picks them up, including an "Abandoned" list.

## Habits
Your habits are the **properties of your daily note** (`prayer: false`, `book_pages: 0`…). Fill them in each day. **[[08_Meta/Dashboards/Habit Tracker|🔁 Habit Tracker]]** shows them all in one table (one row per day, plus monthly totals). New habit: add the property to your daily template, then Ctrl+P → **Open / update Habit Tracker page**.

---

## Your own categories
Decision, Skill log, Mental model, Cheatsheet, Code & tech and Quote are types too, set in **Settings → SB Autopilot → Your categories**. Each has its own folder and template. You can add more (e.g. `recipe` → `04_Resources/Recipes`). Folder renames are followed automatically.

## Plugin cheat-sheet (Ctrl+P → "SB Autopilot")

**Left ribbon icons** (each can be hidden in settings): 🧠 New note · ⚡ Quick capture · ⏱ Time log

**Keyboard shortcuts** (Ctrl+Alt + letter, so they don't clash with Windows; change them in Settings → Hotkeys)

| Keys | Does |
| --- | --- |
| Ctrl+Alt+D | Open today's daily note |
| Ctrl+Alt+Q | Quick capture |
| Ctrl+Alt+S | Start an activity (time log) |
| Ctrl+Alt+E | End the running activity |
| Ctrl+Alt+L | Log a past activity, e.g. `14:00-15:30 Travelling` |

**Features:** core is always on. Pick the optional ones in Settings → SB Autopilot → Features, or Ctrl+P → **Choose features…**

**Capturing fast**
- **⚡ Quick capture**: one line, saved without leaving your note. `t` task · `i` idea · `l` log line · `n` new note · `@Name …` waiting-for · nothing = Inbox. Shift+Enter saves and keeps the box open.

**⏱ Time log** (lines go under 📓 Log in today's note)
- `l Going for the bath` → `- 20:01 Going for the bath`: just the time, for things that happen in a moment.
- `s Book reading` → `- 09:15 ▶ Book reading`: starts an activity. The status bar shows it running.
- `e` → `- 09:15 → 10:05 (50m) Book reading`: ends it. With several running, type `e book`, or pick it in the ⏱ menu. Works past midnight.
- `l 14:00-15:30 Travelling` → `- 14:00 → 15:30 (1h 30m) Travelling`: something you forgot to start.
- You can also type `- 18:00-18:40 Walk` straight into the Log; ⏱ menu → **Update today's time summary** adds the duration.
- The **⏱ Time spent** section after the Log is a table with one row per activity: sessions and total time for the day, plus what's still running. Each session's start → end stays on its Log line. Use the same name each time (e.g. always `Book reading`) so sessions add up. The section is rewritten each time, so don't type in it.
- ⏱ ribbon icon / status bar → menu: Start · Stop · Log a past span · Update summary.

**Creating**
- **Ctrl+N**: the "What is this new note?" dialog opens. Pick the type and title, and it's filed with its template. Esc keeps a plain Inbox note.
- **New note (auto-filed)** / 🧠 ribbon icon: same dialog. If a project is open, it's pre-selected.
- **New meeting / project / book**: shortcuts
- **Where does this go?**: guided yes/no questions
- **Edit note template…**: opens the template a type uses (your `T - …` files are used automatically)

**Moving (automatic)**
- Change a note's `type:` or a project's `status:` and it moves home within 2 s, with **Undo**. `status: done` archives a project.
- Clicking a missing journal link like `[[2026-11-08]]` creates it from your daily template, inside `01_Journal/Daily`.
- **File this note**: move the open note now.

**Projects & links**
- **Link this note to a project**: sets `project: [[…]]` and copies the project's area.

**Tasks** (plain checkboxes: they stay in the note where you wrote them)
- A task belongs to a project if it's in the project note, has `[[Project]]` on the line, or sits in a note with `project:` (e.g. a meeting's action items).
- **Add task**: goes into the project, or under `## 📋 Other tasks` in today's note.
- Review checklists (weekly "Clear the decks"), a project's **Definition of done**, and empty template boxes are *not* tasks.
- **Carry-over**: each morning, unfinished tasks from the last 7 daily notes move into today (`↪ from [[2026-11-06]]`). The old line becomes `[>]`. Undo is offered.

**Reviewing**
- **Review & tidy vault**: weekly check of the Inbox, misfiled notes, overdue projects, projects with no next action, areas that don't link, sync duplicates and lonely notes
- **Fix my templates**: shows every change first, then backs up and fixes: dates from the note's name, the area table built from your areas, no empty `[[ ]]` links
- **Open this day's / week's / month's / year's note**: Ctrl+P → **SB Autopilot: Open this day's note** opens (or creates) today's daily note. Shortcut: **Ctrl+Alt+D**.

Related: [[START-HERE]] · [[08_Meta/FAQ|FAQ]]
