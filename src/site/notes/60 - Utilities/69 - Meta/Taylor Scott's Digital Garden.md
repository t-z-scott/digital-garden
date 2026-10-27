---
{"dg-publish":true,"permalink":"/60-utilities/69-meta/taylor-scott-s-digital-garden/","tags":["type/original","gardenEntry"],"noteIcon":"","created":"2026-10-27T06:58:37.812-07:00","updated":"2026-10-27T10:26:38.685-07:00","ctime":"2026-10-27T06:58:37.812-07:00","mtime":"2026-10-27T10:26:38.685-07:00","dg-note-properties":{"tags":["type/original","gardenEntry"]}}
---

Hi y'all, welcome to my [[digital garden\|digital garden]]! I'm [[Intro to Taylor 101\|Taylor]].

This is a section of my personal [Obsidian](https://obsidian.md) vault that I'm sharing to learn in public.

>[!warning] Some notes will not be published but may have a dead link on a published note.

## What you can find here
- Half-formed thoughts and opinions based on resources
- Notes sorted by type
- Maps (notes that structure links to other notes)
- Lists! (Like this one) (I love making lists)

## What I've been thinking about

```base
properties:
  file.name:
    displayName: Name
  note.dg-publish:
    displayName: Published?
  file.mtime:
    displayName: Modified
  file.tags:
    displayName: Tags
  file.ctime:
    displayName: Created
views:
  - type: table
    name: This week in notes
    filters:
      and:
        - file.ctime > now() - "7d"
        - '!file.tags.containsAny("type/day")'
    order:
      - file.name
      - dg-publish
      - file.mtime
      - file.tags
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC

```
 

## Get in touch!
I'm on LinkedIn, but I'd prefer an email.

## Footer
I don't use AI, generative or otherwise, in any capacity for these notes.[^1] If you want to see more websites like this, check out the [Obsidian Garden Gallery](https://vaults.obsidian-community.com/) Community!

[^1]: That would defeat the purpose of writing to think.
