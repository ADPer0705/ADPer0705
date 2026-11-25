```text
ADPER(1)                         User Systems Manual                        ADPER(1)

NAME
       adper — Anay Dhaval Pandya · Cybersecurity, Forensics & Local-First Systems

SYNOPSIS
       adper [--focus Cybersecurity|local-ai|systems]
             [--env linux] [--cloud-dependency none]

SPEC
       role        :: CSE (Cybersecurity) @ National Forensic Sciences University
       location    :: Gandhinagar, India
       philosophy  :: Deterministic where possible. Offline by default.
                      Zero rent-seeking wrappers around someone else's API.
       long_game   :: A Stark-grade personal workstation.
```

I'm adper, a cybersecurity student at NFSU Gandhinagar. Outside of classes, I mostly build security tools, automation and smart utilities, and work on running machine learning models locally without cloud dependencies. You can find my projects and write-ups at [dearanayji.rocks](https://dearanayji.rocks).

---

### `01` // Flagship Systems

<table>
  <thead>
    <tr>
      <th align="left">System</th>
      <th align="left">Domain</th>
      <th align="left">Engineering Spec</th>
      <th align="left">Links</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong><a href="https://github.com/ADPer0705/verity">Verity</a></strong><br/><code>v0.6.0</code></td>
      <td>Deepfake Forensics</td>
      <td>
        Multi-modal examination for image, video, and audio. Ports <strong>58 detector architectures</strong> (39 evidence-grade) into isolated, version-pinned <code>uv</code> envs alongside 5 model-free forensic analyzers. Never collapses split panels into one fake/real score. Ships as a standalone air-gapped Linux executable with USB kit export/import and SHA-256 chain-of-custody <code>.zip</code> bundles.
      </td>
      <td>
        <a href="https://verity.dearanayji.rocks">Wiki</a><br/>
        <a href="https://github.com/ADPer0705/verity">Repo</a>
      </td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/ADPer0705/droidscanner">DroidScanner</a></strong><br/><code>v1.1.2</code></td>
      <td>Android Security</td>
      <td>
        Rootless, 100% offline Android security guardian with <code>INTERNET</code> permission stripped at the OS manifest level. Pairs Scoring Engine v3 (~380 permissions, 19 combo rules) with streaming low-RAM Deep APK/DEX inspection, pre-install APK cert-mismatch checks, 16 device posture audits, a <code>WorkManager</code> background guard, and a bounded on-device MediaPipe encoder.
      </td>
      <td>
        <a href="https://droidscanner.dearanayji.rocks">Wiki</a><br/>
        <a href="https://github.com/ADPer0705/droidscanner">Repo</a>
      </td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/ADPer0705/sempropos">sempropos</a></strong><br/><code>v1.0.1</code></td>
      <td>Local AI / CLI</td>
      <td>
        Offline-first replacement for <code>apropos</code>, <code>--help</code>, and <code>man</code>. Indexes local binaries across 4 sources (<code>man(7)</code>/<code>mdoc(7)</code>, <code>tldr-pages</code>, Fish/Zsh completions, safe <code>--help</code> probing) into SQLite v3 + FTS5 + FastEmbed. Synthesizes grounded shell commands via curated local GGUF models (<code>llama.cpp</code>) or Ollama behind a warm Unix-socket daemon (<code>&lt;200ms</code>) and <code>Ctrl+S</code> shell widget.
      </td>
      <td>
        <a href="https://sempropos.dearanayji.rocks">Wiki</a><br/>
        <a href="https://github.com/ADPer0705/sempropos">Repo</a><br/>
        <a href="https://pypi.org/project/sempropos/">PyPI</a>
      </td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/GR4Y-SCALE/ChronoTrace">ChronoTrace</a></strong><br/><code>2026</code></td>
      <td>NTFS Forensics</td>
      <td>
        NTFS anti-forensics detection framework for post-mortem EnCase <code>.E01</code> images and live Windows monitoring. Parses <code>$MFT</code>, <code>$UsnJrnl</code>, and <code>$LogFile</code> via <code>libewf</code>, correlates <code>$SI</code> vs <code>$FN</code> timestamps across 15 deterministic rules, and streams live alerts &amp; timelines over FastAPI + React 19 WebSockets.
      </td>
      <td>
        <a href="https://github.com/GR4Y-SCALE/ChronoTrace">Repo</a>
      </td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/ADPer0705/adbsight">ADBSight</a></strong><br/><code>v1.0.0</code></td>
      <td>Systems / Android</td>
      <td>
        Cross-platform Rust + Ratatui TUI deep inspector over USB and Wi-Fi ADB. Features Android 11+ terminal Unicode QR pairing, mDNS auto-discovery, USB-to-Wi-Fi handoff, 8 live inspector modules (CPU/Wi-Fi sparklines, <code>dumpsys</code>, processes, packages, streaming logcat, dual-pane files, personal data, shell), WAL-mode SQLite snapshots, and a <code>--demo</code> simulator.
      </td>
      <td>
        <a href="https://adbsight.dearanayji.rocks">Wiki</a><br/>
        <a href="https://github.com/ADPer0705/adbsight">Repo</a>
      </td>
    </tr>
    <tr>
      <td><strong><a href="https://github.com/ADPer0705/gloss">Gloss</a></strong><br/><code>v2.4.0</code></td>
      <td>On-Device NLP</td>
      <td>
        202-language offline Android translation reader powered by quantized Meta AI <code>NLLB-200-distilled-600M</code> INT8 ONNX (~1.4 GB peak RAM). Built for instant daily lookup: bidirectional tap-a-word meanings, home-screen widgets, offline TTS, and in-app GitHub Releases / Obtainium updates with zero telemetry.
      </td>
      <td>
        <a href="https://gloss.dearanayji.rocks">Wiki</a><br/>
        <a href="https://github.com/ADPer0705/gloss">Repo</a>
      </td>
    </tr>
  </tbody>
