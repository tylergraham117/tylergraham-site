---
tags:
  - index
cssclasses:
  - dashboard
obsidianUIMode: preview
---
# Personal YouTube Index 🎥



``` dataview
TABLE WITHOUT ID
 file.link as "Active Videos",
 (date(today) - file.cday).day as "Days alive"

FROM #effort/video 

WHERE active = true

SORT file.cday desc

LIMIT 500
```





``` dataview
TABLE WITHOUT ID
 file.link as "Video Ideas 💡",
 (date(today) - file.cday).day as "Days alive"

FROM #effort/video AND !"05 - Extras/Templates" 

WHERE !posted = true

SORT file.cday desc

LIMIT 500
```








``` dataview
TABLE WITHOUT ID
 file.link as "Series Ideas 💡",
 (date(today) - file.cday).day as "Days alive"

FROM #effort/video/series and -"Template, Video"

SORT file.cday asc

LIMIT 20
```












