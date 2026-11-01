---
{"dg-publish":true,"permalink":"/home/","noteIcon":"","created":"2026-11-01T01:36:58.227-07:00","updated":"2026-11-01T12:53:04.622-08:00","ctime":"2026-11-01T01:36:58.227-07:00","mtime":"2026-11-01T12:53:04.622-08:00","dg-note-properties":{}}
---

up: [[40 - Outputs/Taylor Scott's Digital Garden\|Taylor Scott's Digital Garden]] 

#type/original 

This is your **launchpad**. Let's go.

>[!idea]- Atlas
> *Your brain, the final frontier.* 
> - If you're inspired, go to [[Add\|Add]], [[Relate\|Relate]], or [[Communicate\|Communicate]].
> - To dive into your knowledge, try [[Library\|Library]] | [[People Map\|People Map]] | [[Source Map\|Source Map]].
> - To start your mind's engine, go into your [[Ideas Map\|Ideas Map]].
> - For grounding in all this theory, [[Life Map\|Life Map]]. For system rules, [[Meta Map\|Meta Map]].

>[!question]- Calendar
> *Orient yourself.* 
> - To journal or capture a quick spark, open the command pallette with `Ctrl+P` and select `QuickAdd: Daily note log`.
> - To focus your day, open the command pallette with `Ctrl+P` and select `Daily note: Open today's daily note`.
> - To capture specific types of things, go to [[Logs\|Logs]].
> - To broadly reflect, go to [[Plan and Review\|Plan and Review]].

>[!example]- Projects
> *Get shit done.* 
> - For a concentrated view, go to [[Projects kanban.base|Projects]].
> >[!tip] On
> > 
```base
properties:
  file.name:
    displayName: Name
  file.ctime:
    displayName: Created
views:
  - type: table
    name: In Progress
    filters:
      and:
        - file.folder == "50 - Projects"
        - note["project status"] == "on"
    order:
      - file.name
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC
  - type: cards
    name: View
    filters:
      and:
        - file.folder == "50 - Projects"
        - note["project status"] == "on"
    groupBy:
      property: dg-publish
      direction: ASC
    order:
      - file.name
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC
    cardSize: 290

```
 
> - Use this to keep priorities in order and adjust as needed.
> >[!warning]- Sleeping
> > 
```base
properties:
  file.name:
    displayName: Name
  file.ctime:
    displayName: Created
views:
  - type: table
    name: On Hold
    filters:
      and:
        - file.folder == "50 - Projects"
        - note["project status"] == "hold"
    groupBy:
      property: dg-publish
      direction: ASC
    order:
      - file.name
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC
  - type: cards
    name: View
    filters:
      and:
        - file.folder == "50 - Projects"
        - file.tags.contains("status/project/hold")
    groupBy:
      property: dg-publish
      direction: ASC
    order:
      - file.name
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC
    cardSize: 220

```
 

---

> *based on the [ideaverse home](https://blog.linkingyourthinking.com/home).* 

