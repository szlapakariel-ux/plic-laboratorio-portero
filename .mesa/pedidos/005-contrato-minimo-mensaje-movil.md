# Pedido 005 — Contrato mínimo del mensaje móvil para operar desde el celular

## 1. Microciclo

MC-LAB-5 — Contrato mínimo del mensaje móvil para operar desde el celular.

## 2. Objetivo único

Definir, sin ejecutar nada real, el contrato documental mínimo para que Ariel pueda enviar mensajes simples desde el celular y el sistema los convierta en decisiones operables por Portero/Torre.

El contrato debe especificar: qué puede escribir Ariel, cómo el Portero interpreta el mensaje, qué responde el Portero, cuándo pide autorización, cuándo escala a Torre y cuándo no debe ejecutar.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación Markdown.
- Producir un pedido (este archivo) y una revisión correspondiente en `.mesa/revisiones/`.
- Hacer commit documental y push a la rama `docs/mc-lab-5-contrato-mensaje-movil`.

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
- No avanzar a MC-LAB-6.

## 5. Actores

- **Ariel** — único decisor humano. Opera desde el celular con mensajes cortos y simples.
- **Mensaje móvil ficticio** — canal simulado de entrada. No es WhatsApp real, no hay número, no hay API activa.
- **Portero Local** — recibe el mensaje, interpreta intención y proyecto, estructura la respuesta con opciones numeradas.
- **Torre** — reformula si hay ambigüedad, clasifica riesgo, define próximo paso seguro.
- **Mesa Local Ficticia** — mesa de trabajo simulada. Único proyecto activo: Laboratorio Portero.

## 6. Regla a definir

- Ariel debe poder enviar mensajes cortos desde el celular **sin redactar prompts técnicos largos**.
- El Portero debe **interpretar intención, proyecto y acción solicitada** con la información disponible.
- La Torre debe **reformular si hay ambigüedad** antes de cualquier acción.
- El sistema debe responder **con opciones simples y numeradas** para que Ariel elija.

## 7. Estructura mínima del mensaje de Ariel

El contrato acepta mensajes simples como:

- "Trabajar en laboratorio portero"
- "Ver estado"
- "Seguí con el celu"
- "Diagnóstico SOFSE"
- "Qué falta"
- "Opción 1" / "1"
- "Suspender"
- "No autorizar"

Ariel **no está obligado** a escribir:
- nombre exacto de rama;
- commit;
- comandos;
- prompt técnico completo;
- rutas de archivos;
- instrucciones para Claude.

## 8. Campos que el Portero debe inferir o pedir

- **proyecto** — inferido por contexto o solicitado si no se menciona;
- **intención** — inferida del texto o clasificada como ambigua;
- **nivel de acción** — lectura, diagnóstico, ejecución, autorización;
- **autorización requerida** — sí/no/pendiente;
- **riesgo** — bajo/medio/alto/bloqueo estructural;
- **estado actual** — último estado conocido del laboratorio;
- **próximo paso seguro** — opción reformulada lista para ejecutar o consultar.

## 9. Tipos de intención

- elegir proyecto;
- consultar estado;
- autorizar diagnóstico read-only;
- suspender ciclo;
- pedir próximo paso;
- responder opción numerada;
- reportar bloqueo;
- pedir reformulación.

## 10. Respuesta mínima del Portero

Toda respuesta debe contener:

- **proyecto detectado** (o "no detectado");
- **estado** del laboratorio o ciclo;
- **acción interpretada**;
- **riesgo**;
- **próximo paso** sugerido;
- **opciones numeradas** para que Ariel elija.

## 11. Criterios de cierre

- Contrato documentado con estructura de entrada y salida.
- Al menos 8 ejemplos de entrada/salida.
- Reglas anti-cartero incluidas.
- Sin código.
- Sin automatización.
- Sin WhatsApp real.
- Sin producción.
- Sin tocar repos reales.
