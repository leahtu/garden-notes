---
title: How I built this site
tags:
  - meta
  - making
---

> [!note] Written with (and by) AI
> I built this website with the help of an AI coding assistant, and this note was written by that AI too. 

## The idea

Two things under one roof:

- a **personal site** — home, résumé, pottery portfolio
- a **digital garden** — a growing, interlinked collection of notes

## The stack

Everything is **static** and **free to host**. The pieces:

| Layer          | What I used                                                |
| -------------- | ---------------------------------------------------------- |
| Front site     | **Next.js** (React, TypeScript) — built as a static export |
| Styling        | custom CSS + **next/font** (Syne, Inter, Outfit, DM Mono)  |
| Digital garden | **Quartz**                                                 |
| Writing notes  | **Obsidian** + the **Obsidian Git** plugin                 |
| Hosting        | **GitHub Pages**                                           |
| Build & deploy | **GitHub Actions**                                         |

## The process

It was *very* iterative. A rough order of how it went:

1. **Cleanup** — started from an old, outdated site and stripped out the dead links and stale pages.
2. **Redesign** — explored a *lot* of directions (layouts, fonts, colour palettes) before the full-screen gradient hero and yellow name finally clicked.
3. **Rebuild in Next.js** — the front site began as plain HTML/CSS, then got ported to Next.js/React so it's easier to add features later.
4. **Digital garden** — set up Quartz and themed it to match the site, with notes written in Obsidian.
5. **Deploy pipeline** — a GitHub Actions workflow builds *both* the site and the garden and publishes them together (site at `/`, garden at `/garden`).
6. **The notes split** — my notes live in their own little repo so I can sync them cleanly to my phone; a push triggers a rebuild and the note shows up here a couple minutes later.
7. **Writing from my phone** — Obsidian + Git on iPhone, so I can plant a note from anywhere.

## How it all connects

```
   Obsidian (laptop)              Obsidian (iPhone)
        │  push                        │  push
        └──────► notes repo ◄──────────┘
                     │  (a push triggers a rebuild)
                     ▼
        site repo ── GitHub Actions ──┐
     (Next.js + Quartz)               │
                     │ build site + build garden
                     ▼                ▼
            site at /  ──────  garden at /garden
                     └── GitHub Pages ──┘
                         → live in ~2 min
```

## What this means in practice

I can open Obsidian, jot down a thought, and it quietly shows up in the garden. That low-friction loop was the whole goal: **make it so simple it's sustainable.**

A few things that keep it tidy going forward:
- to edit the site, I work in the Next.js project and push
- to write, I just type in Obsidian (laptop or phone)
- a note marked `draft: true` stays private until I'm ready

## Reflections

Building this with AI....

If you're curious about any of it, wander around the rest of the garden or reach out.