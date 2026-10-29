# Motex for Claude

Motex tracks your cases in Chile's Judiciary (Poder Judicial, PJUD), and this plugin brings it into your conversation with Claude. Add a case by its docket number (RIT) and court and within seconds you get its caption, its stage and a link to the case in Motex; catch up on what is due and what moved in your portfolio; prepare a hearing by reading the case file; and keep tasks and deadlines in your Motex calendar. Built for Chilean lawyers: the skills and Motex itself speak Spanish.

## What's included

- **Motex connector** (`https://legal.motex.ai/api/mcp`): when you connect it, you sign in with your Google account. If you don't use Motex yet, a workspace is created for you on the free plan (up to 10 cases). If your firm already uses Motex, you get its portfolio.
- **Skills:**
  - `seguir-causa`: finds, registers and explains a case by its docket number.
  - `ponerse-al-dia`: what's urgent, what moved and what's pending in your portfolio.
  - `preparar-audiencia`: a review of the case before a hearing, citing its sources.
  - `plan-de-motex`: what your plan includes and what to do when you reach a limit.
- **Commands:** `/motex:mi-dia` and `/motex:agregar-causa <RIT> <court>`.

Claude confirms before changes in Motex that you didn't explicitly ask for, such as registering a case you only mentioned. A change you asked for runs without a second prompt.

## Install

- **claude.ai and Cowork:** find it in the plugin directory, or in Customize > Plugins > Add > Add marketplace with `MotexAI/motex-claude-plugin`.
- **Claude Code:** `/plugin marketplace add MotexAI/motex-claude-plugin`, then `/plugin install motex@motex`.
- **Just the connector, in any assistant:** https://motex.ai/conectar

## Data

The plugin stores nothing by itself and runs no code: it is instructions plus the reference to the connector. What you ask Claude about your cases goes only to the Motex server at `legal.motex.ai`, authenticated with OAuth. Motex reads public PJUD cases; it cannot access sealed or family-court cases. Privacy policy: https://motex.ai/en/privacy. Support: contacto@motex.ai.

---

## Motex para Claude (español)

Motex sigue tus causas del Poder Judicial de Chile (PJUD) y este plugin lo trae a tu conversación con Claude. Agrega una causa por su RIT y tribunal y en segundos tienes su carátula, su etapa y un link a la ficha en Motex; ponte al día con lo que vence y lo que se movió en tu cartera; prepara una audiencia leyendo el expediente; y deja las tareas y plazos en tu calendario de Motex.

### Qué incluye

- **Conector de Motex** (`https://legal.motex.ai/api/mcp`): al conectarlo, entras con tu cuenta de Google. Si todavía no usas Motex, se crea tu espacio con el plan gratis (hasta 10 causas). Si tu estudio ya usa Motex, entras a su cartera.
- **Skills:**
  - `seguir-causa`: busca, registra y explica una causa por su RIT.
  - `ponerse-al-dia`: lo urgente, lo que se movió y lo pendiente de tu cartera.
  - `preparar-audiencia`: un repaso de la causa antes de una audiencia, con sus fuentes.
  - `plan-de-motex`: qué incluye tu plan y qué hacer cuando llegas a un tope.
- **Comandos:** `/motex:mi-dia` y `/motex:agregar-causa <RIT> <tribunal>`.

Claude confirma antes de los cambios en Motex que no pediste de forma explícita, como registrar una causa que solo mencionaste. Un cambio que pediste tú se hace sin volver a preguntar.

### Instalar

- **claude.ai y Cowork:** búscalo en el directorio de plugins, o en Customize > Plugins > Add > Add marketplace con `MotexAI/motex-claude-plugin`.
- **Claude Code:** `/plugin marketplace add MotexAI/motex-claude-plugin` y después `/plugin install motex@motex`.
- **Solo el conector, en cualquier asistente:** https://motex.ai/conectar

### Datos

El plugin no guarda nada por sí mismo y no ejecuta código: son instrucciones y la referencia al conector. Lo que le pides a Claude sobre tus causas viaja solo al servidor de Motex en `legal.motex.ai`, autenticado con OAuth. Motex lee causas públicas del PJUD; no accede a causas reservadas ni de familia. Política de privacidad: https://motex.ai/es/privacidad. Soporte: contacto@motex.ai.
