---
type: weekly
week: <% tp.date.now("gggg-[W]ww") %>
tags: [journal/weekly]
---

# Week <% tp.date.now("ww, gggg") %>

← [[<% tp.date.now("gggg-[W]ww", -7) %>]] | [[<% tp.date.now("YYYY-MM") %>|Month]] | [[<% tp.date.now("gggg-[W]ww", 7) %>]] →

## ✅ Clear the decks
- [ ] `00_Inbox` emptied to zero
- [ ] Fleeting notes promoted or deleted
- [ ] All Active projects have a defined next action
- [ ] Calendar for next week reviewed
- [ ] Desktop / downloads / phone photos cleared

## 🏆 Wins this week
-

## ❌ Misses — and the actual cause
| What slipped | Real reason (not "no time") |
|---|---|
|  |  |

## 📚 What I learned
-

## 🔁 From my daily notes this week
### Lessons & things to remember
```dataview
TABLE WITHOUT ID file.link AS "Day", lesson AS "Lesson", remember AS "Remember"
FROM "01_Journal/Daily"
WHERE week = this.week AND (lesson OR remember)
SORT file.name ASC
```

### Friction, lost equanimity & problems solved
```dataview
TABLE WITHOUT ID meta(L.section).subpath AS "Section", L.text AS "What", L.children.text AS "Details", file.link AS "Day"
FROM "01_Journal/Daily"
WHERE week = this.week
FLATTEN file.lists AS L
WHERE !L.parent AND regexmatch(".*: *[^ ].*", L.text) AND (contains(meta(L.section).subpath, "Blockers") OR contains(meta(L.section).subpath, "Lost equanimity") OR contains(meta(L.section).subpath, "Problems solved"))
SORT meta(L.section).subpath ASC, file.name ASC
```

## 🔗 Notes created this week
```dataview
LIST
FROM "05_Notes"
WHERE file.cday >= date(today) - dur(7 days)
SORT file.cday DESC
```

## 📊 Area check-in
Rate 1–5. Anything at 2 or below gets an action next week.

| Area | Score | Note |
|---|---|---|
| Health & Fitness |  |  |
| Mind & Learning |  |  |
| Career & Work |  |  |
| Money & Finance |  |  |
| Relationships |  |  |
| Skills & Craft |  |  |
| Systems & Productivity |  |  |
| Creativity & Output |  |  |
| Philosophy & Self |  |  |
| Home & Environment |  |  |

## 🎯 Next week
**The one thing that would make next week a success:**

**Top 3:**
- [ ]
- [ ]
- [ ]

**One experiment to run:**
