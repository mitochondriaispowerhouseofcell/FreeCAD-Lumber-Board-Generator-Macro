# 🪵 FreeCAD Lumber Board Generator Macro

This FreeCAD macro helps you create dimensional lumber boards with real-world standard or custom measurements. Perfect for woodworking mockups, planning framing layouts, or learning parametric CAD workflows.

## 📐 Features

- Select common dimensional lumber sizes (2x4, 4x4, etc.)
- Specify **custom dimensions** for thickness, width, and length
- Parse input in **inches, feet/inches, or fractional inches** (e.g., `8'`, `96"`, `6' 1 1/2"`)
- Specify how many boards to generate
- Stacks boards automatically in 3D space
- Fully parametric modeling using FreeCAD and Part workbench

## 📦 Supported Sizes

By default, the following nominal lumber sizes are available:

| Nominal Size | Actual Dimensions (inches) |
|--------------|----------------------------|
| 2x4          | 1.5 x 3.5                  |
| 2x6          | 1.5 x 5.5                  |
| 2x8          | 1.5 x 7.25                 |
| 2x10         | 1.5 x 9.25                 |
| 2x12         | 1.5 x 11.25                |
| 4x4          | 3.5 x 3.5                  |
| 4x6          | 3.5 x 5.5                  |
| 4x8          | 3.5 x 7.25                 |
| 6x6          | 5.5 x 5.5                  |
| 6x8          | 5.5 x 7.25                 |

You can override any of these with your own custom values.

---

## 🚀 Getting Started

### 1. Install FreeCAD
You’ll need [FreeCAD](https://www.freecad.org/downloads.php) version 0.19 or newer.

### 2. Download the Macro
Download the macro file from this repository:

> [`LumberBoardGenerator.FCMacro`](./LumberBoardGenerator.FCMacro)

Save it to your FreeCAD macro directory. You can find this directory in FreeCAD via:

### 3. Run the Macro
1. Open FreeCAD
2. Click `Macro → Macros...`
3. Select `LumberBoardGenerator.FCMacro` from the list
4. Click **Execute**

This will open the dialog window.

---

## 🛠️ Usage Guide

### Step-by-step:

1. **Select a Standard Size** – Choose from 2x4, 4x4, etc.
2. **(Optional)** Enter custom thickness or width (in inches or fractions)
3. **(Optional)** Enter custom length (supports `8'`, `96"`, or `6' 1/2"`)
4. **Set Quantity** – Number of boards to create
5. Click **"Add Lumber Board"** – Adds the specified number of boards to the scene
6. Click **Finish** to close the dialog

### Units and Format

- Inches: `96"`  
- Feet: `8'`  
- Feet and inches: `8' 3"` or `6' 1 1/2"`  
- Fractions supported: `3 1/4"`, `1/2"`, etc.

---

## 💡 Example Use Case

You’re planning to build a raised garden bed and want to mock up:

- Four 2x6x8' planks for the sides
- Two 4x4x1' posts for the corners

Open the macro and:

- Select `2x6`, set length `8'`, quantity `4`
- Then switch to `4x4`, set custom length `1'`, quantity `2`

You now have a full model of your materials ready to measure or export!

---

## ⚙️ Behind the Scenes

This macro uses:

- `Part.makeBox()` to generate parametric solid boards
- Conversion of user input into inches, then mm (FreeCAD's working unit)
- A small vertical gap (`+0.1 mm`) between stacked boards to keep them separate

If no document is open, the macro will auto-create a new one.

---

## 🧑‍💻 Contributing

Have an idea? Want to add more standard sizes, add labels, or export to spreadsheet?

1. Fork the repo
2. Make your changes
3. Submit a Pull Request

This macro is beginner-friendly and open to collaboration.

---

## 🧾 License

This project is licensed under the MIT License – do whatever you want, just don’t blame me if you make a janky shed. 😄

---

## 👋 Author

**@JodiRayTech**  
New to GitHub, CAD scripting, and automation — learning one macro at a time.  
Mainly building tools for FreeCAD.

---

## 🪚 Fun Fact

A “2x4” isn’t actually 2 inches by 4 inches. The macro knows that and uses **real-world dimensions**, not nominal ones. Take that, lumberyard lies. 😤

