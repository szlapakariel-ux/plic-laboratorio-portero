# plic-laboratorio-portero

Laboratorio seguro, aislado y **no productivo** del proyecto PLIC — Torre de Control.

## Qué es

Este repositorio es un **laboratorio documental** para simular la lógica:

WhatsApp ficticio → Portero Local → Torre → Mesa Local Ficticia

sin tocar ningún proyecto real ni datos reales.

## Qué NO es

- **No reemplaza** a `torre-control`.
- **No toca** `auditoria-sofse`.
- **No toca** `agente-saas`.
- **No activa** automatizaciones reales.
- **No conecta** WhatsApp real. Todo flujo de WhatsApp aquí es ficticio/simulado.
- **No usa** Computer Use.
- **No toca** producción.
- **No contiene** código, scripts, workflows ni secrets.

## Modo de operación

Solo lectura documental y simulación escrita. Toda evidencia se construye en archivos Markdown dentro de este repo. El ciclo termina con documentación aislada y reporte; no avanza a ejecución técnica sin validación previa de la estructura documental.

## Estructura

- `.torre/` — protocolo, jerarquía documental y estado del laboratorio.
- `.mesa/` — simulación de mesa local ficticia, pedidos y revisiones.
- `simulaciones/` — flujos simulados (WhatsApp, bloqueos, escalamientos).
