---
name: ponerse-al-dia
description: Úsala cuando la persona quiera saber cómo están sus causas en general: "¿qué pasó en mis causas?", "ponme al día", "¿qué tengo pendiente esta semana?", "resumen de mi cartera", o al empezar el día de trabajo.
---

# Ponerse al día con la cartera

La persona quiere un panorama de sus causas en Motex, no el detalle de una sola.

## Pasos

1. Llama a `motex_inicio` una vez por conversación para ver las capacidades vigentes.
2. Con `motex_consultar`, trae:
   - la cartera (`listar_causas`): cuántas causas sigue y en qué etapa están;
   - lo pendiente (`tareas_pendientes`): tareas y plazos con fecha, de lo más próximo a lo más lejano.
3. Responde en este orden, breve:
   - **Lo urgente:** lo que vence en los próximos 7 días, con la causa y el `enlace` a su ficha.
   - **Lo que se movió:** causas con actividad reciente, si los datos lo muestran.
   - **El resto:** una línea con cuántas causas siguen sin novedad.

## Siguiente paso en Motex

Termina con **una** pregunta que lleve a la acción, según lo que encontraste. No la ejecutes sin un sí:

- Si una causa tiene algo pendiente sin tarea: "¿La dejo como tarea en tu calendario de Motex?" (`crear_tarea`).
- Si una tarea ya está hecha: "¿La marco como cerrada?" (`actualizar_tarea`).
- Si la cartera está vacía: ofrece agregar su primera causa con la skill `seguir-causa`.

## Reglas

- No inventes movimientos ni plazos: si un dato no está en Motex, dilo.
- Si alguna capacidad responde que el plan llegó a su tope, usa la skill `plan-de-motex`.
