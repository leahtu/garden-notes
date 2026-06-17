---
title: How I built my site
tags:
  - meta
  - making
---

> [!note] Written with AI
> I built my website with the help of an AI coding assistant, and this note was written by AI too. Except for the reflection section.

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

## Reflection

Building my personal site with AI was so much fun. I've heard about so many people having their lightbulb moment with AI, and I thought I'd already had mine when I first contributed code as a PM at work. But I think creating this site was my true aha-moment. 

I've been vibe-coding at work for a few months now, but never on any personal projects. While building this site, I felt the same excitement and wonder I felt when I first learned how to code in my CS class. 

I went into this not knowing how I wanted anything to look, so I did spend a few hours going back and forth with my agent until I was happy with the layout (which was annoying because I kept thinking "grr why can't you just do something good that I like?!"). I spent way more time on this than I expected to. I thought I'd be done in an hour. 

But I became obsessed! All I wanted to do was keep prompting and building. It really felt like having a fairy godmother with a magic wand. Whatever I asked for, it would become real within minutes. I kept losing track of time because I was having so much fun. I just wanted to build!!!!! 

What a great feeling. And it's a feeling I want to continue chasing. I'm excited to make more things that spark joy and creativity!