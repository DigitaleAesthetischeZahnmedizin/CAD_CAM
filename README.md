# 🦷 CAD_CAM – 3D Tooth Visualization

**English** | [Deutsch](README.de.md)

Browser-based tool for **visualizing and measuring 3D tooth models** (STL/PLY).
The application runs directly in the browser via GitHub Pages — no installation required.

**Live application:** https://digitaleaesthetischezahnmedizin.github.io/CAD_CAM/

---

## Table of contents

- [Preview](#preview)
- [Purpose](#purpose)
- [Features](#features)
- [Repository structure](#repository-structure)
- [Quick guide: performing a measurement](#quick-guide-performing-a-measurement)
- [Third-party libraries / license notices](#third-party-libraries--license-notices)
- [License](#license)
- [Notes & disclaimer](#notes--disclaimer)
- [Clinical documentation](#clinical-documentation)

> 📖 The full user manual with screenshots is in **[`doc/README.md`](doc/README.md)**.

---

## Preview

A few impressions of the tool in use — deviation heatmap, distance measurement, section measurement, and a textured model:

![Distance measurement with pins](media/tool/Measurement1.png)
*Distance measurement (pins) on the target model.*

![Distance measurement with pins — overlay view](media/tool/Measurement2.png)
*Distance measurement (pins) — reference and target overlaid.*

![Deviation heatmap](media/tool/Heatmap1.png)
*Deviation heatmap (signed) with measurement pins.*

![Deviation heatmap — detailed view](media/tool/Heatmap2.png)
*Deviation heatmap (signed) — detailed view.*

![Section measurement](media/tool/Section_measurement.png)
*Section measurement (2D cut) along the cutting plane.*

![Textured PLY model](media/tool/Textur_PLY.png)
*Textured PLY model — tooth models placed within a face scan.*

---

## Purpose

The program provides **objective visualization and measurement** of changes to teeth based on
digital 3D scans from different treatment phases (e.g. before and after a preparation, as well as
with restorations in place).

It is used in the context of an **independent procedure for the taking of evidence**
("selbständiges Beweisverfahren", §§ 485 et seq. of the German Code of Civil Procedure, ZPO)
concerning an **alleged / disputed** veneer treatment fault at a dentist in Heilbronn, Germany. One of the
disputed points is whether the restorations are to be classified as veneers or as partial crowns.
The application serves solely to illustrate the technical aspects of the matter in dispute.

> **Note:** This is party documentation for illustration purposes only. The final professional and
> legal assessment rests solely with the court-appointed expert and the court. This presentation
> does **not** constitute any final or binding determination of a treatment error.

---

## Features

- **Load models** – STL/PLY via web link or local file; optional texture (JPG) for PLY models.
- **Display settings** – scale, FOV, background color, grid, camera position (X/Y/Z).
- **Deviation heatmap** – signed color scale (±4 mm) comparing a reference and a target model.
- **Tolerance bands** – adjustable green range, yellow/red and light-blue/dark-blue ranges, maximum threshold.
- **Mouse measurement (pins)** – point-to-surface distances with adjustable point size.
- **Iterative high-precision measurement** ("Sun/Fan") – rays per step, iterations, line-of-sight check to skip gaps.
- **2D cross-section measurement** – clipping plane for precise edge measurement.
- Multilingual interface and light/dark mode.

---

## Repository structure

| File / folder | Contents |
| --- | --- |
| `index.html` | The complete web application (3D viewer & measurement). |
| `STL/` | The 3D models used for comparison. |
| `doc/` | User manual with numbered screenshots (see below). |
| `media/` | Tool screenshots and clinical case images/video shown in this README. |

📖 **Documentation:** A detailed user manual is available in **[`doc/README.md`](doc/README.md)**.

---

## Quick guide: performing a measurement

The following steps are required to perform a distance measurement between two models:

1. Open the web page.
2. Wait until all models have loaded (status at the bottom of the sidebar).
3. In the "Loaded models" section: set one model as "reference" and another as "target".
4. In the "STL/PLY comparison" section: click "Prepare measurement".
5. Activate "Mouse measurement (pins)" — distances are now shown when hovering over the target model.
6. Click on the model to place measurement points (pins).
7. Optional: activate "Show heatmap" for an area-wide deviation display.
8. Optional: use the section measurement for exact 2D cut measurements.

**Keyboard shortcuts**

- **ESC** — deactivate mouse measurement and cutting-plane drawing
- **Mouse wheel** — zoom
- **Left mouse button + drag** — rotate the model
- **Right mouse button + drag** — pan the model

---

## Third-party libraries / license notices

The following open-source libraries are loaded at runtime via the jsDelivr CDN (they are **not**
included in this repository) and remain under their own licenses:

- **three.js** (v0.172.0) – MIT License – © three.js authors – https://github.com/mrdoob/three.js
  (including the `OrbitControls`, `STLLoader`, `PLYLoader` modules)
- **three-mesh-bvh** (v0.9.8) – MIT License – © Garrett Johnson – https://github.com/gkjohnson/three-mesh-bvh
- **Fonts** *DM Sans* and *JetBrains Mono* (SIL Open Font License) – loaded via Google Fonts

---

## License

The **project's own code and content** are licensed under the
**Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.
See the [`LICENSE`](LICENSE) file for the full terms.

This means the application may be shared with attribution, but may **not be modified** and
**not be used commercially**.
License text: https://creativecommons.org/licenses/by-nc-nd/4.0/

> This license applies only to this project's own code. The libraries listed above
> (three.js, three-mesh-bvh) remain under their respective MIT licenses.

---

## Notes & disclaimer

- Purely a **visualization and measurement tool** — **not a medical device**, not a diagnosis, and not a treatment recommendation.
- Measurement and heatmap results depend on the quality, resolution, and alignment (registration) of the input data.

---

## Clinical documentation

> The following images document the individual case (the patient's own records). Personal metadata
> (EXIF/GPS, device and timestamp information) has been removed from all files.

### Initial situation

![Natural teeth before treatment](media/clinical/Image_Natural_Teeth_Before.png)
*Initial situation — natural teeth before treatment.*

### After preparation

![After preparation 1](media/clinical/Image_After_Preparation1.png)
*After preparation (1).*

![After preparation 2](media/clinical/Image_After_Preparation2.png)
*After preparation (2).*

### Result

![Result 1](media/clinical/Image_Result1.png)
*Result — restorations in place (1).*

![Result 2](media/clinical/Image_Result2.png)
*Result — restorations in place (2).*

![Result 3](media/clinical/Image_Result3.png)
*Result — restorations in place (3).*

### Radiographs

![Panoramic radiograph before](media/clinical/OPG_Before.png)
*Panoramic radiograph (OPG) — before.*

![Panoramic radiograph after](media/clinical/OPG_After.png)
*Panoramic radiograph (OPG) — after.*

![Periapical radiograph region 11](media/clinical/Roe_11.png)
*Periapical radiograph — region 11.*

![Periapical radiograph region 13](media/clinical/Roe_13.png)
*Periapical radiograph — region 13.*

![Periapical radiograph region 23](media/clinical/Roe_23.png)
*Periapical radiograph — region 23.*

### Intraoral close-ups

![Intraoral close-up region 11](media/clinical/Endoscope_11.png)
*Intraoral close-up — region 11.*

![Intraoral close-up region 12](media/clinical/Endoscope_12.png)
*Intraoral close-up — region 12.*

![Intraoral close-up region 13](media/clinical/Endoscope_13.png)
*Intraoral close-up — region 13.*

![Intraoral close-up region 21](media/clinical/Endoscope_21.png)
*Intraoral close-up — region 21.*

![Intraoral close-up region 22](media/clinical/Endoscope_22.png)
*Intraoral close-up — region 22.*

![Intraoral close-up region 23](media/clinical/Endoscope_23.png)
*Intraoral close-up — region 23.*

### Video

<a href="media/clinical/Endoscope_Video.mp4"><img src="media/clinical/Video_Thumbnail.png" width="480" alt="Intraoral video — click to play"></a>

*Intraoral video — click the image to open and play it.*
