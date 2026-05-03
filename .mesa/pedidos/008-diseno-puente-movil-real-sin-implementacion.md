# Pedido 008 — Diseño documental del puente móvil real sin implementación

## 1. Microciclo

MC-LAB-8 — Diseño documental del puente móvil real sin implementación.

## 2. Objetivo único

Diseñar documentalmente cómo podría ingresar un mensaje real enviado desde el celular de Ariel al sistema, sin que Ariel actúe como cartero. Este ciclo **no implementa nada**. Solo compara opciones, identifica riesgos y recomienda cuál probar primero.

## 3. Alcance permitido

- Trabajar exclusivamente dentro del repo `plic-laboratorio-portero`.
- Crear únicamente documentación y archivos Markdown.
- Comparar opciones de canal real sin implementar ninguna.
- Producir pedido y revisión bajo `.mesa/`.
- Hacer commit documental y push a la rama `docs/mc-lab-8-diseno-puente-movil-real`.

## 4. Prohibiciones

- No tocar `torre-control`, `auditoria-sofse` ni `agente-saas`.
- No copiar código de repos reales.
- No escribir código ejecutable, scripts ni workflows.
- No tocar secrets.
- No crear endpoint, bot ni API.
- No conectar WhatsApp real.
- No usar Computer Use.
- No activar automatizaciones.
- No tocar producción.
- No abrir PR ni hacer merge.
- No hacer force push.
- No cambiar settings del repo.
- No avanzar a MC-LAB-9.

## 5. Actores

- **Ariel** — único decisor humano. Envía mensaje corto desde su celular real.
- **Celular real de Ariel** — dispositivo desde el que parte el mensaje.
- **Canal puente futuro** — aún no elegido; este ciclo lo diseña y compara.
- **Portero Local** — recibe la entrada ya transformada en formato controlado y devuelve respuesta estructurada.
- **Torre** — reformula si hay ambigüedad antes de que el Portero responda.
- **Mesa Local Ficticia** — único proyecto activo: Laboratorio Portero.
- **Repo laboratorio** — `plic-laboratorio-portero`; único repo permitido en esta etapa.

## 6. Regla a diseñar

- El celular real de Ariel debe poder enviar un mensaje corto.
- Ese mensaje debe entrar al laboratorio **sin tocar repos reales** de producción.
- El mensaje debe terminar como entrada controlada equivalente a `.movil/inbox`.
- El Portero debe responder en formato equivalente a `.movil/outbox`.
- **Nada debe ejecutarse automáticamente** sin autorización posterior explícita.

## 7. Canales candidatos a evaluar

### A. GitHub Issue manual desde celular
Ariel crea un issue directamente desde la app de GitHub en el celular. El título y el cuerpo contienen el mensaje.

### B. GitHub Issue Form futuro
Un formulario de issue estructurado (`ISSUE_TEMPLATE`) guía a Ariel para ingresar datos en campos predefinidos. No requiere automatización hoy; el formulario es solo Markdown.

### C. Google Form
Ariel llena un formulario Google desde el celular. Las respuestas quedan en una hoja de cálculo. Alguien (o un script futuro) lee esa hoja y genera el archivo en `.movil/inbox`.

### D. Email controlado
Ariel envía un email a una dirección específica. Un proceso futuro (manual o automatizado) convierte ese email en entrada controlada.

### E. Telegram bot futuro
Ariel escribe en un chat de Telegram. Un bot futuro recibe el mensaje y lo deposita en `.movil/inbox`.

### F. WhatsApp real futuro
Ariel escribe en WhatsApp. Un bot futuro con la API de WhatsApp Business recibe el mensaje.

### G. Archivo manual en `.movil/inbox`
Ariel (o alguien) crea el archivo Markdown directamente en `.movil/inbox` con el contenido del mensaje. Sigue requiriendo que alguien copie/pegue.

## 8. Criterios de evaluación

Para cada opción se evalúa:

| Criterio | Descripción |
|---|---|
| Facilidad desde celular | ¿Puede Ariel hacerlo en 5 segundos desde la app? |
| Riesgo técnico | ¿Puede fallar, romperse o generar efectos no deseados? |
| Requiere secrets | ¿Necesita tokens, credenciales o API keys? |
| Requiere API | ¿Depende de una API externa? |
| Requiere automatización | ¿Necesita un bot, webhook o trigger? |
| Trazabilidad | ¿Queda registro auditable de cada mensaje? |
| Opera sin cartero | ¿Ariel puede enviar sin copiar nada manualmente? |
| Compatibilidad laboratorio | ¿Encaja con el repo aislado actual? |
| Requiere código | ¿Necesita escribir o ejecutar código? |
| Requiere producción | ¿Toca algo fuera del laboratorio? |

## 9. Recomendación esperada

La primera opción recomendada debe priorizar:
- mínimo riesgo;
- cero secrets;
- cero producción;
- cero WhatsApp real;
- cero automatización automática;
- trazabilidad nativa;
- facilidad para Ariel desde el celular.

## 10. Criterios de cierre

- Diseño documentado.
- Opciones comparadas con matriz.
- Primera opción recomendada justificada.
- Riesgos identificados por opción.
- Autorizaciones futuras listadas.
- Sin código ejecutable.
- Sin scripts.
- Sin workflows.
- Sin secrets.
- Sin producción.
- Sin WhatsApp real.
- Sin automatizaciones.
- Sin tocar repos reales.
