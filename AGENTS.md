# AGENTS.md

Status: ACTIVE
Project: ilsang

## 1. Fail-closed boot

Before changing project state or producing episode artwork:

1. read `CURRENT_STATE.md`;
2. read `ILSANG_V1_SPEC.md`;
3. read only the task-relevant authority documents;
4. verify that the repository state and the user's current instruction do not conflict.

If canonical state cannot be read, stop rather than guessing.

## 2. Repository boundary

Write changes for this project only to `noru358/ilsang` unless the user explicitly authorizes another repository.

The following repositories may be read for patterns/compatibility, but must not be modified as a side effect of ilsang work:

- `noru358/jipbap`
- `noru358/Toondesk`
- `noru358/aitoon`
- `noru358/instatoon`

ToonDesk is a downstream editor/renderer. It does not own ilsang story, approval, or project-default presentation decisions.

## 3. Current visual lock status

Character design and production drawing style are currently `PENDING`.

Until the user explicitly approves a new character/art system:

- do not treat prior generated character sheets as references;
- do not register a style carrier;
- do not generate production episode artwork;
- do not infer character identity, costume, palette, proportions, or drawing language from rejected candidates.

Content/planning/editor architecture work may proceed independently.

## 4. Production default

After visual authority is locked, normal production is:

`BOOT → PLAN/STORYBOARD → USER STORYBOARD GATE → text-free 2×3 BODY BOARD → COVER → EXTRACT/FIT → PRESENTATION_MASTER_DRAFT → USER FINAL PUBLISH GATE → EDITABLE_RECONSTRUCTION → PARITY_QC → DONE`

The storyboard gate is the meaningful creative checkpoint before artwork.

During initial style calibration only, a temporary BOARD/style approval may be used. Once visual delivery is stable, it should not become a permanent extra gate.

## 5. ChatGPT-app runtime image binding

Repository storage of an image does not guarantee that the ChatGPT image runtime will receive it as a visual reference.

When an approved runtime carrier exists:

- store/register its canonical identity in this repo;
- in a normal ChatGPT-app production chat, attach the approved carrier once when image generation begins unless the runtime can actually bind the repository asset directly;
- do not require the user to re-attach it every turn in the same chat;
- the carrier is style/identity delivery only and never owns story, camera, staging, copy, or layout.

## 6. Background discipline

Follow `BACKGROUND_MINIMALISM_POLICY.md`.

Default to no background or only the smallest context cue needed to understand the joke. Decorative completeness is not a quality target.

## 7. Approval identity

Never substitute:

- a newly generated board for an approved board,
- a BODY cell for an approved distinct COVER,
- generic ToonDesk defaults for an approved presentation master,
- image-model text for approved literal copy.

Presentation-only changes do not authorize artwork regeneration.

## 8. Resume behavior

`CURRENT_STATE.md` is the repository-level resume pointer.

Episode-specific work, once episodes exist, must also use `episodes/<id>/state.json.exact_next_action`.

Do not declare `DONE` if canonical artifacts or receipts have not been persisted.
