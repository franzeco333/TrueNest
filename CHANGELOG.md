# Changelog

All notable changes to TrueNest are documented here.

---

## v0.04 - Clean RDWorks output + PNG preview

### English

Focus: make generated files more useful for RDWorks.

Changes:

- Generates a clean SVG intended for RDWorks import.
- Removes debug guides from the productive SVG.
- Adds PNG preview output for visual checking.
- Adds TXT report output.
- Adds export folder organization.
- Keeps direction/priority suffixes in output names.
- Adds notes for future laser kerf / offset polygon compensation.

### Español

Enfoque: hacer que la salida sea más útil para RDWorks.

Cambios:

- Genera un SVG limpio para importar en RDWorks.
- Elimina guías de depuración del SVG productivo.
- Agrega preview PNG para revisión visual.
- Agrega reporte TXT.
- Agrega organización por carpeta de exportación.
- Mantiene sufijos por dirección/prioridad.
- Agrega nota futura para compensación de corte láser / Offset polygon.

---

## v0.03b - Output suffixes and direction tests

### English

Focus: make multiple direction tests easier to compare.

Changes:

- Adds output suffixes based on 3x3 direction and priority.
- Example: `_7_H` = bottom-left + horizontal.
- Prevents reports/results from overwriting each other.
- Enlarges Execute / Cancel buttons.
- Fixes line endings for Windows Notepad.

### Español

Enfoque: facilitar comparar múltiples pruebas de dirección.

Cambios:

- Agrega sufijos según dirección 3x3 y prioridad.
- Ejemplo: `_7_H` = abajo izquierda + horizontal.
- Evita que reportes/resultados se sobrescriban.
- Agranda botones Ejecutar / Cancelar.
- Corrige saltos de línea para Bloc de notas de Windows.

---

## v0.03 - Direction and priority beta

### English

Focus: test direction-based nesting behavior.

Changes:

- Adds a compact options window.
- Adds 3x3 nesting direction selection.
- Adds vertical, horizontal and diagonal priority.
- Adds output report fields for direction and priority.
- Improves window focus behavior in Windows 7.

### Español

Enfoque: probar comportamiento de nesting por dirección.

Cambios:

- Agrega ventana compacta de opciones.
- Agrega selección de dirección 3x3.
- Agrega prioridad vertical, horizontal y diagonal.
- Agrega dirección y prioridad al reporte.
- Mejora el foco de ventanas en Windows 7.

---

## v0.02c - Visible process time

### English

Focus: make processing time visible.

Changes:

- Shows processing time in the final message.
- Adds processing time summary at the end of the report.

### Español

Enfoque: mostrar el tiempo de proceso.

Cambios:

- Muestra el tiempo de proceso en el mensaje final.
- Agrega resumen de tiempo al final del reporte.

---

## v0.02b - Speed optimization

### English

Focus: reduce nesting beta time from minutes to seconds.

Changes:

- Changes candidate search behavior.
- Uses the first valid position according to priority order.
- Increases beta grid step from 2 mm to 4 mm.
- Keeps exact Shapely validation.

### Español

Enfoque: reducir el tiempo de cálculo de minutos a segundos.

Cambios:

- Cambia la búsqueda de posiciones candidatas.
- Usa la primera posición válida según el orden de prioridad.
- Cambia grilla beta de 2 mm a 4 mm.
- Mantiene validación exacta con Shapely.

---

## v0.02 - First real geometry nesting beta

### English

Focus: prove that real geometry nesting is possible.

Changes:

- Reads SVG.
- Detects red work area and black figures.
- Converts SVG shapes to geometry.
- Uses Shapely to validate containment and collisions.
- Applies 3 mm spacing as 1.5 mm figure offset + 1.5 mm work area internal margin.
- Exports SVG result and TXT report.

### Español

Enfoque: comprobar que el nesting con geometría real es posible.

Cambios:

- Lee SVG.
- Detecta mesa roja y figuras negras.
- Convierte figuras SVG a geometría.
- Usa Shapely para validar contención y colisiones.
- Aplica separación de 3 mm como 1,5 mm por figura + 1,5 mm de margen interno de mesa.
- Exporta SVG resultado y reporte TXT.

---

## v0.01d - SVG import diagnosis correction

### English

Focus: fix SVG default black fill handling.

Changes:

- Correctly treats missing SVG fill as black by default.
- Keeps fill/stroke color rules.
- Detects possible compound paths with holes.
- Generates TXT and HTML import reports.

### Español

Enfoque: corregir lectura de relleno negro por defecto en SVG.

Cambios:

- Interpreta correctamente relleno ausente como negro por defecto.
- Mantiene reglas de color relleno/trazo.
- Detecta posibles paths compuestos con hoyos.
- Genera reportes TXT y HTML.
