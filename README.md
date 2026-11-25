### Hi, I'm Anay (`adper`)

I'm a cybersecurity student at NFSU Gandhinagar. Outside of classes, I build security tools, smart utilities, and local-first ML systems that run offline without cloud dependencies.

More write-ups and project notes at **[dearanayji.rocks](https://dearanayji.rocks)**.

---

### Projects

#### [Verity](https://github.com/ADPer0705/verity) `v0.6.0` · [Wiki](https://verity.dearanayji.rocks)
Multi-modal deepfake forensics suite for image, video, and audio. Runs **58 detector architectures** (39 evidence-grade) in isolated, version-pinned `uv` environments alongside 5 model-free forensic analyzers, keeping panel outputs separate rather than collapsing them into a single score. Ships as a standalone air-gapped Linux binary with USB kit export/import and SHA-256 chain-of-custody bundles.

#### [DroidScanner](https://github.com/ADPer0705/droidscanner) `v1.1.2` · [Wiki](https://droidscanner.dearanayji.rocks)
Rootless, offline Android security analyzer with the `INTERNET` permission stripped at the manifest level. Combines a permission/combo scoring engine (~380 permissions, 19 rules) with streaming low-RAM APK/DEX inspection, pre-install certificate mismatch checks, 16 device posture audits, a `WorkManager` background guard, and an on-device MediaPipe encoder.

#### [sempropos](https://github.com/ADPer0705/sempropos) `v1.0.1` · [Wiki](https://sempropos.dearanayji.rocks) · [PyPI](https://pypi.org/project/sempropos/)
Offline semantic replacement for `apropos`, `man`, and `--help`. Indexes local binaries from `man(7)`/`mdoc(7)`, `tldr-pages`, Fish/Zsh completions, and safe `--help` probing into SQLite + FTS5 + FastEmbed, synthesizing grounded commands via local GGUF models (`llama.cpp`) or Ollama over a warm Unix-socket daemon (`<200ms`) with a `Ctrl+S` shell widget.

#### [ChronoTrace](https://github.com/GR4Y-SCALE/ChronoTrace) `2026`
NTFS anti-forensics detection framework for post-mortem EnCase `.E01` images and live Windows hosts. Parses `$MFT`, `$UsnJrnl`, and `$LogFile` via `libewf`, correlates `$SI` vs. `$FN` timestamps across 15 deterministic rules, and streams timelines over FastAPI and React 19 WebSockets.

#### [ADBSight](https://github.com/ADPer0705/adbsight) `v1.0.0` · [Wiki](https://adbsight.dearanayji.rocks)
Cross-platform Rust + Ratatui terminal inspector over USB and Wi-Fi ADB. Includes Android 11+ terminal QR pairing, mDNS discovery, USB-to-Wi-Fi handoff, 8 live modules (CPU/Wi-Fi sparklines, `dumpsys`, processes, packages, streaming logcat, dual-pane file browser, personal data, shell), WAL-mode SQLite snapshots, and a `--demo` mode.

#### [Gloss](https://github.com/ADPer0705/gloss) `v2.4.0` · [Wiki](https://gloss.dearanayji.rocks)
202-language offline Android translation reader running quantized Meta AI `NLLB-200-distilled-600M` INT8 ONNX (~1.4 GB peak RAM). Built for fast daily reading with tap-a-word lookups, home-screen widgets, offline TTS, and in-app GitHub Releases / Obtainium updates.

---

### Smaller Tools & Experiments

- **[`@adper/wordsmith`](https://github.com/ADPer0705/wordsmith)** ([npm](https://www.npmjs.com/package/@adper/wordsmith)) — Zero-config TypeScript CLI using local ONNX zero-shot NER (`GLiNER`) and `chrono-node` to generate probability-ranked password wordlists from OSINT text.
- **[`qr-transfer`](https://github.com/ADPer0705/qr-transfer)** — Rust CLI for air-gapped file transfer between two machines over screen-to-webcam QR codes with stop-and-wait ARQ and SHA-256 verification.
- **[`MerkleWatch`](https://github.com/ADPer0705/MerkleWatch)** — SHA-256 Merkle-tree directory snapshot and tamper verification CLI.
- **[`Inquiro`](https://github.com/CY-N4P5E/Inquiro)** — Local-first RAG document assistant built with LangChain, FAISS, and Ollama.
- **[`TeleDM`](https://github.com/ADPer0705/TeleDM)** — Interrupt-tolerant Tkinter download manager backed by SQLite and the Telegram API.

---

### Stack

- **Languages:** Python, Rust, Kotlin, C/C++, TypeScript, Bash, SQL
- **Local AI & Retrieval:** PyTorch, ONNX Runtime, `llama.cpp`, MediaPipe, FastEmbed, SQLite FTS5
- **Systems & Infra:** Linux (Fedora / Debian / Kali), Android SDK, Jetpack Compose, Ratatui, FastAPI, React, Docker, AWS (Lambda / SAM)
- **Focus Areas:** Deepfake Forensics, NTFS / DFIR, Android Security, Offline Inference

---

[![Portfolio](https://img.shields.io/badge/dearanayji.rocks-05070d?style=flat-square&logo=safari&logoColor=00e5c8)](https://dearanayji.rocks)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-05070d?style=flat-square&logo=linkedin&logoColor=38bdf8)](https://linkedin.com/in/dearanayji)
[![Medium](https://img.shields.io/badge/Medium-05070d?style=flat-square&logo=medium&logoColor=edf2ff)](https://medium.com/@adper0705)
[![X](https://img.shields.io/badge/X-05070d?style=flat-square&logo=x&logoColor=edf2ff)](https://x.com/dearanayji)
[![Email](https://img.shields.io/badge/dearanayji%40gmail.com-05070d?style=flat-square&logo=gmail&logoColor=00e87a)](mailto:dearanayji@gmail.com)
