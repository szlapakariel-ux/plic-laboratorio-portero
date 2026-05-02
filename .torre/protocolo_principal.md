# Protocolo principal — Laboratorio Portero

Reglas operativas del laboratorio. Aplican a todo microciclo dentro de este repo.

## Reglas

1. **Un microciclo por vez.** No se abren ciclos paralelos.
2. **Un objetivo por ciclo.** Si aparece un segundo objetivo, va al backlog del próximo microciclo.
3. **Estabilizar → cerrar → medir → subir un nivel.** En ese orden, sin saltos.
4. **No automatizar si no fue probado.** Toda automatización requiere simulación previa documentada.
5. **No tocar proyecto real mientras exista una forma segura de validar en laboratorio.** Si se puede simular acá, se simula acá.
6. **Evidencia verificable antes de avanzar.** Cada paso deja archivo, registro o salida concreta dentro del repo.
7. **No subir de nivel si no está cerrado.** Cierre = evidencia + estado actualizado + próximo paso explícito.

## Alcance

Estas reglas aplican exclusivamente al laboratorio. No se trasladan a `torre-control`, `auditoria-sofse` ni `agente-saas` sin un microciclo posterior de adopción explícito.
