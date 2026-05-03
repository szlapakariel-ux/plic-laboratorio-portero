# Revisión 004 — Resultado de la simulación de orden ambigua y reformulación por Torre antes de ejecutar

Documento de cierre del pedido `.mesa/pedidos/004-simulacion-orden-ambigua-reformulacion.md`. Toda interacción aquí es **ficticia** y **escrita**, no ejecutada.

## 1. Estado inicial

- MC-LAB-3: cerrado y mergeado en `main`.
- Laboratorio: activo.
- Mesa Local Ficticia: disponible.
- Mensaje móvil ficticio: habilitado solo como simulación (no hay WhatsApp real, no hay API activa).
- Ejecutor ficticio: disponible, en espera de instrucción clara.
- Producción: no aplica.

## 2. Mensaje ambiguo recibido

**Ariel desde mensaje móvil ficticio:**
> "Dale, seguí con lo del celu y pasalo al portero."

## 3. Detección de ambigüedad

La orden es ambigua porque **no define**:

- **Repo objetivo:** ¿`plic-laboratorio-portero`? ¿otro repo?
- **Microciclo:** ¿qué tarea concreta debe ejecutarse?
- **Alcance:** ¿es documental o técnico?
- **Autorización de código:** no indicada.
- **Autorización de push, PR o merge:** no indicada.
- **Involucra WhatsApp real:** no queda claro (menciona "celu").
- **Involucra producción:** no queda claro.

Ejecutar esta orden en crudo podría implicar acciones no autorizadas o tocar repos reales sin permiso explícito.

## 4. Acción correcta del Portero

- **No pasar la orden cruda al ejecutor.**
- **No inventar alcance** ni asumir que "celu" significa WhatsApp real.
- **No tocar archivos** hasta recibir instrucción reformulada.
- **No pedirle a Ariel que redacte todo de nuevo** — eso lo convertiría en cartero.
- **Elevar a Torre** para que interprete, limite y reformule.

## 5. Reformulación por Torre

La Torre analiza el contexto disponible:
- Repositorio activo: `plic-laboratorio-portero`.
- Último microciclo cerrado: MC-LAB-3.
- Historial: laboratorio documental, sin código, sin WhatsApp real, sin producción.
- Intención probable: avanzar hacia el contrato del mensaje móvil (mencionado como sugerencia en MC-LAB-3).

**Orden reformulada:**
> "Continuar en el repo `plic-laboratorio-portero` con un microciclo documental de laboratorio para definir el contrato mínimo del mensaje móvil. No tocar código, no conectar WhatsApp real, no tocar producción, no abrir PR ni mergear sin autorización separada."

La Torre no necesita consultar a Ariel porque la intención puede inferirse por contexto seguro y la reformulación no implica ninguna acción no autorizada.

## 6. Decisión sobre Ariel

Clasificación aplicada:

| Condición | ¿Consultar a Ariel? |
|---|---|
| Intención inferible por contexto seguro | No |
| Acción remota no autorizada | Sí |
| Implica código | Sí |
| Implica WhatsApp real | Sí |
| Implica producción | Sí (frenar) |
| Implica tocar repo real | Sí (frenar) |
| Solo requiere reformulación documental segura | **No** |

En este caso: la orden reformulada es **solo documental** dentro del laboratorio. **No se consulta a Ariel.**

## 7. Transcript simulado

**Ariel:**
> "Dale, seguí con lo del celu y pasalo al portero."

**Portero Local:**
> "Orden recibida. Detecto ambigüedad. No ejecuto todavía. Elevo a Torre para reformulación."

**Torre:**
> "Contexto identificado: laboratorio seguro. Intención probable: avanzar hacia entrada móvil. Reformulo en microciclo documental seguro."

**Torre al ejecutor ficticio:**
> "Crear propuesta documental para contrato mínimo de mensaje móvil en laboratorio. No código. No WhatsApp real. No producción. No PR ni merge."

**Ejecutor ficticio:**
> "Orden reformulada recibida. Alcance claro. No ejecuto todavía porque este microciclo solo valida reformulación."

**Portero Local:**
> "No se molestó a Ariel. La orden fue reformulada sin convertirlo en cartero."

## 8. Validación anti-cartero

- Ariel **no tuvo que redactar** un prompt técnico largo ni repetir la instrucción con más detalle.
- El Portero **no copió la frase cruda** al ejecutor.
- La Torre **interpretó, limitó y reformuló** la intención en una instrucción segura.
- El ejecutor ficticio **recibió una instrucción clara** con alcance, restricciones y próximo paso explícito.
- Si la orden hubiera implicado código, WhatsApp real, producción o repos reales, Ariel habría sido consultado con opciones numeradas antes de cualquier acción.

## 9. Resultado final

- Simulación: completada.
- Orden ambigua: detectada.
- Orden: reformulada.
- Ejecución a ciegas: no ocurrió.
- Ariel: no fue usado como cartero.
- Código: no hubo.
- Scripts: no hubo.
- Workflows: no hubo.
- Secrets: no hubo.
- Producción: no hubo.
- Repos reales (`torre-control`, `auditoria-sofse`, `agente-saas`): no se tocaron.
- WhatsApp real: no se conectó.
- Automatizaciones: no se activaron.

## 10. Próximo microciclo sugerido

**MC-LAB-5 — Contrato mínimo del mensaje móvil para que Ariel pueda operar desde el celular.**

Solo se sugiere. No se desarrolla en este ciclo.
