# Fusion 360 Gear Assembly & Contact Motion Study

A complete Fusion 360 mechanical workflow — from scratch part modeling to physical contact-driven gear rotation — demonstrating how to simulate **real power transmission** without relying on motion links.

**By: Dr. Ankit Chauhan** ([@BuildsByDrAnkit](https://github.com/BuildsByDrAnkit))

---

## 📸 Project Visuals

![Gear Train Motion](Media/gear_motion.gif)

*Static assembly views:*

![Top View](Media/assembly_top_view.png)
![Isometric View](Media/assembly_iso_view.png)

---

## 📐 Gear Specifications

| Parameter | Driver Gear | Driven Gear |
|---|---|---|
| Type | Spur Gear | Spur Gear |
| Number of Teeth | 12 | 12 |
| Gear Ratio | 1:1 | — |
| Rotation Direction | Clockwise | Counter-Clockwise |
| Joint Type | Revolute | Revolute |
| Units | mm, g | mm, g |
| Software | Autodesk Fusion 360 | Autodesk Fusion 360 |

---

## 💡 Why Contact Sets — Not Motion Links?

Most Fusion 360 gear tutorials use **Motion Links** to rotate gears together. Motion Links are purely mathematical — they ignore actual geometry and allow gears to clip and pass through each other unrealistically.

This project uses **Contact Sets** instead:

- ✅ Gears interact based on actual tooth geometry
- ✅ No clipping or tooth phase errors
- ✅ Realistic power transmission simulation
- ✅ Motion Study reflects true physical behavior
- ✅ Driver gear physically pushes the driven gear — just like in the real world

---

## ⚙️ Workflow & Features

This project was built from scratch in Fusion 360 to test physical interactions between rotating components. The complete workflow:

**1. Part Creation**
Modeled individual components including a 12-tooth driver spur gear, a 12-tooth driven spur gear, and their respective mounting shafts — all built from sketch to solid in Fusion 360.

**2. Mechanical Assembly**
Mounted the gears to the shafts and organized components in the Fusion 360 assembly workspace.

**3. Revolute Joints**
Applied Revolute Joints to both gear-shaft pairs to establish the correct single rotational degree of freedom for each axis.

**4. Contact Sets**
Enabled physical Contact Sets between the gear teeth to prevent clipping and simulate real-world power transmission. This is the key step that separates this workflow from motion-link-based tutorials.

**5. Motion Study**
Configured a time-based Motion Study (MotionStudy-1) to drive the primary shaft and analyze the 1:1 gear ratio interaction — verifying smooth, contact-driven rotation throughout the full cycle.

---

## ▶️ How to View the Motion Study

1. Download and open the `.f3d` file from `CAD/fusion/` in **Autodesk Fusion 360**
2. In the browser tree on the left, expand the **Motion Studies** folder
3. Double-click **MotionStudy-1**
4. Press the **Play** button in the pop-up timeline to watch the contact-driven rotation

> 💡 **Don't have Fusion 360?** Download the free personal use version at [autodesk.com/fusion](https://www.autodesk.com/products/fusion-360/personal). The `.step` files in `CAD/parts/` and `CAD/assembly/` can be opened in any CAD tool (FreeCAD, SolidWorks, Onshape, CATIA, build123d).

---

## 📂 Repository Structure

```
fusion360-gear-assembly-contact-motion-study/
│
├── README.md
│
├── CAD/
│   ├── parts/
│   │   ├── driver_Spur_Gear_12teeth.step
│   │   ├── driven_Spur_Gear_12teeth.step
│   │   ├── driver_shaft.step
│   │   └── driven_shaft.step
│   ├── assembly/
│   │   └── simple_gear_train.step
│   └── fusion/
│       └── simple_gear_power.f3d
│
└── Media/
    ├── assembly_top_view.png
    ├── assembly_iso_view.png
    └── gear_motion.gif
```

---

## 📦 File Format Guide

| Format | Contains | Best Used For |
|---|---|---|
| `.f3d` (Fusion Archive) | ✅ Everything — joints, contacts, motion study, sketches | Reopening & editing in Fusion 360 |
| `.step` | Solid geometry only | Importing into any CAD tool (SolidWorks, FreeCAD, CATIA, build123d) |
| `.stl` | Mesh only, no assembly data | 3D printing |
| `.obj` | Mesh only | Rendering / game engines |

> ⚠️ **Note:** STEP files contain universal solid body geometry — great for cross-platform CAD use. However, they do **not** retain Fusion 360 joint data, contact sets, or motion studies. To view the working motion study, open the native `.f3d` file in Fusion 360.

---

## 🚀 How to Use

**To view the geometry in any CAD tool:**
1. Clone or download this repository
2. Import any file from `CAD/parts/` or `CAD/assembly/simple_gear_train.step` into your preferred CAD environment (Fusion 360, SolidWorks, FreeCAD, build123d, etc.)

**To view the full working assembly with motion study:**
1. Open Autodesk Fusion 360
2. Go to `File → Open → From my computer`
3. Select `CAD/fusion/simple_gear_power.f3d`
4. Navigate to `Motion Studies → MotionStudy-1` in the browser panel
5. Hit Play to see the contact-driven gear rotation

**To recreate the workflow from scratch:**
1. Model gears and shafts as individual components
2. Assemble in Fusion 360 using `Assemble → New Component`
3. Apply `Revolute Joints` to each gear-shaft pair via `Assemble → Joint`
4. Enable `Contact Sets` via `Assemble → Enable Contact Sets`, then add gear pairs
5. Create a Motion Study via `Assemble → Motion Study`
6. Set the driver joint angle over time and hit Play

---

## 🖥️ Requirements

- **Autodesk Fusion 360** — for `.f3d` file and motion study
- **Any CAD tool** — for `.step` files (FreeCAD, SolidWorks, CATIA, build123d, Onshape)
- No paid plugins or add-ons required

---

## 🗂️ GitHub Topics

> Add these topics to your repo for discoverability:
> `fusion360` `cad` `gear-train` `spur-gear` `mechanical-assembly` `contact-sets` `motion-study` `autodesk` `mechanical-engineering` `revolute-joint` `3d-modeling` `kinematics`

---

## 📄 License

This project is open-source and free to use for learning and personal projects.
Feel free to fork, adapt, and build on it — a credit back is always appreciated! 🙌

---

*Made with Fusion 360 · Shared for the CAD & engineering community*
