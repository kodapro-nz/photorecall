# Changelog

PhotoRecall finds your photos by describing them, entirely on your own machine.

This file is written for someone *using* PhotoRecall rather than building it: what changed,
and what it means for your photos, your disk and your time. Versions follow
[semantic versioning](https://semver.org/). `photorecall --version` and the window's sidebar
both report the running one.

---

## Unreleased

## 0.1.0 — 2026-08-24

The first release.

There is nothing here to compare against, so this entry says what PhotoRecall *is* rather
than what changed. Later entries will do the usual thing.

### Finding a photo

Point PhotoRecall at a folder and describe what you are looking for — "a dog on a beach",
"red car in snow 2019", "receipts". It ranks your own pictures against the description. No
tags, no albums, no filenames to keep tidy.

It answers with the photos that actually match. When your library holds nothing like what
you asked for, it says so and shows you nothing, rather than filling the window with its
five least-bad guesses. Where it holds results back, it tells you how many.

You can search while it is still reading, and the folder keeps being watched after you
close the window — PhotoRecall carries on from the notification area, and new photos are
picked up as they arrive.

### What it reads

JPEG, PNG, WebP, TIFF, BMP, GIF and JPEG XL. **HEIC** from an iPhone is read through
Windows' own codec, so on a PC that is missing it PhotoRecall names the two free
extensions to install rather than quietly passing those photos by.

RAW files are counted and reported, not read.

Whatever it could not read, it lists, with the reason.

### Choosing how it runs

Two models: **610 MB and fast**, or **4.6 GB and better at finding things**. You choose
which, you choose the drive the download lands on, and switching back later costs nothing.

It runs on your processor or on your graphics card, and it will tell you which. You can
cap how much of the computer it may use while you are working.

### What leaves your machine

Your photos, never. Searching, reading and ranking all happen locally, and there is no
account and no upload.

Two things do use the network, both only when you ask: downloading a model, and the
"check for updates" button, which asks GitHub whether a newer version exists and sends
nothing beyond the fact that a copy of PhotoRecall asked.

### Before you rely on it

Windows only. The installer is per-user and needs no administrator rights, but it is **not
code-signed**, so Windows will show a "Windows protected your PC" warning on first install.

PhotoRecall searches a copy of what it has read. It is **not a backup**, and its matches
come from a machine-learning model that is often wrong — check a photo yourself before
acting on a search.
