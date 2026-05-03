# Pedido 007 — Simulación de respuesta móvil con opción numérica de Ariel

## 1. Microciclo

MC-LAB-7 — Simulación de respuesta móvil con opción numérica de Ariel.

## 2. Objetivo único

Simular que Ariel responde desde el celular ficticio con una opción numérica simple ("1") y el Portero interpreta esa opción usando el último contexto disponible, sin pedirle a Ariel que repita nada.

Este ciclo prueba que Ariel **no tiene que escribir prompts largos**. Un solo número es suficiente.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación y archivos Markdown.
- Agregar un segundo mensaje ficticio en `.movil/inbox/`.
- Agregar una segunda respuesta ficticia del Portero en `.movil/outbox/`.
- Producir pedido y revisión bajo `.mesa/`.
- Hacer commit documental y push a la rama `docs/mc-lab-7-respuesta-opcion-numerica`.

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
- No avanzar a MC-LAB-8.

## 5. Actores

- **Ariel** — único decisor humano. Responde con un número desde el celular ficticio.
- **Entrada móvil ficticia** — canal simulado. Archivos Markdown en `.movil/inbox`. No es WhatsApp real.
- **Portero Local** — recibe la opción numérica, recupera el último contexto y devuelve respuesta estructurada en `.movil/outbox`.
- **Torre** — interviene para proponer el próximo microciclo seguro si hay ambigüedad.
- **Mesa Local Ficticia** — único proyecto activo: Laboratorio Portero.

## 6. Regla a probar

- Ariel puede responder con un número. No necesita escribir el contexto completo.
- El Portero **no debe pedirle a Ariel que repita** lo que ya estaba definido.
- El Portero debe **usar el último contexto disponible** (último outbox) para interpretar la opción.
- El Portero debe **interpretar la opción elegida** y devolver el próximo paso.
- Si la opción implica riesgo (repo real, push, producción), debe pedir confirmación explícita.
- Si la opción es segura y documental, puede devolver el próximo paso sugerido directamente.

## 7. Contexto previo

El último mensaje del Portero (`.movil/outbox/001-respuesta-portero-ficticia.md`) ofrecía estas opciones:

> 1. Preparar prototipo ficticio de entrada móvil.
> 2. Ver estado del laboratorio.
> 3. Suspender.

## 8. Entrada ficticia

Ariel responde desde el celular:

> "1"

## 9. Interpretación esperada

- **Opción recibida:** 1
- **Contexto usado:** último outbox disponible (`.movil/outbox/001-respuesta-portero-ficticia.md`)
- **Acción interpretada:** preparar prototipo ficticio de entrada móvil
- **Estado real:** MC-LAB-6 ya incorporó el prototipo base en `main` (bandeja `.movil/inbox` y `.movil/outbox`)
- **Riesgo:** bajo, siempre que siga en laboratorio documental y sin WhatsApp real
- **Confianza:** media/alta
- **Requiere Torre:** sí, para proponer próximo microciclo seguro
- **Requiere Ariel:** no todavía
- **Acción segura sugerida:** proponer el próximo paso sin ejecutar nada técnico

## 10. Respuesta esperada

El Portero debe responder con:

- opción recibida;
- acción interpretada;
- estado del laboratorio;
- próximo paso sugerido;
- opciones nuevas numeradas para que Ariel elija.

## 11. Criterios de cierre

- Entrada ficticia con opción numérica creada (`.movil/inbox/002-respuesta-ariel-opcion-1-ficticia.md`).
- Respuesta ficticia interpretando la opción creada (`.movil/outbox/002-respuesta-portero-opcion-1-ficticia.md`).
- Resultado documentado en `.mesa/revisiones/`.
- Sin código ejecutable.
- Sin scripts.
- Sin workflows.
- Sin secrets.
- Sin WhatsApp real.
- Sin automatizaciones.
- Sin producción.
- Sin tocar repos reales.
