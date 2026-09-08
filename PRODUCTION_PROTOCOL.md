# PRODUCTION_PROTOCOL

Status: CANONICAL CHATGPT-APP PRODUCTION FLOW
Updated: 2026-09-09

## Current block

Production image generation is currently blocked because the character/art system is not approved.

This protocol becomes executable after the visual lock is established.

## A. Boot

1. Read `AGENTS.md`.
2. Read `CURRENT_STATE.md`.
3. Read `ILSANG_V1_SPEC.md`.
4. If an episode is active, read its `state.json` and follow `exact_next_action`.
5. If repository state cannot be verified, fail closed.

## B. Plan and storyboard

Input may be:

- a user-provided situation;
- a short premise;
- a source anecdote;
- or an AI-proposed everyday situation.

Create:

- premise
- content pillar(s)
- characters/roles needed
- six-panel beat plan
- draft literal copy
- continuity notes
- optional copy-space / focal-area notes

Do not bake exact final lettering coordinates into the storyboard.

### USER GATE 1 — STORYBOARD

The user may approve, edit, or reject the story/copy.

Do not generate BODY artwork before this approval.

## C. Runtime visual binding

After a visual carrier is eventually approved:

- use only the approved production carrier;
- in ChatGPT-app mode, attach it once when beginning image generation if repository-direct binding is not actually available;
- do not ask for it again every turn in the same chat;
- do not use rejected candidate sheets.

## D. BODY board

Generate one text-free 2×3 master board containing S01–S06.

Requirements:

- no dialogue, captions, SFX, labels, or panel numbers inside generated artwork;
- obey approved visual authority;
- obey `BACKGROUND_MINIMALISM_POLICY.md`;
- preserve character identity across all occupied cells;
- vary staging/camera/acting only as the storyboard requires;
- avoid unnecessary multi-person physical contact when the joke does not require it;
- hands/arms/props must remain semantically consistent.

The board is a coherence batch, not the publish canvas.

During initial visual calibration, a temporary user BOARD/style check may be used. It should be removed from routine production once the style is stable.

## E. Extract and fit

Detect actual panel boundaries.

Do not assume perfect equal 2×3 slicing if the generated border positions differ.

Extract S01–S06 and fit each to 1080×1350 without stretching artwork.

Crop/reframe is allowed; geometric distortion is not.

## F. COVER

Create a separate 4:5 cover composition by default.

The cover:

- communicates the premise immediately;
- does not merely duplicate a BODY frame;
- leaves useful negative space for title;
- follows the same approved visual authority;
- follows background minimization.

BODY reuse for COVER requires an explicit editorial decision.

## G. PRESENTATION_MASTER_DRAFT

Before ToonDesk reconstruction, create a quality-first visual draft of the final carousel presentation.

It owns presentation intent such as:

- bubble silhouette
- tail character
- typography character
- explicit line breaks
- relative placement
- emphasis
- SFX treatment
- cover title composition

Literal copy still comes from the approved plan.

This stage is deliberately not constrained to generic editor defaults.

### USER GATE 2 — FINAL PUBLISH

Show the 7-page final presentation preview.

The user approves/revises visual presentation and copy.

## H. Editable reconstruction

After approval, reconstruct the accepted artwork/copy/presentation into ToonDesk-compatible editable scene JSON using `templates/ILSANG_PRESENTATION_SHELL_V1.json`.

Preserve:

- accepted artwork identity/provenance
- exact literal copy
- page IDs/object IDs where available
- explicit line breaks
- bubble/tail geometry
- typography intent
- crop
- user manual overrides

Do not flatten the page and call it editable.

## I. Parity QC

Compare reconstructed output against the approved presentation master.

If the editor cannot reproduce an approved presentation decision:

- improve/extend the scene expression if appropriate; or
- surface a manual adjustment need.

Do not silently downgrade the presentation to a generic bubble/font/layout.

No routine extra user approval is required after parity if the reconstruction is materially equivalent.

## J. Persist

Persist canonical episode state/artifact references and a run receipt before declaring `DONE`.

Final PNG is a publish derivative. Editable project scene data is the canonical presentation artifact.
