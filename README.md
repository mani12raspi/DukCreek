# DukCreek

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-brightgreen.svg)](#)
[![Platform](https://img.shields.io/badge/platform-web-blue.svg)](https://mani12raspi.github.io/DukCreek/)

<p align="left">
<img width="180" height="150" alt="image" src="https://github.com/user-attachments/assets/e909e281-d4f2-413d-8def-287f6653b241" />
</p>

**DukCreek** is a utility that converts **Ducky Script** payloads into **Evil Crow Cable Wind** compatible payloads — no manual rewriting required.

> ⚠️ **Disclaimer:** This project is intended for educational purposes, authorized security testing, and research only. Users are responsible for complying with all applicable laws and obtaining proper authorization before using generated payloads.

## Built For

This converter targets the **[Evil Crow Cable Wind](https://github.com/joelsernamoreno/EvilCrowCable-Wind)** — a BadUSB device created by [Joel Serna Moreno](https://github.com/joelsernamoreno) ([@JoelSernaMoreno](https://x.com/JoelSernaMoreno)), based on the ESP32-S3.

DukCreek is an independent, unofficial companion tool and is not affiliated with or endorsed by the Evil Crow Cable Wind project. For the device's firmware, payload syntax reference, hardware purchase links, and setup instructions, see the [official Evil Crow Cable Wind repository](https://github.com/joelsernamoreno/EvilCrowCable-Wind).

---

## Table of Contents

- [Live Converter](#live-converter)
- [Demo](#demo)
- [Features](#features)
- [Why DukCreek?](#why-dukcreek)
- [Getting Started](#getting-started)
- [Example](#example)
- [Supported Commands](#supported-commands)
- [Known Limitations](#known-limitations)
- [License](#license)

---

## Live Converter

Use the hosted converter directly in your browser — no install needed:

**[→ Open the DukCreek Converter](https://mani12raspi.github.io/DukCreek/)**

## Demo

https://github.com/user-attachments/assets/a3bd59d3-351d-4c33-ad94-c3898ce46e35

## Features

- 🔄 Converts standard Ducky Script commands to Evil Crow Cable Wind syntax
- ⚡ Instant, in-browser conversion — no dependencies to install
- 🪶 Lightweight, single-page tool
- 🧩 Simplifies payload migration between Rubber Ducky and Evil Crow Wind Cable hardware

## Why DukCreek?

Many existing payloads are written in Ducky Script for USB Rubber Ducky devices. Evil Crow Cable Wind uses its own, different command syntax. Rewriting payloads by hand is tedious and error-prone — DukCreek automates that translation so you can reuse your existing script library.

## Getting Started

### Use it online
Just open the [hosted converter](https://mani12raspi.github.io/DukCreek/), paste your Ducky Script, and copy the converted output.

No build step or server is required — the converter runs entirely client-side.

## Example

**Input (Ducky Script):**
```text
REM Open Notepad and type Hello World (Windows - DuckyScript)
DEFAULTDELAY 150
GUI r
DELAY 500
STRING notepad
ENTER
DELAY 800
STRING Hello World!
ENTER
```

**Output (Evil Crow Wind):**
```text
RunWin notepad
Delay 150
Delay 800
PrintLine Hello World!
Delay 150
```

## Supported Commands

| Ducky Script      | Evil Crow Wind Equivalent | Notes                          |
|-------------------|---------------------------|---------------------------------|
| `GUI r`            | `RunWin`                  | Windows Run dialog              |
| `STRING`           | `PrintLine`               | Text entry                      |
| `DELAY`            | `Delay`                   | Millisecond delay               |
| `DEFAULTDELAY`     | *(applied per-command)*   | Converted into explicit delays  |
| `ENTER`            | *(implicit in `PrintLine`)* | Line break handled automatically |

> 📋 *For the complete list of Evil Crow Wind commands (e.g. `Press`, `PressRelease`, `RunPowershellAdmin`, `ShellWin`), see the [Payload Syntax reference](https://github.com/joelsernamoreno/EvilCrowCable-Wind#payload-syntax) in the official repo. Fill in this table as DukCreek's coverage grows.*

## Known Limitations

- Commands not listed above are currently unsupported and will be skipped/ignored during conversion *(update this based on actual converter behavior)*.
- No CLI or batch-file conversion yet — one script at a time via the web UI.

## License

Released under the [MIT License](LICENSE).

Evil Crow Cable Wind itself is licensed separately by its author under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — that license applies to the hardware/firmware project, not to DukCreek.
