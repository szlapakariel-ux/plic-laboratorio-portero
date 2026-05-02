# Simulación — Regla de bloqueo de 15 minutos

Define cómo se comporta el Portero cuando un microciclo se traba.

## Regla

- **Pasan 15 minutos sin avance verificable.**
  Se considera bloqueo activo.

- **Portero NO escala directo a Ariel.**
  No interrumpe a Ariel solo porque hubo demora.

- **Portero junta evidencia parcial.**
  Logs simulados, último estado conocido, último archivo tocado, último intento documentado.

- **Torre intenta recuperación interna.**
  Reintentos lógicos dentro del laboratorio: revisar protocolo, revisar estado, replantear el microciclo, simular alternativas.

- **Solo si el bloqueo es estructural** —es decir, requiere decisión humana, autorización explícita o cambio de alcance— **se avisa a Ariel.**
  El aviso incluye: evidencia parcial, intento de recuperación, motivo por el que no se pudo resolver internamente, y propuesta concreta de decisión.

## Restricción

Esta regla aplica al laboratorio. Su adopción en `torre-control`, `auditoria-sofse` o `agente-saas` requiere microciclo posterior dedicado.
