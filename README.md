# ui-components

A small personal **component library**: reusable interface pieces, each defined
once and shared across projects (Apps 1–3 and beyond) instead of rebuilt per app.
This is the same single-source-of-truth / DRY discipline applied to the data
layer, lifted up to the level of UI controls.

Each component is a **single, self-contained HTML file** you can open in a browser
to see it working, and copy from. Colours and sizing are exposed as CSS variables
at the top of each file (a small "theme block"), so reusing a component in another
app is a matter of changing those variables — never editing the component's guts.

## How to use an entry

1. Open the file in a browser to see the component live and try its states.
2. Copy the marked block: `<!-- ==== COMPONENT — copy from here … to here ==== -->`.
   That block is the whole thing (markup + its scoped CSS + its script).
3. Paste it into the target app, and adjust the theme variables to match that app.

## Index

| File | Component | Use it for |
|------|-----------|------------|
| `toggle-slide.html`  | Sliding two-option switch, with a check on the active side | A set-and-forget **mode/preset selector** (e.g. In order / Shuffle). The motion signals "a switch, not a button." |
| `toggle-welded.html` | Static two-segment control, active segment "welded" to the centre seam, with a check | A mode selector where you want a firmer, "locked-in-place" feel instead of motion. |

## Notes

- Both toggles are two-option. The check mark rides with the selection and mirrors:
  it sits **before** the first option's label and **after** the second's, so the
  checks bookend the control.
- The active fill uses the accent colour; the two designs differ only in *feel*
  (sliding vs. welded), so they're interchangeable at the markup level.
- `toggle-slide.html` is the one shipping in App 1 (Nekudot). `toggle-welded.html`
  is kept here for reuse in a later app.

## Provenance

Designed collaboratively: the direction (a set-and-forget selector, visually
distinct from action buttons; the recessed/welded treatments; the mirrored checks)
was mine; the implementations were drafted by Claude to that direction. See each
app's decision log for the specific entries.
