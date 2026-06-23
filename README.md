# Duk Creek

<p align="center">
  <img width="100" height="80" alt="Duk Creek Logo" src="https://github.com/user-attachments/assets/3a913605-acb5-48f7-ade5-4ab3302a40f2" />
</p>

**Duk Creek** is a utility that converts **Ducky Script** payloads into **Evil Crow Cable Wind** compatible payloads.

## Features

- Convert standard Ducky Script commands
- Generate Evil Crow Cable Wind payloads automatically
- Simplify payload migration between platforms
- Lightweight and easy to use

### Example

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

## Why Duk Creek?

Many payloads are written for USB Rubber Ducky devices using Ducky Script. Duk Creek helps translate those payloads for use with Evil Crow Wind Cable devices, reducing manual conversion work.

## Disclaimer

This project is intended for educational purposes, authorized security testing, and research only. Users are responsible for complying with all applicable laws and obtaining proper authorization before using generated payloads.

## License

MIT License

## Converter

[dukCreek.webm](https://github.com/user-attachments/assets/d61b434a-8aa0-498a-805a-a813eff5462b)

