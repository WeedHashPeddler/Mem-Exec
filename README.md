<div align="center">

# 🐚 MEMEXEC

### Fileless In-Memory PE Loader for Cobalt Strike

![Status](https://img.shields.io/badge/status-public-2ea043)
![BOF](https://img.shields.io/badge/type-BOF-2ea043)
![Platform](https://img.shields.io/badge/platform-Windows%20x86%20%2F%20x64-2ea043)
![Cobalt Strike](https://img.shields.io/badge/Cobalt%20Strike-4.x-2ea043)
![Author](https://img.shields.io/badge/author-WeedPeddler-2ea043)

</div>

---

## 👋 Hey researchers

This is a very old BOF of mine. I don't really need it anymore, so I'm releasing it publicly.

`MEMEXEC` runs a Windows EXE fully in-memory — nothing touches disk, no dropped files, no mess left behind. It comes as a Beacon Object File (BOF) with a simple Aggressor script, so you just right-click a beacon and pick it from a menu.

---

## ✅ AV / EDR tested

| # | Vendor / Product | Type | Bypass |
|---|------------------|------|:------:|
| 1 | Kaspersky | EDR | ✅ |
| 2 | Trend Micro Apex One | XDR + EDR | ✅ |
| 3 | Microsoft Defender | AV | ✅ |
| 4 | AVG | AV | ✅ |
| 5 | Avast | AV | ✅ |
| 6 | ESET | EDR | ✅ |
| 7 | Bitdefender | EDR | ✅ |
| 8 | Trellix | EDR | ✅ |

---

## 🚀 How to use

### What you need

- Cobalt Strike with a live beacon.
- The EXE you want to run.
- The compiled `memexec.o` file.

### Getting started

1. **Drop the files** into your Cobalt Strike scripts folder:
   - `memexec.cna`
   - `memexec.o`

2. **Load the script** through the Script Manager, or just:
   - Right-click in the beacon console → **MEMEXEC** → **Load PE In-Memory**.

3. **Pick a beacon**, then use the GUI below.

---

### Using the GUI (right-click)

1. Right-click a beacon → **MEMEXEC** → **Load PE In-Memory**.
2. Pick your EXE file.
3. Choose a **target** from the presets:
   - `Native x64`
   - `Native x86`
   - `.NET x64`
   - `.NET x86`
   - `Custom path` → type your own target
4. *(Optional)* Add arguments.
5. Pick the output mode:
   - `Capture Output (Always)`
   - `No Output (Fire And Forget)`
6. Hit **Execute**.

---

## ⚠️ Disclaimer

This is for **education and authorized security testing only**.

Only use `MEMEXEC` on machines you own or have written permission to test. Using this the wrong way can land you in legal trouble, and I take no responsibility for how you use it.

---

<div align="center">

**Made by WeedPeddler**

</div>
