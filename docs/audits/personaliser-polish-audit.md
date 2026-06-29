# Personaliser Polish Audit

## What changed

- Replaced Personaliser-specific uses of `"Courier New"` with the app's existing typography stack.
- Increased contrast for preview text and user-entered values.
- Styled empty and completed variables to align more closely with the Library page treatment.
- Added a `Currently editing: [prompt title]` label above the live preview.
- Updated the empty state and simplified variable input placeholders.
- Slightly increased spacing between selector categories and increased input padding.

## What was checked

- Personaliser-only CSS and markup changes stayed scoped to the Personaliser section in [index.html](../../index.html).
- Existing layout order was preserved:
  - Fill in the blanks
  - Live preview
- Existing Personaliser functionality was preserved:
  - prompt selection
  - variable extraction
  - live preview updates
  - copy prompt behavior

## Known issues

- The app still contains some legacy encoding artifacts in unrelated parts of `index.html`.
- Visual verification was limited to code inspection in this pass; a browser spot-check is still recommended.
- Some non-Personaliser areas still use `"Courier New"` intentionally or historically and were left untouched.

## Suggested next steps

- Open the page locally and spot-check the Personaliser on desktop and mobile widths.
- Decide whether the remaining `"Courier New"` usage elsewhere in the app should be standardized later.
- Consider splitting prompt data out of `index.html` if the library grows much larger.
