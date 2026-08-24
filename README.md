# PhotoRecall

Find a photo by describing it. Type "a dog on a beach", "red car in snow 2019" or
"receipts", and PhotoRecall ranks your own pictures against it — no tags, no albums, no
filenames to keep tidy.

Everything runs on your computer. Your photos are never uploaded.

### [Download the latest release →](https://github.com/kodapro-nz/photorecall/releases/latest)

Windows. Per-user installer, no administrator rights. Unsigned, so SmartScreen warns on
first install.

## What it does

- Point it at a folder. It reads what is in it, then watches for what arrives.
- Choose a model to analyze your photos (Fast, Medium and Slow).
- Reads JPEG, PNG, WebP, TIFF, BMP, GIF and JPEG XL.
  To read HEIC files, your system must have an HEIC codec installed.

## Screenshots

<img width="1169" height="811" alt="image" src="https://github.com/user-attachments/assets/db4a9188-35e8-418e-93e2-bab688049eef" />
Photo search screen

## Built with

**Rust**, end to end — eight engine crates, a command-line tool, and a
[Tauri](https://tauri.app) window whose front end is three static files with no bundler.

**[LanceDB](https://lancedb.com)** for storage and search: vectors, paths and camera
metadata in one embedded table.

Photos are understood by [OpenCLIP](https://github.com/mlfoundations/open_clip) models
running on [ONNX Runtime](https://onnxruntime.ai), on the processor or the graphics card.

## Status

**0.1.0** — the first release. Searches your library by description, reads HEIC as well
as the usual formats, and shows only the photos that actually match. Current supports Windows only.

## Licence

Copyright (c) 2026 Kodapro. All Rights Reserved.

This software and associated documentation files (the "Software") are proprietary 
and confidential. You are hereby granted a personal, non-exclusive, non-transferable 
license to download, install, and execute the Software solely for its intended purpose.

You may NOT:
1. Modify, translate, adapt, or create derivative works of the Software.
2. Reverse engineer, decompile, disassemble, or attempt to derive the source code.
3. Rent, lease, sell, sublicense, or commercially exploit the Software.
4. Redistribute or re-host the Software binaries on third-party channels without prior written permission.

CLIP models are separately licensed (Apache-2.0 and MIT).

PhotoRecall is provided as is, with no warranty: Kodapro accepts no responsibility for any
loss or damage arising from its use. It searches a copy of what it has read and is **not a
backup**, and its matches come from a machine-learning model that is often wrong — check a
photo yourself before acting on a search.
