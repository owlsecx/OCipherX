# 🦉 OCipherX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%2F%20Windows-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OCipher%20%2F%20Classical%20Ciphers-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Interface-GUI%20%28Tkinter%29-blueviolet?style=flat-square"/>
  <img src="https://img.shields.io/badge/No%20Dependencies-Stdlib%20Only-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-2.0-cyan?style=flat-square"/>
</p>

> **OCipherX** is the GUI edition of the classical cipher suite — a full dark-themed desktop application with 8 cipher engines, Caesar brute-force, letter frequency analysis with bar chart, Index of Coincidence, clipboard integration, session history, and JSON/TXT export.

---

> ⚠️ Classical ciphers are **not secure** for protecting real data. Use **OCrypt** for modern encryption.

---

## 📌 Overview

OCipherX wraps the same classical cipher engine as OCipher inside a Tkinter dark-themed GUI (1280×840). The sidebar controls the cipher, key, mode, and actions — the main panel provides tabbed views for the cipher workspace, brute-force results, frequency analysis chart, history log, cipher reference, and about.

---

## 🔐 Ciphers

| Cipher | Key Format | Symmetric |
|--------|-----------|-----------|
| **Caesar** | Integer 1–25 | ✔ with inverse shift |
| **Vigenère** | Letters keyword | ✗ |
| **Atbash** | None | ✔ self-inverse |
| **Beaufort** | Letters keyword | ✔ same key for E/D |
| **Affine** | `a,b` e.g. `5,8` — `a` must be coprime with 26 | ✗ |
| **Rail Fence** | Integer 2–10 (number of rails) | ✗ |
| **XOR** | Any string | ✔ same key for E/D |
| **Playfair** | Letters keyword (J treated as I) | ✗ |

---

## 🖥️ Interface Tabs

| Tab | Contents |
|-----|---------|
| **CIPHER** | Input textarea · Run Cipher button · Output textarea with Copy and Use-as-Input actions |
| **BRUTE FORCE** | All 25 Caesar shifts displayed simultaneously — colour-highlighted |
| **FREQ ANALYSIS** | Canvas bar chart (observed % vs English reference %) + letter-by-letter table with observed%, English%, and diff |
| **HISTORY** | Treeview table of all session operations — timestamp, cipher, mode, key, input/output previews; click a row for full detail |
| **REFERENCE** | Built-in cipher reference — description, key format, and example for each cipher |
| **ABOUT** | Tool info |

---

## 🎛️ Sidebar Controls

| Section | Controls |
|---------|---------|
| **CIPHER** | Dropdown selector · Key entry with live hint |
| **MODE** | Encrypt / Decrypt radio buttons |
| **ACTIONS** | Run Cipher · Swap I/O · Brute Force · Freq Analysis · Clear |
| **CLIPBOARD** | Paste to Input · Copy Output |
| **TEXT STATS** | Input char count · Letter count · Index of Coincidence (IC value) |
| **EXPORT** | Export JSON · Export TXT · Clear Log |

---

## 📊 Frequency Analysis

The Freq Analysis tab produces a dual-bar canvas chart comparing the observed letter distribution in the input text against standard English frequencies. The table below the chart shows observed%, English%, and the deviation (±) per letter — useful for frequency-based cryptanalysis of substitution ciphers.

The sidebar also shows the **Index of Coincidence (IC)** live as text is typed — a value near 0.065 suggests English plaintext or a monoalphabetic cipher; values closer to 0.038 suggest a polyalphabetic cipher like Vigenère.

---

## 📤 Export

History can be exported at any time via the sidebar:

| Format | Contents |
|--------|----------|
| **JSON** | Full session: tool metadata, exported timestamp, list of all operations with cipher, mode, key, input, output |
| **TXT** | Human-readable log of all session operations |

Files are saved via a native file-save dialog.

---

## ⚙️ Requirements

- **Linux or Windows** with a display
- **No Python installation needed** — runs as a standalone executable
- **No external dependencies** — Tkinter is part of the Python standard library

---

## 🚀 Usage

```bash
./OCipherX
```

---

## 🔗 Related Tools

| Tool | Description |
|------|-------------|
| **OCipher** | CLI edition — same 8 ciphers plus Bacon, Polybius, ROT13, and Auto-Detect |
| **OCrypt** | Modern encryption suite for real security needs |

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
