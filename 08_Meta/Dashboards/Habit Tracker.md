---
type: dashboard
tags: [meta]
---

# 🔁 Habit Tracker

Your habits are the **properties of your daily notes**. Fill them in each day's note; this page only *shows* them, all in one place.

<!-- habit-tracker:start (made by SB Autopilot; regenerate with “Update Habit Tracker page”) -->
## 📅 Last 31 days
```dataview
TABLE WITHOUT ID file.link AS "Day", mood AS "Mood", energy AS "Energy"
FROM "01_Journal/Daily"
WHERE file.day
SORT file.day DESC
LIMIT 31
```
<!-- habit-tracker:end -->
