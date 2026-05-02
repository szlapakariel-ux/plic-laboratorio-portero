# Jerarquía documental — Laboratorio Portero

Define el orden de precedencia de los documentos del laboratorio. En caso de conflicto, gana la capa de número más bajo.

## Capas

- **Capa 1 — Protocolo principal del laboratorio.**
  Archivo: `.torre/protocolo_principal.md`.
  Contiene las reglas operativas. Es la fuente de verdad de cómo se trabaja.

- **Capa 2 — Estado actual.**
  Archivo: `.torre/estado.md`.
  Describe la foto presente del laboratorio: qué está activo, qué está prohibido, próximo paso.

- **Capa 3 — Simulaciones.**
  Carpeta: `simulaciones/`.
  Flujos ficticios documentados (WhatsApp simulado, bloqueos, escalamientos). No ejecutables.

- **Capa 4 — Pedidos y revisiones de mesa ficticia.**
  Carpetas: `.mesa/pedidos/`, `.mesa/revisiones/`.
  Material operativo de la mesa local ficticia. Subordinado a las tres capas anteriores.

## Regla de modificación

Cualquier cambio en una capa superior obliga a revisar las capas inferiores. Cualquier cambio en una capa inferior no puede contradecir una capa superior.
