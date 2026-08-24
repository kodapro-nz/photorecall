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
- Search while it is still working, and after you close the window — it keeps going from
  the tray.
- Choose a model: 610 MB and fast, or 4.6 GB and best at finding things. Switching back
  costs nothing, and you choose which drive the download lands on.
- Reads **HEIC** from your iPhone, as well as JPEG, PNG, WebP, TIFF, BMP, GIF and JPEG XL.
  HEIC uses Windows' own codec, so if your PC is missing it PhotoRecall says which two free
  extensions to install rather than quietly skipping those photos.
- It tells you what it could not read, and why.

## Built with

**Rust**, end to end — eight engine crates, a command-line tool, and a
[Tauri](https://tauri.app) window whose front end is three static files with no bundler.

**[LanceDB](https://lancedb.com)** for storage and search: vectors, paths and camera
metadata in one embedded table. Search is exact rather than approximate — every vector is
compared, every time, so nothing is quietly missed.

Photos are understood by [OpenCLIP](https://github.com/mlfoundations/open_clip) models
running on [ONNX Runtime](https://onnxruntime.ai), on the processor or the graphics card.

## Status

**0.1.0** — the first release. Searches your library by description, reads HEIC as well
as the usual formats, and shows only the photos that actually match. Windows only in
practice.

## For developers

`photorecall` is the same engine from a terminal (`index`, `search`, `status`, `compare`,
all with `--json`), installed beside the window. [CHANGELOG.md](CHANGELOG.md) records what
each version did.

The source is not public. This repository is where PhotoRecall is released, not where it
is written.

## Licence

MIT — see [LICENSE](LICENSE). Models are separately licensed (Apache-2.0 and MIT).

PhotoRecall is provided as is, with no warranty: Kodapro accepts no responsibility for any
loss or damage arising from its use. It searches a copy of what it has read and is **not a
backup**, and its matches come from a machine-learning model that is often wrong — check a
photo yourself before acting on a search.
