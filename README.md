# SLDMAT Editor

A browser-based editor for SolidWorks material library files (`.sldmat`). No installation, no build step — open the HTML file and go.

## Usage

Open the editor for your SolidWorks version:

- [SolidWorks 2025](https://sldmateditor.csankey.com/sldmat-editor.html?version=2025)

If no version is specified, the latest supported version is selected automatically: [open editor](https://sldmateditor.csankey.com/sldmat-editor.html)

To use offline, download `sldmat-editor.html` from this repo and open it in any modern browser — no server or internet connection required.

From the landing page:

- **Import .sldmat** — load an existing SolidWorks material library
- **Create New** — start a blank library from scratch

## Features

**Library management**
- Add, rename, delete, and merge categories
- Add, rename, duplicate, and delete materials
- Drag and drop materials between categories
- Multi-select materials with Ctrl+click (toggle) or Shift+click (range), then bulk delete
- Search/filter materials across all categories

**Material editing**
- Edit name, description, and all physical properties inline
- Add or remove individual properties per material
- Unit conversion built into every numeric field — enter a value in MPa, GPa, psi, etc. and it converts automatically to SI on save
- Edit cross-hatch pattern and swatch color

**File I/O**
- Outputs valid `.sldmat` XML with UTF-16 LE encoding and BOM, matching the format SolidWorks expects
- **Save** — re-downloads using the original filename
- **Save As** — prompts for a new name
- **Export** — same as Save As for newly created libraries

## Supported Properties

| Key | Property | Unit |
|-----|----------|------|
| EX / EY / EZ | Elastic modulus | N/m² |
| NUXY / NUXZ / NUYZ | Poisson's ratio | — |
| GXY / GXZ / GYZ | Shear modulus | N/m² |
| ALPX / ALPY / ALPZ | Thermal expansion coefficient | /K |
| DENS | Mass density | kg/m³ |
| KX / KY / KZ | Thermal conductivity | W/(m·K) |
| C | Specific heat | J/(kg·K) |
| SIGXT | Tensile strength | N/m² |
| SIGXC | Compressive strength | N/m² |
| SIGYLD | Yield strength | N/m² |
