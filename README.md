 # A. Karim Bouchiba

**I build local-first software** — desktop and data tools that run entirely offline, cost $0/month, and never send your files to someone else's server.

Based in Tunisia. Open to full-time roles, contract work, and custom builds.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karim-shade-161ab5400/)
[![Email](https://img.shields.io/badge/Email-karimvshade@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:karimvshade@gmail.com)

---

## 🎙️ DoVoice — my current focus

**[→ DoVoice](https://github.com/karimvshade-a11y/DoVoice)** · Python · PyTorch · Kokoro-82M · Gradio

Turn text — or a whole book — into spoken audio, entirely on your own machine. No API keys, no cloud, no per-character billing. Once the model is cached it never touches the network again.

**[Download it and double-click it](https://github.com/karimvshade-a11y/DoVoice/releases/latest)** — 708 MB, no Python, no setup, no internet. The model and all 46 voices are inside the download.

- **61 hours of finished audiobook across six books**, including Moby Dick (21.6 h, 143 chapters) and a scanned OCR Sherlock Holmes. Not a demo — the bugs that mattered were all found by real books.
- **EPUB in, `.m4b` out**, with chapter markers and cover art read from the book's own table of contents. Renders are resumable, so an interrupted twelve-hour job picks up where it stopped.
- **Every render is planned first.** Chapter count, estimated length and estimated render time are reported *before* any audio is made, and chapters that will fail are named up front. On the Odyssey the estimate landed within 2% of the real 12 hours.
- **46 voices across 9 languages**, each routed through its own phonemizer — the failure it prevents is silent, not loud: a British voice sent through American rules produces no error, only subtly wrong pronunciation.
- **Word-level subtitles** built from the model's own phoneme durations, not interpolated from character counts.
- **OpenAI-compatible API.** Point any app that already pays for OpenAI TTS at `localhost` and change one URL.

Runs at **25× realtime** on a GTX 1650 SUPER — a card from 2019 — and 1.5× on a plain processor, which is why the download works on any Windows PC.

---

## ⚡ Gary Defeater

**[→ defeat-gary](https://github.com/karimvshade-a11y/defeat-gary)** · Python · SQLite · Streamlit

Every company runs on a spreadsheet somebody built years ago and nobody dares touch. Gary Defeater replaces it — any Excel workbook becomes a real SQLite database with a web dashboard, without a single line of configuration.

- **Computed columns the database physically refuses to overwrite.** Define a formula once; SQLite recalculates it on every read and rejects any write. No more pasting over row 4,000 and silently breaking the sheet.
- **Conflict detection.** Two people editing the same record no longer means one of them silently loses.
- **Dynamic schema.** Forms, filters and charts are generated from the live database at runtime, so any workbook works without touching the code.
- **Optional roles** (admin / editor / viewer) with salted PBKDF2 hashing, off by default.
- **$0/month, fully offline, no vendor lock-in** — the reasons the original spreadsheet won in the first place.

---

## 🧰 The rest of the workshop

Same principle throughout: your data stays on your machine.

| Project | What it does | Stack |
| --- | --- | --- |
| **[ultimate-converter](https://github.com/karimvshade-a11y/ultimate-converter)** | Privacy-first desktop file converter — video, audio, images, documents and scanned PDFs, entirely offline with no uploads or size limits. | Rust · Tauri |
| **[CyclopsPro](https://github.com/karimvshade-a11y/CyclopsPro)** | High-performance screen capture and live streaming for Windows. | — |
| **[gari](https://github.com/karimvshade-a11y/gari)** | Graph-augmented repository intelligence — a fully offline AI software engineering workspace. | — |
| **[AgeCraft](https://github.com/karimvshade-a11y/AgeCraft)** | Local, private face re-aging for photos and video. | — |

These tools build each other. The demo GIF on Gary Defeater was recorded with CyclopsPro and converted by ultimate-converter — the demo of an offline tool, made entirely with offline tools.

---

## How I work

- **Offline by default.** No telemetry, no API keys, no cloud dependency. If a feature needs the internet, it earns it. DoVoice ships its model *inside* the download rather than fetching it on first run, because a tool sold as offline should not need the network to say its first word.
- **Failures that explain themselves.** Every error says what went wrong and what to do next — never a blank file that pretends to have worked.
- **Measured, not assumed.** Codec quality decisions in ultimate-converter came from SSIM comparisons, not defaults. Three optimizations were cut from DoVoice on measurement — `torch.compile` gave no gain, `cudnn.benchmark` was actively worse, fp16 broke — because a knob that does nothing is worse than no knob at all.
- **Documented like someone else has to run it.** Every repo has a README that gets a stranger from clone to working in one pass. Where a limit is untested, it says so.

**Toolbox:** Python · Rust · PyTorch · SQL / SQLite · Streamlit · Tauri · Pandas · FFmpeg & ImageMagick pipelines · Tesseract OCR · PyInstaller · Git

---

## Work with me

I take on contract builds and I'm open to full-time roles.

If your team runs on a spreadsheet that everyone is afraid to touch, or you need a desktop tool that works without a subscription and without uploading anything — that's exactly the problem I build for.

📫 **karimvshade@gmail.com** · [LinkedIn](https://www.linkedin.com/in/karim-shade-161ab5400/)
