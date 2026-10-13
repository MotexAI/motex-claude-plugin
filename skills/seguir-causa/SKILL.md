---
name: seguir-causa
description: Úsala cuando la persona nombre una causa judicial chilena por su RIT (por ejemplo O-1234-2026, C-567-2025, T-89-2026) o pida "agrega", "sigue", "revisa" o "¿qué pasó en?" una causa, o cuando pregunte por una causa que no aparece en su cartera de Motex.
---

# Seguir una causa con Motex

Motex lee el Poder Judicial (PJUD) y deja cada causa seguida en la cartera de la persona: carátula, movimientos, escritos y documentos, con un link a su ficha. Esta skill resuelve lo que la persona pidió sobre UNA causa y, al final, le ofrece el siguiente paso en Motex.

## 1. Buscarla en su cartera

Llama a `motex_inicio` una vez por conversación para ver las capacidades vigentes y sus nombres. Después busca la causa con `motex_consultar` (`listar_causas` o `detalle_causa` con el RIT).

- **Si está:** contesta lo que se pidió con sus datos (`detalle_causa`, `resumen_causa`, `folios_causa`, `leer_documento` según la pregunta). Cita de qué documento o movimiento sale cada dato y entrega el `enlace` a la ficha en Motex.
- **Si no está:** dile que no está en su cartera y pregúntale si quiere agregarla. Necesitas el RIT y el tribunal con su nombre completo; si falta el tribunal, pregúntalo. Nunca elijas un tribunal parecido: el mismo RIT existe en muchos juzgados.

## 2. Registrarla (solo si la persona lo confirma)

Con la confirmación, llama a `motex_modificar` con `registrar_causa`. Según el `estado`:

- `registrada` con `ficha`: cuéntale la carátula, el tribunal, el procedimiento y la etapa, entrega el `enlace` y aclara que la demanda y los documentos se terminan de leer en los minutos siguientes.
- `registrada` con `buscando_en_pjud`: el PJUD todavía no la trae; dile que aparecerá en su cartera en un rato y que puede volver a preguntar.
- `no_encontrada`: el PJUD dice que no existe; muestra el `motivo` y pide revisar el RIT y el tribunal.
- `tope_alcanzado`: usa la skill `plan-de-motex`.

## 3. Ofrecer el siguiente paso en Motex

Después de resolver lo pedido, ofrece **uno** de estos pasos, el que corresponda a la causa. Ofrécelo con una pregunta; no lo hagas sin que la persona diga que sí.

- Si hay un plazo, una audiencia o algo pendiente: "¿Quieres que lo deje como tarea en tu calendario de Motex?" (`crear_tarea` con fecha).
- Si la causa recién se registró: "Motex te avisará cuando haya un movimiento nuevo. ¿Quieres que te muestre la demanda cuando esté leída?"
- Si la persona trabaja la causa con frecuencia: recuérdale que la ficha completa (documentos, escritos, línea de tiempo) está en el `enlace`.

## Reglas

- Solo causas públicas del PJUD. Las reservadas y las de familia no se pueden leer sin la Clave Única de la persona: dilo y no intentes conseguirlas por otro camino.
- No inventes plazos ni fechas: si el documento no lo dice, dilo.
- No registres causas que la persona no pidió agregar.
