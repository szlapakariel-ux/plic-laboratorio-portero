# Pedido 001 — Simulación documental del flujo WhatsApp ficticio → Portero → Torre

## 1. Microciclo

MC-LAB-1 — Simulación documental del flujo WhatsApp ficticio → Portero → Torre.

## 2. Objetivo único

Documentar, sin ejecutar nada real, el primer flujo operativo del laboratorio:

WhatsApp ficticio → Portero Local → Torre → autorización de Ariel → diagnóstico read-only ficticio → respuesta final con estado, pendientes, bloqueos y próximo microciclo sugerido.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación Markdown.
- Producir un pedido (este archivo) y una revisión correspondiente en `.mesa/revisiones/`.
- Hacer commit documental y push a la rama `docs/mc-lab-1-simulacion-flujo-whatsapp`.

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

- **Ariel** — único decisor humano. Interactúa por WhatsApp ficticio mediante mensajes cortos u opciones numeradas.
- **WhatsApp ficticio** — canal de mensajería simulado. No hay número, no hay API, no hay sesión real.
- **Portero Local** — intermediario entre WhatsApp ficticio y la Torre. Confirma conexión, junta evidencia, contiene escalamientos.
- **Torre** — capa de orquestación lógica del laboratorio. Pide autorización, ejecuta diagnóstico ficticio, devuelve estado.
- **Mesa Local Ficticia** — mesa de trabajo simulada. Único proyecto activo: Laboratorio Portero. Modo: simulación. Datos reales: ninguno.

## 6. Flujo esperado

1. Ariel escribe por WhatsApp ficticio.
2. Ariel elige el proyecto **Laboratorio Portero**.
3. Portero confirma conexión con la Mesa Local Ficticia.
4. Torre pide autorización con opciones numeradas.
5. Ariel responde `1`.
6. Se inicia diagnóstico read-only simulado.
7. Torre devuelve: estado, pendientes, bloqueos y próximo microciclo sugerido.

## 7. Criterios de cierre

- Simulación documentada de extremo a extremo.
- Sin código.
- Sin automatización.
- Sin WhatsApp real.
- Sin producción.
- Sin tocar repos reales.
