---
date: <% tp.file.creation_date("YYYY-MM-DD") %>
tags:
  - log/meeting
publish: false
---
# <% tp.file.title %>
'[[<% tp.file.creation_date("YYYY-MM-DD") %>]]'

<% await tp.file.rename(tp.file.creation_date("YYYY-MM-DD ") + tp.file.title) %>


## Meeting Sheet
### Meeting Subject:

### Meeting Agenda:

### Duration:

### Critical Attendees:

### Additional Attendees:

### Context of Meeting:

### If decision based:
**What is the decision?:** 
**Who needs to make it?:** 
**Is it a one-way door?:** 
**If yes, why?** 


## Notepad
- 



## Action items
- 




