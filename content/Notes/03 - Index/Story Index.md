---
tags:
  - index
cssclasses:
  - dashboard
obsidianUIMode: preview
---
# Story Index

``` dataview
TABLE WITHOUT ID
 file.link as "Stories",
 date(file.ctime) as "Date Created"

FROM #story  AND !"05 - Extras/Templates" 

SORT file.cday desc

LIMIT 500

```
