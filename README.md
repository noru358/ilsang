# ilsang

한국 20–30대의 일상을 짧은 상황 코미디로 만드는 Instagram comic project.

이 저장소가 프로젝트 authority다. ToonDesk는 편집/렌더링 엔진이며 프로젝트의 스토리·승인·레이아웃 기본값을 소유하지 않는다.

## Canonical boot

새 세션 또는 재개 시 반드시 다음 순서로 읽는다.

1. `AGENTS.md`
2. `CURRENT_STATE.md`
3. `ILSANG_V1_SPEC.md`
4. 현재 작업과 직접 관련된 authority 문서

`CURRENT_STATE.md`의 `exact_next_action`이 재개 지점이다.

## Product default

- Instagram carousel
- COVER 1 + BODY 6
- BODY는 text-free 2×3 master board에서 파생
- 최종 페이지 1080×1350 (4:5)
- quality-first `PRESENTATION_MASTER_DRAFT`를 먼저 승인
- 승인된 artwork/copy/presentation intent를 ToonDesk용 editable scene으로 재구성
- editable reconstruction이 창작 품질을 낮추는 방향으로 upstream design을 단순화해서는 안 됨
- 배경은 가능한 한 생략하고, 상황 이해에 필요한 최소 정보만 사용

## Content scope

기본 소재 축:

- 회사
- 돈/소비
- 연애/썸/인간관계
- 친구
- 자취/일상

장르 정체성은 “일기”보다 “고정 세계관 안의 짧은 생활 시트콤”에 가깝다. 한 화는 하나의 사건/상황에 집중하고, 6컷 안에서 읽히는 명확한 코미디 리듬을 갖는다.

## Current visual status

캐릭터 설계와 production drawing style은 아직 재작업 대상이다.

따라서 현재 저장소는 다음을 authority로 선언하지 않는다.

- 캐릭터 이름/외형/성격 조합
- 고정 그림체
- production style carrier
- character carrier

이 항목들은 사용자 승인 전까지 `PENDING`이다. 이전 채팅에서 생성된 캐릭터/작화 시안은 production reference가 아니다.

## Main documents

| Path | Role |
|---|---|
| `AGENTS.md` | fail-closed boot/execution contract |
| `CURRENT_STATE.md` | 현재 상태와 exact next action |
| `ILSANG_V1_SPEC.md` | V1 고정/유동 경계 |
| `CONTENT_SYSTEM.md` | 소재·스토리·대사 authority |
| `BACKGROUND_MINIMALISM_POLICY.md` | 배경/소품 최소화 정책 |
| `PRODUCTION_PROTOCOL.md` | 실제 ChatGPT-app 제작 절차 |
| `prompts/` | 단계별 production prompt |
| `templates/ILSANG_PRESENTATION_SHELL_V1.json` | ToonDesk용 프로젝트 기본 profile |
| `episodes/` | 승인된 에피소드 상태/산출물 |

## Reference repos

다른 저장소는 구조 참고용으로 읽을 수 있지만, 이 프로젝트 작업 중에는 명시적 요청 없이 수정하지 않는다.

- `noru358/jipbap`
- `noru358/Toondesk`
- `noru358/aitoon`
- `noru358/instatoon`

특히 JIPBAP의 board-first / presentation-master-first / editable-reconstruction 경험과 ToonDesk의 profile/scene model을 참고하되, 음식툰 고유 규칙이나 과거 legacy state machine을 그대로 복제하지 않는다.
