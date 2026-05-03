# Pedido 002 — Simulación documental de bloqueo por 15 minutos sin avance verificable

## 1. Microciclo

MC-LAB-2 — Simulación documental de bloqueo por 15 minutos sin avance verificable.

## 2. Objetivo único

Documentar, sin ejecutar nada real, el comportamiento esperado del laboratorio cuando un microciclo se traba: pasan 15 minutos sin avance verificable, sin error explícito y sin decisión humana pendiente.

La simulación debe **probar** que el Portero **no escala automáticamente a Ariel**, que junta evidencia parcial, que la Torre intenta recuperación interna, y que solo se avisa a Ariel si el bloqueo es estructural o requiere decisión humana real.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación Markdown.
- Producir un pedido (este archivo) y una revisión correspondiente en `.mesa/revisiones/`.
- Hacer commit documental y push a la rama `docs/mc-lab-2-bloqueo-15-minutos`.

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
- **Torre** — capa de orquestación lógica del laboratorio. Clasifica el bloqueo, intenta recuperación interna y emite órdenes cortas.
- **Mesa Local Ficticia** — mesa de trabajo simulada. Único proyecto activo: Laboratorio Portero. Modo: simulación.
- **Ejecutor ficticio** — actor que estaba ejecutando el microciclo y se trabó. No es un agente real.

## 6. Regla a validar

- Pasan 15 minutos sin avance verificable.
- El Portero **no** escala directo a Ariel.
- El Portero junta evidencia parcial: último estado conocido, último archivo tocado, último intento documentado.
- La Torre intenta recuperación interna: revisar protocolo, revisar estado, replantear el microciclo, simular alternativas.
- **Solo si** el bloqueo es estructural —es decir, requiere decisión humana, autorización explícita o cambio de alcance— **se avisa a Ariel.**

## 7. Criterios de cierre

- Simulación documentada de extremo a extremo.
- Clasificación explícita del bloqueo simulado.
- Decisión explícita sobre si Ariel debe ser avisado o no.
- Sin código.
- Sin automatización.
- Sin WhatsApp real.
- Sin producción.
- Sin tocar repos reales.
