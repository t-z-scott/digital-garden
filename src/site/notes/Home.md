---
{"dg-publish":true,"permalink":"/home/","noteIcon":"","created":"2026-11-01T01:36:58.227-07:00","updated":"2026-11-07T03:36:23.134-08:00","ctime":"2026-11-01T01:36:58.227-07:00","mtime":"2026-11-07T03:36:23.134-08:00","dg-note-properties":{}}
---

up: [[50 - Outputs/Taylor Scott's Digital Garden\|Taylor Scott's Digital Garden]] 

#type/original 

This is your **launchpad**. Let's go.

>[!idea]- Atlas
> *Your brain, the final frontier.* 
> - If you're inspired, go to [[60 - Utilities/65 - Maps/Add\|Add]], [[60 - Utilities/65 - Maps/Relate\|Relate]], or [[60 - Utilities/65 - Maps/Communicate\|Communicate]].
> - To dive into your knowledge, try [[60 - Utilities/65 - Maps/Library\|Library]] | [[People Map\|People Map]] | [[Sources Map\|Sources Map]].
> - To start your mind's engine, go into your [[50 - Outputs/My ideas\|Ideas Map]] or [[60 - Utilities/65 - Maps/Concepts Map\|Concepts Map]].
> - For grounding in all this theory, [[60 - Utilities/65 - Maps/Life Map\|Life Map]]. For system rules, [[60 - Utilities/65 - Maps/Meta Map\|Meta Map]].

>[!question]- Calendar
> *Orient yourself.* 
> - To journal or capture a quick spark, open the command pallette with `Ctrl+P` and select `QuickAdd: Daily note log`.
> - To focus your day, open the command pallette with `Ctrl+P` and select `Daily note: Open today's daily note`.
> - To capture specific types of things, go to [[60 - Utilities/65 - Maps/Logs\|Logs]].
> - To broadly reflect, go to [[60 - Utilities/65 - Maps/Plan and Review\|Plan and Review]].

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

