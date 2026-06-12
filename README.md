<div align="center">

![DriftKing — C++, embedded, FPGA, AI audio, LLM tooling](assets/banner.svg)

[![Discord](https://img.shields.io/badge/Discord-Dołącz_do_serwera-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/D3mUWyqh)

</div>

# 👋 Cześć, jestem DriftKing

Łączę dwa światy: **żelazo** (C++, FPGA, mikrokontrolery) i **AI** (synteza mowy po
polsku, narzędzia dla agentów LLM). Lubię projekty, które kończą się mierzalnym
dowodem — benchmarkiem, zielonym CI albo działającym sprzętem na biurku.

- 🎙️ **AI audio po polsku** — pipeline'y TTS i klonowania głosu z automatyczną
  gwarancją jakości (pętla ASR + CER), normalizacją głośności EBU R128 i konwersją RVC
- 🔌 **Embedded** — RP2350 (Pico 2), ESP32, FPGA Tang Nano (Verilog), PCB w KiCadzie
- 🤖 **Narzędzia dla agentów AI** — mniej tokenów, szybsze hooki, twarde benchmarki
- 🛠️ Buduję z pomocą agentów AI (Claude Code, Gemini) — od pomysłu do publicznego
  repo z CI potrafi minąć jedna sesja, czasem prowadzona z telefonu

---

## 🚀 Wybrane projekty

### [tok](https://github.com/gangg111/tok) — uniwersalne proxy odchudzające tokeny
Filtruje i kompresuje wyjścia komend CLI **zanim trafią do kontekstu LLM**
(Claude Code / Gemini / Copilot / Cursor). Czysty Rust **bez ani jednego crate'a**
(build samym `rustc`, binarka ~600 kB) + fallback w jednym pliku Pythona.
Zbudowany, żeby pokonać [rtk](https://github.com/rtk-ai/rtk) (61k★) — i wygrywa
w benchmarkach: **86,6% vs 27,8% redukcji tokenów**, hook PreToolUse 2–5× szybszy,
dedup sesyjny, którego rtk nie ma, CI na trzech systemach. Całość powstała
w jednej sesji Claude Code na telefonie (Termux), a wynik potwierdziły m.in.
pojedynki bliźniaczych subagentów na żywym kodzie.

![Token savings — tok vs rtk](https://raw.githubusercontent.com/gangg111/tok/main/assets/bench1.svg)

### [Lektor AI](https://github.com/gangg111/Lektor_AI) — polski lektor napędzany AI
Aplikacja desktopowa do syntezy mowy i dubbingu po polsku: TTS + klonowanie głosu
(RVC przez onnxruntime), **pętla gwarancji zgodności tekstu** (generuj → transkrybuj
ASR → porównaj CER z polską normalizacją liczebników i godzin → regeneruj),
profesjonalna głośność (EBU R128) i miks z tłem filmu. Dystrybucja jako frozen
build z dociąganymi paczkami GPU (CUDA / onnxruntime-gpu) — działa od strzału,
bez instalowania Pythona.

### [RP2350 UART Crash Diagnostics](https://github.com/gangg111/RP2350-UART-Crash-Diagnostics)
System diagnostyczny HardFault dla Raspberry Pi Pico 2 — przechwytuje stan
rejestrów przy awarii i wypycha go po UART, zanim rdzeń zdąży umrzeć na dobre.
`C++ · Pico SDK`

### [ESP32 Bluetooth Audio Receiver](https://github.com/gangg111/ESP32-Bluetooth-Audio-Receiver)
Odbiornik audio Bluetooth na ESP32 — embedded spotyka audio także po stronie sprzętu.

### [awesome-ai-voice](https://github.com/gangg111/awesome-ai-voice)
Kurowana lista narzędzi AI do głosu — TTS, klonowanie, konwersja, ASR.

---

## 🛠️ Stack techniczny

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-1a1a1a?style=for-the-badge&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Verilog](https://img.shields.io/badge/Verilog-FPGA-orange?style=for-the-badge)
![Raspberry Pi](https://img.shields.io/badge/RP2350-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white)
![Espressif](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![Qt](https://img.shields.io/badge/PySide6-41CD52?style=for-the-badge&logo=qt&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX_Runtime-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=for-the-badge&logo=ffmpeg&logoColor=white)
![KiCad](https://img.shields.io/badge/KiCad-314CB0?style=for-the-badge&logo=kicad&logoColor=white)

- **Hardware:** RP2350 (Pico 2), ESP32, Tang Nano (FPGA), własne PCB
- **Software:** C++, Rust (zero-dependency), Python, Verilog
- **AI/audio:** RVC, ASR/Whisper, pyloudnorm, PyInstaller + paczki runtime GPU
- **Warsztat:** Claude Code, Gemini/Antigravity, GitHub Actions

---

## 📊 GitHub w liczbach

<div align="center">

![Statystyki](https://github-readme-stats.vercel.app/api?username=gangg111&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117)
![Języki](https://github-readme-stats.vercel.app/api/top-langs/?username=gangg111&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&langs_count=8)

</div>

---
*Na warsztacie: **n64_pico** — śledź postępy!*
