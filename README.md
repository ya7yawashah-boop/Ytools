YTOOLS Py

Free, open-source pyRevit extension for Autodesk Revit — built by a BIM Manager for real production work in the Middle East.

YTOOLS Py brings together tools that usually need paid add-ins: coordination checks, model transfer, model comparison, quantities and documentation helpers. They all run on one shared core.

Features

Coordinate

• Clash Detection: Side A / Side B categories across the model and links, presets, and a review workflow. An early check inside Revit before the formal Navisworks/Revizto cycle.
• Opening Engine: places openings and sleeves where services actually cross hosts, with an editable preview grid.
• IFC to Topography: turns IFC geometry into a Revit Toposolid.

Transfer

• Transfer Pro: transfers elements and annotations between documents and links, with a dry-run preview, per-target transactions and a history log.
• Transfer Standards: copies views, sheets, types and families between open projects.
• Transfer View Elements: copies everything visible in a view to another project.
• Import Mesh JSON: rebuilds 3ds Max / SketchUp exports in Revit with their per-face materials.

Model

• Project to Template: strips placed elements, links and CAD imports, and keeps the standards so you can save the file as a template.
• In-Place to Family: converts in-place elements into loadable families.

Select

• Save Selection: saves the current selection to a project or family file.
• Select by Parameters: Fast mode (pick, choose, select) and Advanced builder mode.

Annotate

• Area Schedule: area tables from picked points or rectangles.
• Sum Text: adds up numeric text notes.

YTOOLS Hub

Shows the version, run and error counts per tool, a log viewer, environment info, and a reset for stored settings.

Requirements

• Autodesk Revit 2024 or newer
• pyRevit 6.5+ (pyRevit 7 recommended)

Installation

1. Download this repository (Code → Download ZIP) and extract it.
2. Copy the YTOOLS.extension folder to:
%APPDATA%\pyRevit\Extensions\
3. Restart Revit, or press pyRevit → Reload.
4. The YTOOLS Py tab appears in the ribbon.

Or install it with the pyRevit CLI:

pyrevit extend ui YTOOLS https://github.com/ya7ya95/YTOOLS-Py.git

Project structure

YTOOLS.extension/
├── YTOOLS Py.tab/        # Ribbon tab, panels and buttons
└── lib/
    ├── ytools_core.py    # Error trap, logging, transactions, units, settings, reports
    └── ytools_theme.py   # Shared dark UI theme

Each button is a one-line script.py launcher plus a _tool.py body, so every tool gets the same error reporting and logging.

Roadmap

• Model Compare: detect deleted, modified and moved elements, then transfer selected changes
• BWIC openings from MEP models, with revision sync
• View-template and graphic-standards QA for every discipline
• Arabic documentation

Contributing

Issues and pull requests are welcome. Please test on a copy of a model first, never on live project files.

Credits

The Area Schedule and Sum Text tools were inspired by classic AutoCAD LISP routines by Maha Odeh (AREA_SCH, 1998) and Eng. Saad Abduljaleel Albdeiri (sum.LSP, 1994).

License

MIT © 2026 Yahya Washah