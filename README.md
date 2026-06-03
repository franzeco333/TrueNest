# TrueNest

![TrueNest logo](assets/logo/TrueNest.svg)

**TrueNest** is an experimental real nesting tool for laser cutting workflows. It is designed to import vector artwork prepared in SVG / Adobe Illustrator-style workflows, arrange real shapes inside custom work areas, and export clean SVG files for RDWorks. Windows is the first test platform, with macOS support planned.

> Current status: technical beta. The project is not production-ready yet.

## What TrueNest is trying to solve

Many laser workflows use Illustrator, CorelDRAW, SVG, DXF, EPS or similar vector formats before importing files into RDWorks. TrueNest aims to become a lightweight nesting tool that can:

- import vector shapes from SVG files;
- detect real closed shapes, including compound paths with holes;
- distinguish figures from work areas;
- place shapes inside irregular work areas, not just rectangles;
- respect spacing between pieces and work area margins;
- export a clean RDWorks-compatible SVG;
- generate a PNG preview and a TXT report for traceability.

## Current workflow

```text
Adobe Illustrator / vector editor
→ export SVG
→ TrueNest beta
→ clean SVG output
→ RDWorks
```

## Current beta capabilities

The latest beta can:

- read SVG files;
- detect colors using TrueNest import rules;
- use a red work area and black figures as a temporary convention;
- apply real geometry validation using Shapely;
- apply 3 mm spacing logic as 1.5 mm offset per figure and 1.5 mm internal work area margin;
- choose a starting direction using a 3x3 grid;
- use horizontal, vertical, diagonal, or center-style search behavior;
- generate a clean SVG for RDWorks, a PNG preview, and a TXT report.

## Requirements for current beta scripts

The current test scripts use Python.

### Windows 7

Use Python **3.8.10**.

Official download page:

https://www.python.org/downloads/release/python-3810/

Recommended installers:

- Windows 64-bit: `python-3.8.10-amd64.exe`
- Windows 32-bit: `python-3.8.10.exe`

During installation, enable:

```text
Add Python 3.8 to PATH
```

### Dependencies

The beta uses:

```text
shapely==1.8.5.post1
svgpathtools==1.6.1
Pillow==9.5.0
```

The beta ZIPs include a `.bat` installer for these dependencies.

## Platform plans

TrueNest is planned as one project with builds for multiple platforms:

```text
Windows build: planned
macOS build: planned
```

The repository should remain shared; platform-specific builds can be published separately in GitHub Releases.

## Project language

The repository is documented in English and Spanish. The current prototype UI is mostly Spanish, because it began as a production workflow tool for Francisco Núñez Parra. Future versions should support language files, such as:

```text
locales/es.json
locales/en.json
```

and optionally detect the operating system language.

---

# TrueNest en español

**TrueNest** es una herramienta experimental de nesting real para flujos de corte láser. Está pensada para importar arte vectorial preparado desde SVG / Adobe Illustrator, acomodar figuras reales dentro de mesas de trabajo personalizadas y exportar SVG limpio compatible con RDWorks. Primero se está probando en Windows, con soporte para macOS planeado.

> Estado actual: beta técnica. Todavía no es una versión final de producción.

## Objetivo

TrueNest busca resolver el nesting de figuras reales para corte láser:

- importar SVG;
- detectar figuras cerradas;
- detectar figuras compuestas con hoyos;
- diferenciar figuras y mesas de trabajo;
- acomodar piezas dentro de mesas irregulares;
- respetar separación entre figuras y márgenes;
- exportar SVG limpio para RDWorks;
- generar preview PNG y reporte TXT.

## Créditos

Created by / Creado por:

**Francisco Núñez Parra**

Technical assistance and code generation support / Asistencia técnica y generación de código:

**ChatGPT / OpenAI**
