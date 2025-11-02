# Pocket G‑Code Generator (GUI)

A lightweight **Tkinter** app to generate safe, layered **pocketing G‑code** for CNC routers (tested with **WinPC‑NC / Stepcraft**). Supports single‑hole entry and **batch CSV import**, with built‑in validation, concentric passes, optional finish passes, live statistics, and WinPC‑NC‑friendly output.

> **Safety first**: Always do a dry run above the material and verify toolpaths before cutting.

---

## ✨ Features
- Clean **Tkinter** GUI (no external deps)
- **Concentric pocket** toolpaths with configurable *stepdown*, *stepover*, *feeds*, *spindle*, *dwell*
- Optional **finish passes** (leave stock, then final radius)
- **CSV batch import** (`X, Y, Diameter, Depth`) with range checks
- **Stats**: holes / layers / passes
- **Profiles**: save/load machining parameters (JSON)
- **WinPC‑NC** friendly output (G21 G90 G17 G94 G54, `M3/M5`, arc `G3` with IJ)
- **Logging** to `logs/`Amir Mobasheraghdam

---

## 🖼️ Screenshots
*(Place your screenshots in `docs/` and link them here)*

---

## 📦 Installation
- **Windows / macOS / Linux** with **Python 3.9+**
- Tkinter ships with most Python builds (on Windows/macOS). On some Linux distros install: `sudo apt-get install python3-tk`

```bash
# clone repo
git clone https://github.com/<your-user>/pocket-gcode-generator.git
cd pocket-gcode-generator

# (Optional) create venv
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# No external deps needed
python main.py
