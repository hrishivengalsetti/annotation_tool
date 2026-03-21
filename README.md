
# 🖼️ Image Annotation Tool

> A desktop-grade annotation tool built for modern computer vision workflows — fast, flexible, and actually pleasant to use.

---

## 🌟 Overview

This is a **PyQt5-based image annotation tool** designed for building high-quality datasets for computer vision tasks.

It supports precise bounding box annotation, multi-format dataset export (YOLO, COCO), and goes further with **built-in augmentation pipelines** and **AI-powered 3D view generation**.

If you're working on ML models and tired of clunky tools — this one’s built to feel smoother.

---

## 🚀 Key Features

### 🎯 Annotation Engine

* Draw, resize, drag, and delete bounding boxes interactively
* Smooth canvas interactions with real-time updates
* Undo / Redo support for safe editing

### 🔄 Dataset Compatibility

* Import & export in:

  * YOLO
  * COCO
  * Custom TXT
* Export visualized annotations for quick verification

### 🧪 Data Augmentation

* Built-in augmentation pipeline:

  * Flips, rotations, zoom
  * Brightness & noise adjustments
  * Translations

### 🧠 AI-Powered 3D View Generation

* Generate alternate perspectives using the **Replicate API**
* Useful for dataset expansion without manual effort

### 🏷️ Class Management

* Create and manage annotation classes
* Automatic color assignment
* Fast switching while annotating

### 🔍 Canvas Controls

* Zoom in/out
* Fit-to-screen
* Precision editing with mouse controls

### ⚡ Performance & Stability

* Memory monitoring using `psutil`
* Handles large datasets without crashing

---

## 🛠 Tech Stack

* **Language:** Python 3.x
* **GUI:** PyQt5
* **Computer Vision:** OpenCV, NumPy, Pillow
* **Utilities:**

  * `psutil` (memory management)
  * `requests` (API calls)
  * `PyYAML` (config handling)

---

## 🧱 Architecture

The project is modular and cleanly separated:

```bash
annotation_tool-main/
│
├── main.py              # Entry point (app setup, logging, error handling)
├── ui_mainwindow.py     # Main UI and user interaction layer
├── annotation_canvas.py # Core annotation logic (drawing, editing, undo/redo)
├── annotation_io.py     # Import/export, augmentation, API integration
├── image_loader.py      # Image loading utilities
└── rework/              # Experimental/refactor work
```

### Core Components

* **Canvas Engine** → Handles all drawing + interaction
* **IO Layer** → Formats, augmentation, dataset export
* **UI Layer** → User flow, dialogs, toolbars
* **System Layer** → Memory + error handling

---

## ⚙️ Installation

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/image-annotation-tool.git
cd image-annotation-tool
```

---

### 2. Setup environment (recommended)

```bash
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
```

---

### 3. Install dependencies

```bash
pip install PyQt5 opencv-python numpy psutil Pillow PyYAML requests
```

---

## ▶️ Usage

### Launch the app

```bash
python main.py
```

---

### Workflow

1. **Load Images**

   * Click *Select Image Folder*

2. **Create Classes**

   * Add labels in the Class Panel

3. **Annotate**

   * Click + drag to draw bounding boxes
   * Resize using corners
   * Move by dragging

4. **Augment (Optional)**

   * Use *Create Augmentations*

5. **3D Generation (Optional)**

   * Requires Replicate API token

6. **Export Dataset**

   * Choose format → Export

---

## ⌨️ Shortcuts

| Action         | Shortcut   |
| -------------- | ---------- |
| Save           | `Ctrl + S` |
| Undo           | `Ctrl + Z` |
| Redo           | `Ctrl + Y` |
| Zoom In        | `+` / `=`  |
| Zoom Out       | `-`        |
| Fit Screen     | `F`        |
| Next Image     | `→`        |
| Previous Image | `←`        |
| Delete Box     | `Delete`   |

---

## 🔐 Environment

* **Replicate API Token**

  * Required only for 3D generation
  * Entered dynamically via UI (no `.env` needed)

---

## 🔮 Roadmap

* Polygon / segmentation annotations
* Auto-labeling (Segment Anything / foundation models)
* Project/session saving
* Dark mode UI

---

## 🤝 Contributing

```bash
git checkout -b feature/your-feature
git commit -m "Add feature"
git push origin feature/your-feature
```

Then open a PR — simple as that.

---

## 📄 License

MIT License — use it, break it, improve it.

---

## 🧠 Notes

* Designed for **computer vision dataset creation workflows**
* Optimized for usability + performance balance
* Architecture keeps UI and logic cleanly separated 
