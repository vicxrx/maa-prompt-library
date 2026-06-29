# Prompt Library Notes

This folder holds working notes about how the prompt library is structured, how prompts are authored, and small implementation audits.

## What to know

- The app is driven by a single source file: [index.html](../index.html).
- Prompt data is embedded directly in the `const data = [...]` array inside that file.
- Each prompt entry uses four core fields:
  - `title`
  - `tool`
  - `source`
  - `prompt`
- Categories also include a short `desc` field used on the homepage cards.

## Wording pattern

Most prompts in this library follow a practical structure:

1. State the context.
2. Ask for a clear task.
3. Add focus or quality constraints.
4. Specify the output format.
5. End with a bracketed placeholder where needed.

Examples of recurring language patterns:

- "Help me..."
- "Write..."
- "Review..."
- "Analyse..."
- "Explain..."

The tone is plain-English, business-friendly, and action-oriented. It favors clarity over cleverness and usually asks for a tangible output such as bullet points, a table, a summary, recommendations, or code.

## Important implementation detail

Square brackets are the Personaliser's variable system. Anything written as `[like this]` becomes a fillable field on the Personaliser page, so placeholder wording should stay user-friendly and specific.

## Related docs

- [Authoring guide](./authoring-guide.md)
- [Personaliser polish audit](./audits/personaliser-polish-audit.md)
- [Design references](./design-references/README.md)
