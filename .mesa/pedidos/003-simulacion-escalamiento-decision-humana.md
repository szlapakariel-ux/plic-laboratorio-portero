# Pedido 003 — Simulación documental de escalamiento correcto a Ariel cuando sí hay decisión humana real

## 1. Microciclo

MC-LAB-3 — Simulación documental de escalamiento correcto a Ariel cuando sí hay decisión humana real.

## 2. Objetivo único

Documentar, sin ejecutar nada real, el comportamiento esperado del laboratorio cuando un bloqueo **sí** requiere decisión humana real.

La simulación debe **probar** que el Portero y la Torre **no** molestan a Ariel por bloqueos recuperables internamente, y que **sí** lo escalan cuando hay decisión humana real, autorización faltante, cambio de alcance, riesgo de tocar repos reales, riesgo de producción, secrets, workflows, o ambigüedad que la Torre no puede resolver sola.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación Markdown.
- Producir un pedido (este archivo) y una revisión correspondiente en `.mesa/revisiones/`.
- Hacer commit documental y push a la rama `docs/mc-lab-3-escalamiento-decision-humana`.

## 4. Prohibiciones

- No tocar `torre-control`, `auditoria-sofse` ni `agente-saas`.
- No copiar código de repos reales.
- No escribir código, scripts ni workflows.
- No tocar secrets.
- No conectar WhatsApp real.
- No usar Computer Use.
- No activar automatizaciones.
- No tocar producción.
- No abrir PR ni hacer merge.
- No hacer force push.
- No cambiar settings del repo.

## 5. Actores simulados

- **Ariel** — único decisor humano. Solo se lo molesta ante decisión humana real.
- **Portero Local** — intermediario. No es cartero: filtra, junta evidencia, contiene escalamientos.
- **Torre** — capa de orquestación lógica del laboratorio. Clasifica el bloqueo, intenta recuperación interna, y cuando corresponde convierte el bloqueo en una decisión simple para Ariel.
- **Mesa Local Ficticia** — mesa de trabajo simulada. Único proyecto activo: Laboratorio Portero. Modo: simulación.
- **Ejecutor ficticio** — actor que estaba ejecutando el microciclo y se trabó. No es un agente real.

## 6. Regla a validar

- **No todo bloqueo se escala a Ariel.**
- Primero se intenta recuperación interna en Torre.
- Si el bloqueo requiere decisión humana real, **se escala**.
- La consulta a Ariel debe ser **breve, con opciones numeradas**.
- **Ariel no debe actuar como cartero** ni redactar instrucciones técnicas largas.

## 7. Casos que SÍ requieren escalar a Ariel

- Autorización para tocar un repo real.
- Autorización para PR, merge o push no previsto en el alcance vigente.
- Cambio de alcance del microciclo.
- Riesgo de tocar producción.
- Riesgo de exponer o usar secrets.
- Riesgo de crear o modificar workflows.
- Decisión entre dos caminos válidos con impacto de producto.
- Bloqueo técnico estructural no resoluble por Torre.

## 8. Casos que NO requieren escalar a Ariel

- Falta de evidencia recuperable (Torre pide reporte breve al ejecutor).
- Error menor de formato.
- Duda que Torre puede reformular.
- Espera breve sin impacto.
- Revisión documental sin riesgo.

## 9. Criterios de cierre

- Simulación documentada de extremo a extremo.
- Decisión humana identificada y justificada.
- Mensaje a Ariel reducido a opciones simples (numeradas).
- Sin código.
- Sin automatización.
- Sin WhatsApp real.
- Sin producción.
- Sin tocar repos reales.
