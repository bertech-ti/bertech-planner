# Código fuente Planner MPS V109 - Bertech Panamá

## Qué archivo es el programa real
El programa completo original está en:
- `Planner_V109_original.html`

Ese archivo HTML contiene todo lo necesario para ejecutar el planner en el navegador:
- estructura visual HTML,
- estilos CSS embebidos,
- motor JavaScript embebido,
- formularios, reportes, Gantt, exportaciones y lógica del motor heurístico.

## Archivos separados para revisión TI
Para facilitar la revisión, se separó el mismo código en:
- `Planner_V109_html_separado.html`: estructura HTML con referencias externas.
- `Planner_V109_estilos.css`: estilos visuales extraídos desde el bloque `<style>`.
- `Planner_V109_motor.js`: código JavaScript extraído desde el bloque `<script>`.

## Importante
El archivo operativo original sigue siendo `Planner_V109_original.html`.
Los archivos separados son una extracción técnica para lectura, auditoría y mantenimiento. Si TI quiere modularizar el proyecto, puede usar estos archivos como punto de partida.

## Tecnología identificada
- HTML5
- CSS3
- JavaScript vanilla / ES6+
- Sin React, Angular, Vue, jQuery, npm, node_modules ni backend.
- Persistencia mediante archivo JSON compartido: `mps_datos.json`.
- Carga de stock mediante TXT SAP.
- Exportaciones mediante CSV y XLS generado desde HTML.

## Módulos principales dentro de `Planner_V109_motor.js`
- Constantes maestras: familias, BOM, actividades, stocks y códigos SAP.
- Reglas de limpieza de fabricación.
- Módulo de pedidos S&OP.
- Persistencia en JSON compartido.
- Motor heurístico principal: `runScenario()`.
- Evaluación de cumplimiento ETD.
- Inventario dinámico y stock final.
- Real vs Plan y KPIs.
- Exportadores CSV/XLS.
