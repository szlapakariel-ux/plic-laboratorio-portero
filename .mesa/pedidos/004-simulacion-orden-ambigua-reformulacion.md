# Pedido 004 — Simulación documental de orden ambigua y reformulación por Torre antes de ejecutar

## 1. Microciclo

MC-LAB-4 — Simulación documental de orden ambigua y reformulación por Torre antes de ejecutar.

## 2. Objetivo único

Documentar, sin ejecutar nada real, el comportamiento esperado del laboratorio cuando Ariel envía una orden incompleta, mezclada o ambigua desde el celular.

La simulación debe **probar** que el sistema **no ejecuta a ciegas**: el Portero detecta la ambigüedad, la Torre reformula la orden en formato seguro y ejecutable, y solo si la ambigüedad no puede resolverse sin decisión humana se consulta a Ariel con opciones simples.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación Markdown.
- Producir un pedido (este archivo) y una revisión correspondiente en `.mesa/revisiones/`.
- Hacer commit documental y push a la rama `docs/mc-lab-4-orden-ambigua-reformulacion`.

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
- No avanzar a MC-LAB-5.

## 5. Actores simulados

- **Ariel** — único decisor humano. Puede mandar mensajes cortos e imprecisos desde el celular.
- **Mensaje móvil ficticio** — canal simulado de entrada móvil. No es WhatsApp real, no hay número, no hay API activa.
- **Portero Local** — intermediario. Recibe el mensaje, detecta ambigüedad, no lo pasa crudo al ejecutor.
- **Torre** — capa de orquestación lógica. Interpreta la intención, la limita y reformula en instrucción segura y concreta.
- **Mesa Local Ficticia** — mesa de trabajo simulada. Único proyecto activo: Laboratorio Portero. Modo: simulación.
- **Ejecutor ficticio** — actor que recibirá la orden ya reformulada. No actúa hasta recibir instrucción clara.

## 6. Regla a validar

- Ariel puede enviar mensajes incompletos, mezclados o ambiguos desde el celular.
- El Portero **no debe pasar la orden cruda** al ejecutor.
- La Torre **debe detectar ambigüedad** y no asumir alcance.
- La Torre **debe reformular** la orden en formato seguro, concreto y ejecutable.
- Si la intención es suficiente para inferir un microciclo seguro: la Torre avanza **sin molestar a Ariel**.
- Si falta decisión humana real: la Torre **consulta a Ariel con opciones simples**.

## 7. Ejemplos de órdenes ambiguas

- "seguí con lo de ayer"
- "metele al portero"
- "hacé que funcione"
- "pasalo a Claude"
- "probemos lo del celu"
- "arreglá lo que falta"

Ninguno de estos mensajes define: repo objetivo, microciclo, alcance, si es documental o técnico, si autoriza código, si autoriza push/PR/merge, si involucra WhatsApp real ni si involucra producción.

## 8. Criterios de cierre

- Simulación documentada de extremo a extremo.
- Ambigüedad detectada y documentada.
- Orden reformulada en formato seguro.
- Decisión explícita sobre si Ariel debe intervenir o no.
- Sin código.
- Sin automatización.
- Sin WhatsApp real.
- Sin producción.
- Sin tocar repos reales.
