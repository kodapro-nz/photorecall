# PhotoRecall

Find a photo by describing it. Type "a dog on a beach", "red car in snow 2019" or
"receipts", and PhotoRecall ranks your own pictures against it — no tags, no albums, no
filenames to keep tidy.

Everything runs on your computer. Your photos are never uploaded.

### [Download the latest release →](https://github.com/kodapro-nz/photorecall/releases/latest)

For Windows OS. Currently unsigned, so SmartScreen will warn on first install.

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

See [LICENSE](LICENSE)

This software and associated documentation files (the "Software") are proprietary 
and confidential. You are hereby granted a personal, non-exclusive, non-transferable 
license to download, install, and execute the Software solely for its intended purpose.

You may NOT:
1. Modify, translate, adapt, or create derivative works of the Software.
2. Reverse engineer, decompile, disassemble, or attempt to derive the source code.
3. Rent, lease, sell, sublicense, or commercially exploit the Software.
4. Redistribute or re-host the Software binaries on third-party channels without prior written permission.

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

The machine-learning models PhotoRecall downloads are not covered by this
licence. They are Apache-2.0 (SigLIP 2) and MIT (OpenAI CLIP); see
THIRD-PARTY-NOTICES.html and tools/model_notices/ for the full text and
attribution. THIRD-PARTY-NOTICES.html also lists every Rust dependency and its
licence, and is shipped with the installer.
