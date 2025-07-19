# DeviceTagger-AUTOCAD
AutoCAD Device Tagger automates labeling of device blocks like SD, MD, etc., with tags in the format L1/SD-1-GF. It auto-detects device types, increments numbering, places MTEXT below each device, and supports custom loop/floor settings with resume and reset features.
# AutoCAD Device Tagger

## 📌 Overview

AutoCAD Device Tagger is a productivity-enhancing AutoLISP script for AutoCAD. It automates the placement of formatted device tags (like `L1/SD-1-GF`) below selected device blocks such as Smoke Detectors (SD), Manual Detectors (MD), and others.

## ✨ Features

- 🔄 **Auto-Increment Tags**: Automatically numbers tags (e.g., SD-1, SD-2).
- 🔍 **Auto-Detect Device Type**: Extracts type (SD, MD, etc.) from block names.
- ✏️ **Custom Loop/Floor**: Set loop (L1, L2...) and floor (GF, 1F...) before tagging.
- 📍 **Precise Tag Placement**: Places MTEXT neatly below each device.
- 🧠 **Smart Resume**: Continues count properly even after skipping or re-running.
- 🛠️ **Manual Reset**: Reset floor/loop or numbering at any time.

## 🚀 Getting Started

### ✅ Load the Script

1. Open AutoCAD.
2. Type `APPLOAD` and load `devicetagger.lsp`.

### 🏷️ Run the Tagger

1. Type `DEVICETAG` in the command line.
2. Select the devices (blocks) you want to tag.
3. Enter:
   - Loop ID (e.g., `L1`)
   - Floor ID (e.g., `GF`)
4. The script places tags like: `L1/SD-1-GF`, `L1/SD-2-GF`, ...

### 🔁 Reset Count (if needed)

- Use `RESETTAGCOUNT` to restart numbering from 1 (if implemented).
- Or reload the script to start fresh.

## 📂 File Structure

AutoCAD-Device-Tagger/
│
├── devicetagger.lsp # Main tagging script
├── README.md # Project documentation
├── .gitignore # Git ignore rules

shell
Copy
Edit

## 📄 Tag Format

<LOOP>/<DEVICE_TYPE>-<NUMBER>-<FLOOR>
Example: L2/MD-3-1F

markdown
Copy
Edit

## ⚠️ Requirements

- AutoCAD 2020 or later
- Block names must clearly contain device types (e.g., `SD`, `MD`)

## 🧪 Example Use Case

You select 5 `SD` blocks and 2 `MD` blocks.  
With loop = `L1`, floor = `GF`, it will place:

L1/SD-1-GF
L1/SD-2-GF
...
L1/MD-1-GF
L1/MD-2-GF

yaml
Copy
Edit

## 📧 Support

For support or feature requests, contact the script developer.

---

© 2025 Hassin Arman. All rights reserved.