</table>

---

### `02` // Lab Archive & Smaller Utilities

Smaller tools, focused experiments, and coursework builds that solve one sharp problem and stay out of the way:

- **[`@adper/wordsmith`](https://github.com/ADPer0705/wordsmith)** ([npm](https://www.npmjs.com/package/@adper/wordsmith)) — Zero-config TypeScript CLI using local ONNX zero-shot NER (`GLiNER`) + `chrono-node` to turn OSINT text into probability-ranked password wordlists.
- **[`qr-transfer`](https://github.com/ADPer0705/qr-transfer)** — Rust terminal file transfer between two air-gapped laptops over screen-to-webcam QR codes implementing stop-and-wait ARQ and SHA-256 verification.
- **[`MerkleWatch`](https://github.com/ADPer0705/MerkleWatch)** — Deterministic SHA-256 Merkle-tree directory snapshots and tamper verification CLI.
- **[`Inquiro`](https://github.com/CY-N4P5E/Inquiro)** — Local-first RAG document assistant built on LangChain, FAISS, and Ollama.
- **[`TeleDM`](https://github.com/ADPer0705/TeleDM)** — Interrupt-tolerant Tkinter desktop download manager backed by SQLite and the Telegram API.

---

### `03` // Toolchain & Runtime

```text
languages     :: Python · Rust · Kotlin · C/C++ · TypeScript · Bash · SQL
ai / local ml :: PyTorch · ONNX Runtime · llama.cpp · MediaPipe · FastEmbed · RAG / FTS5
web / infra   :: FastAPI · React · WebSockets · SQLite · Docker · AWS (Lambda / SAM)
platforms     :: Linux (Fedora / Debian / Kali) · Android SDK · Jetpack Compose · Ratatui
domains       :: Deepfake Forensics · NTFS / DFIR · Android Security · Systems Tooling
```

---

### `04` // Signals

[![Portfolio](https://img.shields.io/badge/dearanayji.rocks-05070d?style=flat-square&logo=safari&logoColor=00e5c8)](https://dearanayji.rocks)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-05070d?style=flat-square&logo=linkedin&logoColor=38bdf8)](https://linkedin.com/in/dearanayji)
[![Medium](https://img.shields.io/badge/Medium-05070d?style=flat-square&logo=medium&logoColor=edf2ff)](https://medium.com/@adper0705)
[![X](https://img.shields.io/badge/X-05070d?style=flat-square&logo=x&logoColor=edf2ff)](https://x.com/dearanayji)
[![Email](https://img.shields.io/badge/dearanayji%40gmail.com-05070d?style=flat-square&logo=gmail&logoColor=00e87a)](mailto:dearanayji@gmail.com)
