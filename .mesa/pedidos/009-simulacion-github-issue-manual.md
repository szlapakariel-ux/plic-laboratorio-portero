# Pedido 009 — Simulación de puente móvil mediante GitHub Issue manual

## 1. Microciclo

MC-LAB-9 — Simulación de puente móvil mediante GitHub Issue manual, sin automatización.

## 2. Objetivo único

Crear una simulación documental del primer puente móvil semirreal usando GitHub Issue manual como canal de entrada desde el celular. Demostrar cómo Ariel podría crear un issue desde el celular con un mensaje corto y cómo Portero/Torre lo tratarían como entrada móvil controlada.

Este ciclo **no crea issue real**, **no usa API**, **no crea automatizaciones**, **no crea bot**, **no crea endpoint**. Solo documenta y simula el flujo.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación y archivos Markdown.
- Crear una simulación de GitHub Issue manual en `.movil/issues/`.
- Crear respuesta del Portero equivalente en `.movil/outbox/`.
- Producir pedido y revisión bajo `.mesa/`.
- Hacer commit documental y push a la rama `docs/mc-lab-9-github-issue-manual`.

## 4. Prohibiciones

- No tocar `torre-control`, `auditoria-sofse` ni `agente-saas`.
- No copiar código de repos reales.
- No escribir código ejecutable, scripts ni workflows.
- No tocar secrets.
- No crear endpoint, bot ni API.
- No crear issue real en GitHub.
- No conectar WhatsApp real.
- No usar Computer Use.
- No activar automatizaciones.
- No tocar producción.
- No abrir PR ni hacer merge.
- No hacer force push.
- No cambiar settings del repo.
- No avanzar a MC-LAB-10.

## 5. Actores

- **Ariel** — único decisor humano. Crea el issue desde su celular (simulado en este ciclo).
- **Celular de Ariel** — dispositivo desde el que partiría el mensaje real.
- **GitHub Issue manual ficticio** — canal simulado. Archivo Markdown en `.movil/issues/`. No es issue real.
- **Portero Local** — recibe el issue como entrada controlada y devuelve respuesta estructurada en `.movil/outbox/`.
- **Torre** — interviene para proponer el próximo paso seguro.
- **Mesa Local Ficticia** — único proyecto activo: Laboratorio Portero.
- **Repo laboratorio** — `plic-laboratorio-portero`; único repo permitido en esta etapa.

## 6. Regla a probar

- Ariel puede crear un GitHub Issue desde el celular con un mensaje corto.
- Ese issue representa una entrada móvil semirreal.
- Portero/Torre **no deben tratarlo como orden técnica cruda**.
- Portero/Torre deben **convertirlo en entrada controlada** equivalente a `.movil/inbox`.
- La respuesta debe volver como `.movil/outbox`.
- **Nada debe ejecutarse automáticamente** sin autorización posterior explícita.

## 7. Canal simulado

GitHub Issue manual ficticio representado en Markdown dentro de:

```
.movil/issues/
```

Esta carpeta representa issues manuales simulados. No es una API. No es un webhook. No es automatización.

## 8. Entrada ficticia

**Título del issue:**
> "movil: Seguí con lo del celu"

**Cuerpo del issue:**
> "1"

## 9. Interpretación esperada

- **Canal:** GitHub Issue manual ficticio
- **Proyecto probable:** Laboratorio Portero
- **Intención:** continuar puente móvil semirreal
- **Opción recibida:** 1
- **Contexto usado:** último estado de `.movil/outbox` (outbox 002)
- **Riesgo:** bajo, siempre que siga en laboratorio documental y sin automatización
- **Confianza:** media/alta
- **Requiere Ariel:** sí, para avanzar a prueba manual real
- **Requiere Torre:** sí, para proponer checklist previo a prueba real
- **Acción segura:** responder con opciones, no ejecutar

## 10. Criterios de cierre

- Issue ficticio documentado (`.movil/issues/001-issue-manual-ficticio.md`).
- Respuesta ficticia creada (`.movil/outbox/003-respuesta-portero-issue-manual-ficticia.md`).
- Resultado documentado en `.mesa/revisiones/`.
- Sin issue real.
- Sin API.
- Sin endpoint.
- Sin bot.
- Sin código ejecutable.
- Sin scripts.
- Sin workflows.
- Sin secrets.
- Sin WhatsApp real.
- Sin automatizaciones.
- Sin producción.
- Sin tocar repos reales.
