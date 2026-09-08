# RECONSTRUCTION_PROMPT

Reconstruct an approved ilsang `PRESENTATION_MASTER_DRAFT` into ToonDesk-compatible editable scene data.

Use `templates/ILSANG_PRESENTATION_SHELL_V1.json` as the project default profile, not as a capability ceiling.

## Preserve

- accepted artwork source/provenance
- exact approved literal copy
- explicit line breaks
- crop/FIT
- bubble body geometry
- rich tail geometry
- typography intent and resolved fallback information when available
- object position/scale/rotation/z-order
- stable IDs
- property-level manual overrides on an existing scene

## Do not

- flatten the whole page and call it editable;
- silently replace a COVER source with a BODY cell;
- silently regenerate artwork;
- silently replace approved copy with image-model text;
- silently simplify approved bubble/tail/typography design to a generic preset.

If parity is not representable, surface the capability gap or manual adjustment requirement.

Presentation-only changes never authorize artwork regeneration.
