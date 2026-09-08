# ILSANG_V1_SPEC

Status: CANONICAL V1 ARCHITECTURE
Updated: 2026-09-09

## 1. Product

Default publishable episode:

- 1 COVER
- 6 BODY slides
- final page size 1080×1350 (4:5)
- BODY artwork originates from one text-free 2×3 master board
- COVER is a distinct composition by default
- final lettering remains editable

The default page count is a production format, not an editor capability ceiling. ToonDesk may add/delete/duplicate pages through explicit user editing.

## 2. Frozen architecture

The following are V1 defaults:

1. board-first coherence for BODY artwork;
2. one text-free 2×3 BODY master board;
3. actual panel-boundary extraction rather than blind equal slicing;
4. no artwork stretch during 4:5 fit;
5. distinct COVER artwork/composition by default;
6. quality-first `PRESENTATION_MASTER_DRAFT` before editable scene reconstruction;
7. approved artwork and literal copy preserved through reconstruction;
8. `EDITOR_SCENE_MODEL_V1` / ToonDesk-compatible editable output;
9. minimal publish-blocking QC rather than a sprawling permanent gate system;
10. background omission/minimalism as the production default.

## 3. Fluid creative space

The architecture must not hard-code:

- exact camera per panel;
- exact expression intensity;
- exact joke structure;
- exact location;
- exact dialogue length;
- exact bubble coordinates;
- exact cover layout;
- exact character lineup;
- exact drawing style.

The six-beat comedy rhythm in `CONTENT_SYSTEM.md` is a planning heuristic, not a compulsory template.

## 4. Visual authority status

At this revision:

- character authority: `PENDING`
- drawing-style authority: `PENDING`
- production carrier: `PENDING`

No previously generated candidate becomes authority merely because it exists in chat history.

Production artwork is blocked until these are user-approved.

## 5. Content identity

The project covers ordinary life for Korean 20–30s, with five default content pillars:

- work
- money/consumption
- dating/relationships
- friends
- living alone/everyday life

The goal is not diary transcription. Each episode should behave like a compact situation comedy: one recognizable situation, escalation or contrast, and a readable payoff.

## 6. Copy

Approved literal copy is authority.

Image-model glyphs, spelling, or baked text never override approved copy.

Prefer:

- actual spoken Korean;
- short reactions;
- community/thread-like natural phrasing when appropriate;
- visual implication over explanatory narration.

Avoid:

- literary exposition;
- redundant captions that restate visible information;
- forced slang in every line;
- mechanically identical punchline syntax across episodes.

## 7. Background and prop budget

`BACKGROUND_MINIMALISM_POLICY.md` is canonical.

Background complexity is a cost to coherence and character quality. Add only what is necessary for comprehension or the joke.

## 8. Runtime carrier policy

Once approved, the carrier is a runtime delivery asset, not story authority.

For ChatGPT-app production, attaching the approved carrier once at the beginning of the image-generation phase is the normal fallback if repository-direct image binding is unavailable.

A new chat requires a fresh runtime attachment unless direct binding is actually verified.

## 9. Presentation architecture

Normal production sequence:

`BOOT + PLAN → STORYBOARD_USER_GATE → BOARD → COVER/EXTRACT/FIT → PRESENTATION_MASTER_DRAFT → FINAL_PUBLISH_GATE → EDITABLE_RECONSTRUCTION/PARITY_QC`

The presentation master is allowed to be visually richer and more organic than generic editor presets.

Editable reconstruction must follow the approved presentation; it must not simplify the design merely to fit the editor.

If ToonDesk cannot express an approved presentation decision, surface the capability gap or manual adjustment need.

## 10. State authority

Repository resume authority:

- `CURRENT_STATE.md`

Episode resume authority, once an episode is active:

- `episodes/<episode_id>/state.json.exact_next_action`

Do not reconstruct obsolete state from Git history unless explicitly asked.
