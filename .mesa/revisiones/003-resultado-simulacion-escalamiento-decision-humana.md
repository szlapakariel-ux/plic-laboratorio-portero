# Revisión 003 — Resultado de la simulación de escalamiento correcto a Ariel cuando sí hay decisión humana real

Documento de cierre del pedido `.mesa/pedidos/003-simulacion-escalamiento-decision-humana.md`. Toda interacción aquí es **ficticia** y **escrita**, no ejecutada.

## 1. Estado inicial

- MC-LAB-2: cerrado y mergeado en `main`.
- Laboratorio: activo.
- Mesa Local Ficticia: disponible.
- Ejecutor ficticio: asignado a un microciclo ficticio en curso.
- Diagnóstico simulado: en curso.
- Producción: no aplica.

## 2. Evento que dispara posible escalamiento

- El ejecutor ficticio detecta que para avanzar tendría que **tocar un repo real** o **cambiar el alcance autorizado** del microciclo.
- No hay autorización previa para esa acción.
- Continuar sin permiso **rompería el protocolo** del laboratorio.

Es un bloqueo no recuperable internamente: aunque la Torre tiene capacidad técnica para reformular, no tiene autoridad para decidir el cambio de alcance.

## 3. Recuperación interna previa

- El Portero **no escala de inmediato**.
- Junta evidencia: último estado conocido, último archivo tocado, intento documentado del ejecutor.
- La Torre revisa si puede resolver sin Ariel: ¿se puede reformular? ¿se puede cerrar el microciclo como "sin cambios"? ¿se puede mover el alcance dentro del laboratorio sin tocar repo real?
- La Torre determina que **no puede decidir sola** porque la decisión implica autorización humana real (cambio de alcance).

## 4. Clasificación del bloqueo

Matriz simple aplicada al laboratorio:

| Tipo de bloqueo | Acción | ¿Escalar a Ariel? |
|---|---|---|
| Falta de evidencia | recuperación interna: pedir reporte breve | No |
| Ambigüedad corregible por Torre | Torre reformula | No |
| Cambio de alcance | escalar | Sí |
| Repo real involucrado | escalar | Sí |
| Push / PR / merge no autorizado | escalar | Sí |
| Producción / secrets / workflows | escalar y frenar | Sí |
| Dos caminos válidos con impacto de producto | escalar con opciones | Sí |

En este caso: **cambio de alcance** + **repo real involucrado** ⇒ corresponde escalar.

## 5. Transcript simulado

**Portero Local:**
> "Detecté bloqueo. No escalo todavía. Recolecto evidencia y consulto a Torre."

**Torre:**
> "Evidencia recibida. El bloqueo no es recuperable internamente porque implica cambiar alcance autorizado."

**Torre a Ariel:**
> "Necesito decisión humana. El ejecutor no puede avanzar sin cambiar el alcance. Elegí una opción:
> 1. Mantener alcance actual y cerrar como bloqueado.
> 2. Autorizar nuevo microciclo documental para redefinir alcance.
> 3. Suspender el ciclo."

**Ariel:**
> "2"

**Torre:**
> "Decisión registrada. No se toca código ni repo real. Próximo paso: abrir microciclo documental de redefinición de alcance."

**Portero Local:**
> "Escalamiento correcto. Ariel decidió con una opción simple. No actuó como cartero."

## 6. Validación anti-cartero

- Ariel **no redactó** instrucciones técnicas largas.
- Ariel **eligió** entre opciones numeradas presentadas por la Torre vía Portero.
- La Torre **convirtió el bloqueo en decisión**: no le pidió a Ariel que diagnostique, le presentó alternativas accionables.
- El Portero **no escaló antes** de juntar evidencia ni antes de que la Torre intentara recuperación interna.
- Se evitó pedirle a Ariel que copie y pegue mensajes entre agentes.

## 7. Resultado final

- Simulación: completada.
- Escalamiento: justificado (cambio de alcance + repo real involucrado).
- Ariel: fue consultado **solo** por decisión humana real, mediante una opción simple.
- Código: no hubo.
- Scripts: no hubo.
- Workflows: no hubo.
- Secrets: no hubo.
- Producción: no hubo.
- Repos reales (`torre-control`, `auditoria-sofse`, `agente-saas`): no se tocaron.
- WhatsApp real: no se conectó.
- Automatizaciones: no se activaron.

## 8. Próximo microciclo sugerido

**MC-LAB-4 — Simulación documental de orden ambigua y reformulación por Torre antes de ejecutar.**

Solo se sugiere. No se desarrolla en este ciclo.
