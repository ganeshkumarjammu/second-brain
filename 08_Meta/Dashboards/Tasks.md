# Tasks

> [!tip] Change a list
> Click into a block and edit its lines.
> - Only some folders: `folder includes 03_Projects`
> - Skip a folder: `path does not include 07_Archive`
> - Date range: `happens after 2026-11-01` + `happens before 2026-11-30`
> - Group by: `group by folder` · `group by filename` (note) · `group by happens` (day) · `group by priority` · `group by tags`
> - Sort by: `sort by happens` · `sort by due` · `sort by priority` · `sort by path`
> - Only your Top 3: `tags include #focus`

## Overdue
```tasks
not done
(due before today) OR (scheduled before today)
path does not include 07_Archive
path does not include 08_Meta
path does not include Habits
description regex matches /\S/
group by folder
sort by due
```

## Today
```tasks
not done
happens today
path does not include 07_Archive
path does not include 08_Meta
path does not include Habits
description regex matches /\S/
sort by priority
```

## This week
```tasks
not done
happens this week
path does not include 07_Archive
path does not include 08_Meta
path does not include Habits
description regex matches /\S/
group by folder
sort by happens
sort by priority
```

## By project
```tasks
not done
folder includes 03_Projects/Active
description regex matches /\S/
group by filename
sort by due
```

## No date yet
```tasks
not done
no happens date
path does not include 07_Archive
path does not include 08_Meta
path does not include Habits
description regex matches /\S/
group by folder
```

## Done this week
```tasks
done this week
path does not include 08_Meta
description regex matches /\S/
group by done
```
