---
{"dg-publish":true,"permalink":"/home/","noteIcon":"","created":"2026-11-01T01:36:58.227-07:00","updated":"2026-11-17T04:11:52.370-08:00","ctime":"2026-11-01T01:36:58.227-07:00","mtime":"2026-11-17T04:11:52.370-08:00","dg-note-properties":{"up":["[[50 - Outputs/Taylor Scott's Digital Garden]]"],"type":["original"],"growth":"evergreen"}}
---

This is your **launchpad**. Let's go.

>[!idea]- Atlas
> *Your brain, the final frontier.* 
> - If you're inspired, go to [[60 - Utilities/65 - Maps/Add\|Add]], [[60 - Utilities/65 - Maps/Relate\|Relate]], or [[60 - Utilities/65 - Maps/Communicate\|Communicate]].
>![mckie-ship-and-sea-mid-narrow-.jpg\|400](/img/user/60%20-%20Utilities/61%20-%20Assets/mckie-ship-and-sea-mid-narrow-.jpg)
> - To dive into your knowledge, try [[60 - Utilities/65 - Maps/Library\|Library]] | [[60 - Utilities/65 - Maps/People Map\|People Map]] | [[Sources Map\|Sources Map]].
> - To start your mind's engine, go into your [[10 - North Star/My ideas\|Ideas Map]] or [[60 - Utilities/65 - Maps/Concepts Map\|Concepts Map]].
> - For grounding in all this theory, [[60 - Utilities/65 - Maps/Life Map\|Life Map]]. For system rules, [[60 - Utilities/65 - Maps/Meta Map\|Meta Map]].

>[!question]- Calendar
> *Orient yourself.* 
> - To journal or capture a quick spark, open the command pallette with `Ctrl+P` and select `QuickAdd: Daily note log`.
> - To focus your day, open the command pallette with `Ctrl+P` and select `Daily note: Open today's daily note`.
> ![robert-mccall-space-ship-launch-narrower.png\|400](/img/user/60%20-%20Utilities/61%20-%20Assets/robert-mccall-space-ship-launch-narrower.png)
> - To capture specific types of things, go to [[60 - Utilities/65 - Maps/Logs\|Logs]].
> - To broadly reflect, go to [[60 - Utilities/65 - Maps/Plan and Review\|Plan and Review]].

>[!example]- Projects
> *Get shit done.* 
> - For a concentrated view, go to [[60 - Utilities/65 - Maps/Projects\|Projects]].
> >[!tip] On
> > 
```base
filters:
  and:
    - file.folder == "40 - Projects"
    - '!note["project status"].isEmpty()'
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
        - note["project status"] == "on"
    order:
      - file.name
      - file.ctime

```
 
> - Use this to keep priorities in order and adjust as needed.
> >[!warning]- Sleeping
> > 
```base
filters:
  and:
    - file.folder == "40 - Projects"
    - '!note["project status"].isEmpty()'
properties:
  file.name:
    displayName: Name
  file.ctime:
    displayName: Created
views:
  - type: table
    name: Simmering
    filters:
      or:
        - note["project status"] == "hold"
        - note["project status"] == "sleeping"
    groupBy:
      property: project status
      direction: ASC
    groupOrder:
      - on
      - hold
      - sleeping
      - done
    order:
      - file.name
      - file.ctime
    sort: []
    columnSize:
      file.name: 364

```
 
>
>![robert-mccall-black-hole-concept-art copy.jpg\|400](/img/user/60%20-%20Utilities/61%20-%20Assets/robert-mccall-black-hole-concept-art%20copy.jpg)

---

> *based on the [ideaverse home](https://blog.linkingyourthinking.com/home).* 
