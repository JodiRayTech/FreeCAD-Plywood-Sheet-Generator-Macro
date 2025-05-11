# 🪚 FreeCAD Plywood Sheet Generator Macro

This FreeCAD macro creates plywood sheet models with configurable dimensions and thickness, letting you quickly mock up real-world materials in your 3D workspace. It supports both **standard plywood sizes** and **custom widths, lengths, and thicknesses** entered in feet/inches or fractions.

## 📐 Features

- Choose from a list of **standard plywood panel sizes**
- Specify **custom width and length** in feet/inches (e.g. `4'`, `36"`, `3' 6"`)
- Select from **common plywood thicknesses** or enter a custom value
- Stack multiple copies of the same panel
- Converts everything to **millimeters** for FreeCAD compatibility
- Automatically adds plywood parts to the current or new document

---

## 📏 Built-in Sizes

The following standard plywood sheet sizes are included:

| Label | Width (in) | Length (in) |
|-------|------------|-------------|
| 4x8   | 48         | 96          |
| 4x4   | 48         | 48          |
| 3x8   | 36         | 96          |
| 3x6   | 36         | 72          |
| 2x8   | 24         | 96          |
| 2x6   | 24         | 72          |
| 2x4   | 24         | 48          |
| 1x8   | 12         | 96          |
| 1x6   | 12         | 72          |
| 1x4   | 12         | 48          |
| 1x3   | 12         | 36          |
| 1x2   | 12         | 24          |
| 1x1   | 12         | 12          |

---

## 🪵 Supported Thicknesses

Nominal plywood thicknesses and their actual sizes (in inches):

| Nominal | Actual Inches |
|---------|---------------|
| 1/8"    | 7/64"         |
| 1/4"    | 7/32"         |
| 3/8"    | 11/32"        |
| 1/2"    | 15/32"        |
| 5/8"    | 19/32"        |
| 3/4"    | 23/32"        |
| 1-1/8"  | 1.125"        |
| 1-1/4"  | 1.25"         |

Or you can enter a **custom thickness** using feet/inches format.

---

## 🚀 Getting Started

### 1. Install FreeCAD

Download the latest version from:  
👉 [https://www.freecad.org/downloads.php](https://www.freecad.org/downloads.php)

---

### 2. Download the Macro

Download the file [`PlywoodBoardGenerator.FCMacro`](./PlywoodBoardGenerator.FCMacro) and place it in your FreeCAD macros folder:

In FreeCAD:  
**Tools → Macros → Macros Folder**

---

### 3. Run the Macro

1. Open FreeCAD
2. Go to **Macro → Macros**
3. Select `PlywoodBoardGenerator.FCMacro`
4. Click **Execute**

---

## 🛠️ How to Use

### Fields:

- **Select Plywood Size**: Choose a preset, or leave blank to enter your own
- **Custom Width / Length**: Optional overrides; accepts `'6'`, `'36"'`, `'3' 6"'`
- **Thickness**: Choose from common values or enter a custom value (in ft/in format)
- **Quantity**: Number of identical sheets to create (they will stack)

---

### Input Format Examples

| Input Type      | Example       |
|-----------------|---------------|
| Inches          | `96"`         |
| Feet            | `8'`          |
| Feet + Inches   | `4' 6"`       |
| Fractions       | `2' 1 1/2"`   |
| Decimal Inches  | `12.5"`       |

---

### Output

- All parts are created as 3D `Part::Feature` boxes in the model
- Stacked vertically with 1 mm separation
- Units automatically converted to **millimeters**

---

## 🧪 Example Use Case

You want to mock up five 4x8 sheets of 3/4" plywood. Simply:

- Select `4x8` from the list
- Leave width/length blank
- Select `3/4"` as thickness
- Set Quantity = `5`

Hit **"Create Plywood Piece"**, and you're done!

---

## 🔒 Safety Notes

If no document is open, the macro will automatically create a new FreeCAD document named `"PlywoodSheets"`.

---

## 💬 Feedback or Contributions

Want to improve this? Found a bug? Feel free to fork the project, submit a pull request, or open an issue!

This macro is beginner-friendly and open for improvement.

---

## 📜 License

MIT License – free to use, modify, and distribute.

---

## 👋 Author

**@JodiRayTech**  
New to GitHub, CAD scripting, and automation — learning one macro at a time.  
Mainly building tools for FreeCAD.

---

## 🧠 Fun Fact

You *can* design an entire shed or shop wall using this macro — and it’s surprisingly accurate for layout planning!
