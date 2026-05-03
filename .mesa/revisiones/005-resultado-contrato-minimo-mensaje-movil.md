# Revisión 005 — Contrato mínimo del mensaje móvil: resultado

Documento de cierre del pedido `.mesa/pedidos/005-contrato-minimo-mensaje-movil.md`. Toda interacción aquí es **ficticia** y **escrita**, no ejecutada.

## 1. Estado inicial

- MC-LAB-4: cerrado y mergeado en `main`.
- Laboratorio: activo.
- Entrada móvil: todavía ficticia (canal simulado, sin WhatsApp real, sin API activa).
- WhatsApp real: no conectado.
- Automatizaciones: no activadas.
- Producción: no aplica.

## 2. Contrato mínimo de entrada

Ariel puede escribir (formato libre, sin sintaxis obligatoria):

| Tipo de mensaje | Ejemplos |
|---|---|
| Elegir proyecto | "Laboratorio Portero", "SOFSE", "trabajar en portero" |
| Consultar estado | "Qué falta", "Ver estado", "Cómo vamos" |
| Autorizar acción | "Dale", "1", "Opción 2", "Autorizar" |
| Suspender | "Suspender", "Parar", "Dejalo" |
| Pedir próximo paso | "Qué sigue", "Seguí", "Próximo" |
| Reportar bloqueo | "No anda", "Está trabado" |
| Pedir reformulación | "No entiendo", "Reformulá" |

Ariel **no está obligado a escribir**:
- nombre exacto de rama;
- hash de commit;
- comandos de terminal;
- prompt técnico completo;
- rutas de archivos;
- instrucciones para Claude.

## 3. Interpretación del Portero

El Portero convierte el mensaje en una estructura interna documental:

```
texto_original:        "Trabajar en Laboratorio Portero"
proyecto_detectado:    plic-laboratorio-portero
intención_detectada:   elegir proyecto
confianza:             alta
requiere_torre:        no
requiere_ariel:        no
riesgo:                bajo
acción_segura_sugerida: presentar estado y opciones de proyecto
opciones_para_ariel:   [1. Ver estado, 2. Diagnóstico read-only, 3. Suspender]
```

Si la confianza es baja o la intención es ambigua, el campo `requiere_torre` pasa a `sí` y la Torre reformula antes de devolver opciones a Ariel.

## 4. Estados de respuesta

El Portero usa estos estados internos:

- `conectado`
- `proyecto detectado`
- `falta proyecto`
- `intención ambigua`
- `autorización requerida`
- `diagnóstico no iniciado`
- `diagnóstico en curso`
- `recuperación interna`
- `bloqueo estructural`
- `suspendido`
- `listo para próximo paso`

## 5. Ejemplos de entrada/salida

---

**Ejemplo 1**

Ariel: `"Trabajar en Laboratorio Portero"`

Portero:
> "Proyecto detectado: Laboratorio Portero.
> Estado: conectado.
> Opciones:
> 1. Ver estado actual.
> 2. Autorizar diagnóstico read-only ficticio.
> 3. Suspender."

---

**Ejemplo 2**

Ariel: `"Seguí con lo del celu"`

Portero:
> "Intención detectada: continuar entrada móvil.
> Riesgo: bajo si sigue en laboratorio documental.
> Torre reformula el próximo paso.
> Opciones:
> 1. Abrir microciclo documental seguro.
> 2. Suspender.
> 3. Pedir resumen."

---

**Ejemplo 3**

Ariel: `"Diagnóstico SOFSE"`

Portero:
> "Proyecto detectado: auditoria-sofse.
> Atención: repo real.
> No ejecuto sin autorización.
> Opciones:
> 1. Autorizar diagnóstico read-only.
> 2. No autorizar.
> 3. Trabajar primero en laboratorio."

---

**Ejemplo 4**

Ariel: `"1"`

Portero:
> "Recibí opción 1.
> Acción interpretada según último estado pendiente.
> Confirmo antes de ejecutar si implica repo real, push, PR, merge o producción."

---

**Ejemplo 5**

Ariel: `"Qué falta"`

Portero:
> "Estado solicitado.
> Devuelvo: ciclo actual, pendiente principal, bloqueo si existe y próximo paso sugerido."

---

**Ejemplo 6**

Ariel: `"Pasalo a Claude"`

Portero:
> "Orden ambigua.
> No paso el mensaje crudo.
> Torre reformula antes de enviar al ejecutor."

---

**Ejemplo 7**

Ariel: `"Suspender"`

Portero:
> "Ciclo marcado como suspendido.
> No se ejecutan acciones nuevas hasta nueva autorización."

---

**Ejemplo 8**

Ariel: `"Mandalo a producción"`

Portero:
> "Bloqueo estructural.
> Producción requiere protocolo especial.
> Opciones:
> 1. Frenar.
> 2. Abrir diagnóstico de riesgo.
> 3. Solicitar checklist de producción."

---

## 6. Reglas anti-cartero

- Ariel **no redacta** prompts técnicos largos.
- Ariel **responde** con intención u opción numerada.
- El Portero **estructura** el mensaje en campos internos.
- La Torre **reformula** si hay ambigüedad o riesgo.
- El ejecutor **recibe** una orden limpia con alcance, restricciones y próximo paso.
- Si hay riesgo real, Ariel **decide con opciones** antes de que se ejecute nada.

## 7. Reglas de seguridad

El mensaje móvil **nunca autoriza por sí solo**:

| Acción | Requiere confirmación separada |
|---|---|
| Tocar producción | Sí |
| Usar secrets | Sí |
| Crear o modificar workflows | Sí |
| Tocar repo real | Sí |
| Merge | Sí |
| PR | Sí |
| Push a main | Sí |
| Conectar WhatsApp real | Sí |
| Activar automatizaciones | Sí |

Para todas estas acciones se requiere confirmación explícita separada, independientemente de lo que diga el mensaje móvil.

## 8. Resultado final

- Contrato mínimo: definido.
- Entrada móvil ficticia: lista para ser simulada en MC-LAB-6.
- Código: no hubo.
- Scripts: no hubo.
- Workflows: no hubo.
- Secrets: no hubo.
- Producción: no hubo.
- Repos reales (`torre-control`, `auditoria-sofse`, `agente-saas`): no se tocaron.
- WhatsApp real: no se conectó.
- Automatizaciones: no se activaron.

## 9. Próximo microciclo sugerido

**MC-LAB-6 — Prototipo mínimo de entrada móvil ficticia sin WhatsApp real.**

Solo se sugiere. No se desarrolla en este ciclo.
