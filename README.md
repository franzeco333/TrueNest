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

![Logotipo de TrueNest](assets/logo/TrueNest.svg)

**TrueNest** es una herramienta experimental de nesting real para flujos de corte láser. Está pensada para importar arte vectorial preparado desde SVG / Adobe Illustrator, acomodar figuras reales dentro de mesas de trabajo personalizadas y exportar SVG limpio compatible con RDWorks. Primero se está probando en Windows, con soporte para macOS planeado.

> Estado actual: beta técnica. Todavía no es una versión final de producción.

## Qué problema busca resolver TrueNest

Muchos flujos de corte láser usan Illustrator, CorelDRAW, SVG, DXF, EPS u otros formatos vectoriales antes de importar los archivos en RDWorks. TrueNest busca convertirse en una herramienta liviana de nesting que pueda:

- importar figuras vectoriales desde archivos SVG;
- detectar figuras cerradas reales, incluyendo paths compuestos con hoyos;
- diferenciar figuras y mesas de trabajo;
- acomodar piezas dentro de mesas irregulares, no solo rectángulos;
- respetar separación entre piezas y márgenes de la mesa;
- exportar SVG limpio compatible con RDWorks;
- generar una imagen PNG de vista previa;
- generar un reporte TXT para dejar registro de la configuración usada.

## Flujo actual

```text
Adobe Illustrator / editor vectorial
→ exportar SVG
→ TrueNest beta
→ SVG limpio de salida
→ RDWorks
```

## Funciones actuales de la beta

La beta más reciente puede:

- leer archivos SVG;
- detectar colores usando las reglas de importación de TrueNest;
- usar una mesa roja y figuras negras como convención temporal;
- validar geometría real usando Shapely;
- aplicar separación de 3 mm como 1,5 mm de expansión por figura y 1,5 mm de margen interno de mesa;
- elegir una dirección inicial usando una cuadrícula 3x3;
- usar prioridad horizontal, vertical, diagonal o comportamiento de centrado;
- generar un SVG limpio para RDWorks;
- generar un PNG preview;
- generar un reporte TXT.

## Requisitos para usar las betas actuales

Los scripts actuales usan Python.

### Usuarios de Windows 7

Usar Python **3.8.10**.

Página oficial de descarga:

https://www.python.org/downloads/release/python-3810/

Instaladores recomendados:

- Windows 64 bits: `python-3.8.10-amd64.exe`
- Windows 32 bits: `python-3.8.10.exe`

Durante la instalación hay que activar:

```text
Add Python 3.8 to PATH
```

Si no se activa esa casilla, Windows puede mostrar un error parecido a:

```text
python no se reconoce como un comando interno o externo
```

### Dependencias

La beta usa:

```text
shapely==1.8.5.post1
svgpathtools==1.6.1
Pillow==9.5.0
```

Los ZIP de prueba incluyen un archivo `.bat` para instalar esas dependencias automáticamente.

## Plan de compatibilidad

TrueNest está pensado como un solo proyecto con compilaciones separadas por plataforma:

```text
Versión Windows: planeada
Versión macOS: planeada
```

La idea es mantener un solo repositorio y publicar versiones específicas para cada sistema en la sección de Releases de GitHub.

## Idioma del programa

El prototipo actual está principalmente en español. A futuro debería usar archivos de idioma como:

```text
locales/es.json
locales/en.json
```

Así el programa podría detectar el idioma del sistema operativo o permitir elegir manualmente entre español e inglés.

## Estado del proyecto

TrueNest está en desarrollo activo. Las versiones actuales son pruebas técnicas para confirmar que el núcleo de geometría, la importación SVG, el nesting real y la exportación hacia RDWorks funcionan correctamente.

Todavía faltan funciones importantes como:

- interfaz final con tema oscuro;
- miniaturas por figura;
- asignación manual de Figura / Mesa de trabajo;
- rotación inteligente;
- orden de corte interno/externo;
- compensación de grosor de corte láser / Offset polygon;
- builds empaquetados para Windows y macOS.

## Créditos

Creado por:

**Francisco Núñez Parra**

Asistencia técnica y generación de código:

**ChatGPT / OpenAI**
