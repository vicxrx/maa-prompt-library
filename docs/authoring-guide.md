# Prompt Authoring Guide

This guide explains how to add or edit prompts so they match the current library style and work cleanly with the Personaliser.

## Where prompts live

All prompts live in the `const data = [...]` array in [index.html](../index.html).

Each category looks like:

```js
{
  category: "Category name",
  desc: "Short homepage description.",
  prompts: [
    {
      title: "Prompt title",
      tool: "ChatGPT, Copilot, Claude",
      source: "Starter prompt",
      prompt: "Prompt text goes here. [placeholder]"
    }
  ]
}
```

## Core writing style

Use wording that is:

- practical
- direct
- easy to scan
- low-jargon
- outcome-focused

The best prompts in this library usually do four things well:

1. Set the context quickly.
2. Ask for one clear job.
3. Add useful constraints.
4. Tell the model what shape the answer should take.

## Recommended prompt shape

Use this pattern when writing new prompts:

```text
I’m working on [context].
Help me [task].
Focus on [what matters most].
Present the output as [format].
[paste content / data / notes]
```

Not every prompt needs every line, but this structure is a strong default.

## Placeholder rules

Bracketed text powers the Personaliser, so placeholders should be written for humans, not developers.

Use:

- `[topic]`
- `[audience]`
- `[paste draft]`
- `[context or goal]`

Avoid:

- `[]`
- `[var1]`
- `[input]`
- duplicate labels that mean different things

## Title guidance

Keep titles:

- short
- action-led
- specific enough to scan in a list

Good examples:

- `Summarise for leadership`
- `Fix bugs step by step`
- `Analyse churn drivers`

## Tool field guidance

The `tool` field is display and search metadata. It does not change prompt behavior.

Keep the format consistent:

- separate tool names with a comma and space
- use the naming already present in the library

Examples:

- `ChatGPT, Copilot, Claude`
- `Snowflake Cortex`
- `Adobe`

## Source field guidance

Use one of the current labels:

- `Starter prompt`
- `Team submission`

Keep these exact unless the app is updated to support new badge types.

## Tone checklist

Before adding a prompt, check that it:

- sounds helpful, not academic
- asks for useful output, not generic commentary
- avoids unnecessary role-play unless it adds value
- uses plain-English instructions
- tells the model what "good" looks like

## Output-format prompts work best

The library is strongest when prompts ask for structured outputs like:

- a table
- bullet points
- a short summary
- recommended actions
- a step-by-step plan
- corrected code with explanation

## Common mistakes to avoid

- vague prompts with no outcome format
- placeholders that are too abstract
- titles that are too broad to scan quickly
- prompts that ask for too many separate jobs at once
- inconsistent `tool` formatting

## Quick authoring checklist

- Add the prompt to the right category in [index.html](../index.html).
- Keep the wording concise and task-focused.
- Use readable square-bracket placeholders.
- Confirm the `tool` label matches existing naming.
- Confirm the `source` label is one of the two current values.
- Test the prompt in the Personaliser if it uses placeholders.
