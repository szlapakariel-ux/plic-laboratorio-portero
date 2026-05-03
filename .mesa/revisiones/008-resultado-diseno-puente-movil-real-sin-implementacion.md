# Revisión 008 — Diseño documental del puente móvil real: resultado

Documento de cierre del pedido `.mesa/pedidos/008-diseno-puente-movil-real-sin-implementacion.md`. Toda interacción aquí es **ficticia** y **escrita**, no ejecutada.

## 1. Estado inicial

- MC-LAB-7: cerrado y mergeado en `main`. Opción numérica validada.
- Bandeja ficticia `.movil/inbox` y `.movil/outbox`: disponibles.
- Ariel ya puede simular frase corta y opción numérica dentro del laboratorio.
- Canal real desde celular: todavía inexistente.
- WhatsApp real: no conectado.
- Automatizaciones: no activadas.
- Producción: no aplica.

## 2. Problema a resolver

Ariel sigue actuando como **cartero** cuando debe copiar mensajes manualmente entre el celular, ChatGPT y Claude. El laboratorio ya tiene inbox/outbox ficticio que valida el flujo. Falta un **puente de entrada real o semirreal** que permita que el mensaje de Ariel llegue al sistema sin que él lo transcriba.

No se debe saltar directo a WhatsApp real: los riesgos (secrets, API externa, automatización, producción) son demasiado altos para este estado del laboratorio.

## 3. Opciones evaluadas

| Opción | Cómo entraría el mensaje | Ventaja | Riesgo | ¿Código? | ¿Secrets? | ¿Automatización? | ¿Producción? | Dictamen |
|---|---|---|---|---|---|---|---|---|
| A. GitHub Issue manual | Ariel crea issue desde app GitHub en celular | Trazabilidad nativa, cero secrets, cero bot | Ariel debe tener app instalada | No | No | No | No | **Recomendado** |
| B. GitHub Issue Form | Issue con plantilla estructurada | Guía a Ariel con campos predefinidos | Requiere crear `ISSUE_TEMPLATE` (Markdown, sin código) | No | No | No | No | Viable futuro |
| C. Google Form | Ariel llena form en celular | Muy fácil en celular | Requiere puente de lectura posterior (manual o script) | Parcial | No | Parcial | No | Posible, pero agrega paso intermedio |
| D. Email controlado | Ariel envía email | Universal desde celular | Requiere proceso de conversión (manual o automático) | Parcial | Posible | Parcial | No | No todavía |
| E. Telegram bot | Ariel escribe en chat | Muy natural en celular | Requiere bot, token, webhook | Sí | Sí | Sí | No | No todavía |
| F. WhatsApp real | Ariel escribe en WhatsApp | Más natural para Ariel | Requiere API Business, secrets, automatización, costo | Sí | Sí | Sí | Sí | No todavía |
| G. Archivo manual `.movil/inbox` | Alguien crea el `.md` a mano | Cero riesgo, laboratorio puro | Sigue requiriendo cartero para copiar | No | No | No | No | Útil en laboratorio, no resuelve el problema |

## 4. Dictamen de opciones

- **WhatsApp real:** NO todavía. Requiere API Business, secrets, automatización y potencial contacto con producción.
- **Telegram bot:** NO todavía. Requiere bot, token y webhook activo.
- **Email automático:** NO todavía. Requiere proceso de conversión no trivial.
- **Google Form:** posible como siguiente paso, pero todavía requiere un puente de lectura (manual o script) para convertir la respuesta en archivo de `.movil/inbox`.
- **Archivo manual en `.movil/inbox`:** útil para el laboratorio, pero mantiene el cartero — Ariel sigue copiando.
- **GitHub Issue manual:** **recomendado como primer puente semirreal**. Cero secrets, cero automatización, cero producción. Trazabilidad nativa. Ariel puede crear el issue desde la app de GitHub en el celular en segundos. La Torre/Portero lo lee como entrada humana controlada.

## 5. Opción recomendada para próximo microciclo

**MC-LAB-9 — Simulación de puente móvil mediante GitHub Issue manual, sin automatización.**

Ariel podría:
- abrir la app de GitHub en el celular;
- crear un issue en `plic-laboratorio-portero`;
- escribir el título: `movil: <mensaje corto>`;
- escribir el cuerpo: la opción o intención (ej. `"1"` o `"Seguí con lo del celu"`).

Torre/Portero:
- leerían el issue como entrada humana controlada;
- tratarían el título/cuerpo exactamente como si fuera `.movil/inbox`;
- generarían una respuesta documental equivalente a `.movil/outbox`.

Ariel:
- recibiría opciones para decidir el próximo paso (en el mismo issue o en un nuevo outbox documental).

Esto **no requiere**:
- bot;
- endpoint;
- secrets;
- WhatsApp real;
- producción;
- automatización.

## 6. Flujo propuesto sin implementación

```
Ariel (celular real)
  → abre app GitHub
  → crea issue en plic-laboratorio-portero
  → título: "movil: Seguí con lo del celu"
  → cuerpo: "1"

Torre/Portero (próximo microciclo)
  → lee el issue como entrada humana controlada
  → lo interpreta equivalente a .movil/inbox/003-...md
  → genera respuesta equivalente a .movil/outbox/003-...md

Ariel
  → lee la respuesta del Portero en el issue o en el outbox documental
  → elige opción numérica para el siguiente paso
```

Nada de este flujo se implementa en MC-LAB-8. Solo se diseña.

## 7. Límites del diseño

- No se creó issue real.
- No se conectó API.
- No se creó bot.
- No se creó endpoint.
- No se creó workflow.
- No se usó secret.
- No se conectó WhatsApp.
- No se activó automatización.

## 8. Seguridad

- Código ejecutable: no hubo.
- Scripts: no hubo.
- Workflows: no hubo.
- Secrets: no hubo.
- Producción: no hubo.
- WhatsApp real: no se conectó.
- Automatizaciones: no se activaron.
- `torre-control`: no se tocó.
- `auditoria-sofse`: no se tocó.
- `agente-saas`: no se tocó.

## 9. Validación anti-cartero

- El objetivo central es que **Ariel no tenga que copiar prompts largos** entre dispositivos.
- El canal recomendado (GitHub Issue) acepta **frases cortas u opciones numéricas** desde el celular.
- Torre/Portero **estructuran la entrada**: el texto crudo del issue nunca llega sin filtro al ejecutor.
- El ejecutor recibe siempre una **orden limpia** con proyecto, intención, riesgo y próximo paso.
- Ariel **solo decide con opciones simples** — nunca redacta instrucciones técnicas.

## 10. Próximo microciclo sugerido

**MC-LAB-9 — Simulación de puente móvil mediante GitHub Issue manual, sin automatización.**

Solo se sugiere. No se desarrolla en este ciclo.
