
# MEP-AUTOCAD-Scripts

A collection of AutoLISP scripts developed to streamline common MEP drafting tasks in AutoCAD. This includes automatic device tagging and sprinkler layout generation with customizable parameters.

---

## 📁 Scripts Included

### 1. `TagDevices.lsp` – Auto Device Tagger
Automates the process of tagging MEP devices in AutoCAD.

#### 🔧 Features:
- Automatically detects block name (e.g., SD, MD, HD, etc.).
- Inserts MTEXT tags under each selected device.
- Tag format: `Loop/DeviceType-Number-Floor` (e.g., `L1/SD-1-GF`)
- Supports:
  - Custom loop (`L1`, `L2`, etc.)
  - Custom floor (`GF`, `1F`, etc.)
  - Auto-incrementing device numbers
  - Manual reset of counter (`ResetTagCount`)
- Remembers last used loop and floor for ease of use.
- Skipped or previously tagged devices don’t break numbering.

#### 📌 Usage:
1. Load the script with `APPLOAD`.
2. Type `TagDevices` in the command line.
3. Select blocks → Tags will be placed below each block.

---

### 2. `SprinklerLayout.lsp` – Auto Sprinkler Layout
Auto-generates sprinkler layout grids based on user-defined dimensions and spacing.

#### 🔧 Features:
- Accepts custom area dimensions (length, width).
- Accepts custom spacing (X and Y direction).
- Automatically inserts `Sprinkler` blocks in grid.
- User provides reference point **inside the drawing**, blocks are inserted relative to it (suggested 5ft by 5ft margin from top).
- Ensures correct spacing between each block.

#### 📌 Usage:
1. Load the script with `APPLOAD`.
2. Type `SprinklerLayout` in the command line.
3. Enter:
   - Length of the area
   - Width of the area
   - Horizontal and vertical spacing
4. Click on the **insertion point inside drawing** for grid reference.
5. Sprinkler blocks will be inserted accordingly.

---

## 📘 Requirements

- AutoCAD 2020 or later (tested)
- AutoLISP support

---

## 🚀 Getting Started

1. Open AutoCAD
2. Load `.lsp` files using `APPLOAD`
3. Run the commands:
   - `TagDevices` for tagging
   - `ResetTagCount` to reset count
   - `SprinklerLayout` for layout generation

---

## 🧠 Author

**Hassin Arman**  
Intern MEP Engineer | AutoCAD Automation Enthusiast

---

## 📝 License

Free to use and modify.
