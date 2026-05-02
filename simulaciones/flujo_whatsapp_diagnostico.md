# Simulación — Flujo WhatsApp ficticio para diagnóstico

Flujo **simulado**. No hay WhatsApp real conectado. Sirve únicamente como guion de referencia para validar la lógica antes de cualquier integración futura.

## Pasos del flujo

1. **Ariel elige proyecto por WhatsApp (ficticio).**
   Mensaje simulado al Portero indicando sobre qué proyecto quiere trabajar.

2. **Portero confirma conexión con la mesa local.**
   Verifica que la Mesa Local Ficticia esté disponible y que el proyecto exista en el catálogo simulado.

3. **Torre pide autorización.**
   Antes de cualquier diagnóstico, la Torre formula la pregunta de autorización a Ariel a través del Portero.

4. **Ariel responde `1`.**
   Confirmación explícita. Sin esta respuesta, no se inicia ningún diagnóstico.

5. **Se inicia diagnóstico read-only simulado.**
   Solo lectura. Ningún archivo del proyecto real se modifica. En este laboratorio, además, no hay proyecto real involucrado.

6. **Se devuelve estado, pendientes, bloqueos y próximo microciclo sugerido.**
   Resultado entregado por la Torre al Portero, y por el Portero a Ariel por WhatsApp ficticio.

## Restricciones

- Este flujo es **documental**. No se ejecuta.
- Cualquier ejecución real exige microciclo posterior con autorización explícita.
