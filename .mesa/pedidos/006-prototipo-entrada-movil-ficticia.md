# Pedido 006 — Prototipo mínimo de entrada móvil ficticia sin WhatsApp real

## 1. Microciclo

MC-LAB-6 — Prototipo mínimo de entrada móvil ficticia sin WhatsApp real.

## 2. Objetivo único

Crear el primer prototipo mínimo, seguro y no ejecutable de entrada móvil ficticia: representar que Ariel envía un mensaje desde el celular y el Portero lo transforma en una respuesta estructurada con opciones simples.

Este ciclo **no conecta WhatsApp real**, **no crea automatizaciones** y **no crea código ejecutable**. Solo crea archivos Markdown en `.movil/inbox` y `.movil/outbox` que representan el canal ficticio.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación y archivos Markdown.
- Crear carpeta `.movil/inbox` y `.movil/outbox` como bandejas ficticias.
- Crear un mensaje entrante ficticio y una respuesta ficticia del Portero.
- Producir pedido y revisión bajo `.mesa/`.
- Hacer commit documental y push a la rama `docs/mc-lab-6-prototipo-entrada-movil-ficticia`.

## 4. Prohibiciones

- No tocar `torre-control`, `auditoria-sofse` ni `agente-saas`.
- No copiar código de repos reales.
- No escribir código ejecutable, scripts ni workflows.
- No tocar secrets.
- No conectar WhatsApp real.
- No usar Computer Use.
- No activar automatizaciones.
- No tocar producción.
- No abrir PR ni hacer merge.
- No hacer force push.
- No cambiar settings del repo.
- No avanzar a MC-LAB-7.

## 5. Actores

- **Ariel** — único decisor humano. Envía mensaje corto desde el celular (ficticio).
- **Entrada móvil ficticia** — canal simulado. Archivos Markdown en `.movil/inbox`. No es WhatsApp real.
- **Portero Local** — recibe el mensaje, interpreta intención y devuelve respuesta estructurada en `.movil/outbox`.
- **Torre** — reformula si hay ambigüedad antes de que el Portero responda.
- **Mesa Local Ficticia** — único proyecto activo: Laboratorio Portero.

## 6. Regla a probar

- Ariel envía un mensaje corto desde el celular: **no debe ser un prompt técnico largo**.
- El Portero interpreta el mensaje usando el contrato de MC-LAB-5.
- La Torre interviene si hay ambigüedad antes de devolver respuesta.
- La respuesta vuelve a Ariel con **opciones simples y numeradas**.

## 7. Canal ficticio elegido

- Archivos Markdown dentro de `.movil/inbox/` y `.movil/outbox/`.
- Este canal **representa** una entrada móvil simulada.
- **No es WhatsApp real.**
- **No es una automatización.**
- **No ejecuta nada.**

## 8. Entrada ficticia inicial

Mensaje de Ariel: `"Seguí con lo del celu"`

## 9. Interpretación esperada

- **Proyecto probable:** Laboratorio Portero.
- **Intención:** continuar trabajo sobre entrada móvil.
- **Riesgo:** bajo, si sigue en laboratorio documental.
- **Requiere Torre:** sí, para reformular.
- **Requiere Ariel:** no, porque el contexto permite una acción documental segura.
- **Acción segura sugerida:** preparar respuesta del Portero con opciones, sin ejecutar.

## 10. Respuesta esperada

El Portero responde con:
- proyecto detectado;
- intención interpretada;
- riesgo;
- estado;
- próximo paso sugerido;
- opciones numeradas para que Ariel elija.

## 11. Criterios de cierre

- Entrada ficticia creada (`.movil/inbox/001-mensaje-ariel-ficticio.md`).
- Respuesta ficticia creada (`.movil/outbox/001-respuesta-portero-ficticia.md`).
- Resultado documentado en `.mesa/revisiones/`.
- Sin código ejecutable.
- Sin scripts.
- Sin workflows.
- Sin secrets.
- Sin WhatsApp real.
- Sin automatizaciones.
- Sin producción.
- Sin tocar repos reales.
