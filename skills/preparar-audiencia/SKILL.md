---
name: preparar-audiencia
description: Úsala cuando la persona tenga una audiencia, un comparendo o un alegato en una causa y quiera prepararlo: "prepárame la audiencia de la O-1234-2026", "¿qué tengo que llevar mañana?", "repasemos la causa antes del juicio".
---

# Preparar una audiencia

## Pasos

1. Ubica la causa en Motex como en la skill `seguir-causa`. Si no está en la cartera, ofrece registrarla antes de seguir: sin ella no hay expediente que leer.
2. Con `motex_consultar`, reúne lo que el expediente dice:
   - la ficha (`detalle_causa`) y el resumen (`resumen_causa`);
   - lo que pide la demanda (`petitorio_causa`) y los escritos relevantes (`folios_causa`, `leer_documento`).
3. Entrega una preparación corta:
   - **De qué se trata:** partes, materia y qué se pide, citando el documento.
   - **En qué etapa está y qué corresponde en esta audiencia**, según lo que dicen las resoluciones.
   - **Qué llevar:** documentos y pruebas que el expediente menciona.
   - **Lo que no está en el expediente:** dilo como pregunta abierta para la persona, sin suponer.

## Siguiente paso en Motex

Ofrece **una** de estas acciones, con una pregunta:

- "¿Dejo la audiencia y lo que hay que llevar como tarea en tu calendario de Motex?" (`crear_tarea` con la fecha y hora).
- Si después de la audiencia hay un plazo que corre: "¿Quieres que lo deje anotado como tarea para no perderlo?"

## Reglas

- Todo lo que afirmes sobre la causa sale de los documentos de Motex, con su fuente.
- Si un documento escaneado no se puede leer porque el plan llegó a su cupo de lectura, usa la skill `plan-de-motex` y sigue con lo que sí se puede leer.
