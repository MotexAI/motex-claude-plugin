# Motex para Claude

Motex sigue tus causas del Poder Judicial de Chile (PJUD) y este plugin lo trae a tu conversación con Claude. Agrega una causa por su RIT y tribunal y en segundos tienes su carátula, su etapa y un link a la ficha en Motex; ponte al día con lo que vence y lo que se movió en tu cartera; prepara una audiencia leyendo el expediente; y deja las tareas y plazos en tu calendario de Motex.

## Qué incluye

- **Conector de Motex** (`https://legal.motex.ai/api/mcp`): al conectarlo, entras con tu cuenta de Google. Si todavía no usas Motex, se crea tu espacio con el plan gratis (hasta 10 causas). Si tu estudio ya usa Motex, entras a su cartera.
- **Skills:**
  - `seguir-causa`: busca, registra y explica una causa por su RIT.
  - `ponerse-al-dia`: lo urgente, lo que se movió y lo pendiente de tu cartera.
  - `preparar-audiencia`: un repaso de la causa antes de una audiencia, con sus fuentes.
  - `plan-de-motex`: qué incluye tu plan y qué hacer cuando llegas a un tope.
- **Comandos:** `/motex:mi-dia` y `/motex:agregar-causa <RIT> <tribunal>`.

Claude te pide confirmación antes de cualquier cambio en Motex, como registrar una causa o crear una tarea.

## Instalar

- **claude.ai y Cowork:** búscalo en el directorio de plugins, o en Customize > Plugins > Add > Add marketplace con `MotexAI/motex-claude-plugin`.
- **Claude Code:** `/plugin marketplace add MotexAI/motex-claude-plugin` y después `/plugin install motex@motex`.
- **Solo el conector, en cualquier asistente:** https://motex.ai/conectar

## Datos

El plugin no guarda nada por sí mismo y no ejecuta código: son instrucciones y la referencia al conector. Lo que le pides a Claude sobre tus causas viaja solo al servidor de Motex en `legal.motex.ai`, autenticado con OAuth. Motex lee causas públicas del PJUD; no accede a causas reservadas ni de familia. Política de privacidad: https://motex.ai/es/privacidad. Soporte: contacto@motex.ai.
