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

- a **front site** — home, résumé, pottery
- a **digital garden** — a growing, interlinked collection of notes (you're reading one right now 🌱)

## The stack

Everything is static and free to host. The pieces:

- **Next.js** (React) for the front site — built as a static export
- **Quartz** for the digital garden
- **Obsidian** for writing notes (on my laptop *and* my phone)
- **GitHub Pages** for hosting, **GitHub Actions** for the build/deploy
- Fonts: Syne (my name), DM Mono, Inter, Outfit

## The process

It was *very* iterative. We went through several full redesigns before landing on the look. The front site started as plain HTML/CSS, then got rebuilt in Next.js so it's easier to add to later.

The garden took a bit of plumbing. Notes live in their own little repo so I can sync them cleanly to my phone; when I write something, it pushes to GitHub, a workflow rebuilds the site, and the note appears here a couple of minutes later. No manual publishing — I just write.

## What this means in practice

I can open Obsidian, jot down a thought, and it quietly shows up in the garden. That low-friction loop was the whole goal: **make it so simple it's sustainable.**

## Reflections

Building this with AI was a strange and lovely experience — equal parts "wow, that was fast" and "no, not like *that*." I drove the taste and the decisions; the AI handled the wiring and the parts I didn't know how to do. The result is something I actually want to tend.

If you're curious about any of it, wander around the rest of the garden or reach out.