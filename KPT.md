# KPT 회고

**프로젝트:** UnitConverter_25 · Session 3

| | 요약 |
|---|---|
| **K** | 커밋 리뷰 · ARRR · C2C · Mom Test→AC · Dual-Track · 구조화 프롬프트 · pytest+GM |
| **P** | 리뷰·PRD 지연 · 개념 선행 부족 · Mom Test≠강의 FR · PRD/NFR 혼선 · 교차검증 피로 |
| **T** | 리뷰 시한 · 커밋→리뷰→다음 · Mom Test→AC→FR→추적표 · PRD·SSOT · 프롬프트 표준 |

---

## K — Keep

- 단계별 **커밋 리뷰**로 구조·의도 이해
- **ARRR** 사이클 가치 체감
- **C2C** — PRD·Rules·테스트로 개념→코드 추적
- **Mom Test → AC** — 진짜 문제(확신·20분) 우선
- **Dual-Track** — Boundary(U-*) / Domain(D-*)
- **변환 SSOT** — meter base · `constants.py` · ft↔yd meter 경유
- **구조화 프롬프트** — Phase/Layer/Track · 제약 · Budget
- **지시 체계** — `.cursorrules` · Skill · `/tdd-red` · `/review-ecb`
- **Ask + 수정 없음** · **pytest Green** · **GM 불변**

---

## P — Problem

- **리뷰 적체** · **PRD 보완 지연** → 구현·검증 미완
- **개념 선행 부족** — C2C·TDD·ECB 숙지 전 실습
- **Mom Test FR ≠ 강의 추적표 FR** — 확신·1회 vs 파싱·3줄·OCP
- **PRD NFR 혼선** — Rule/TDD/범위가 NFR에 섞임
- **Starter 3줄 vs AC-2 1회 1결과** 충돌
- **워크북 잔재** — Magic Square·cubit·json 등
- **프롬프트·개념 미숙** → 레이어·GM·naming 위반
- **AI 문서 교차검증 피로** · **Ground Rule 미명시**

---

## T — Try

- **리뷰 완료 시한** · **커밋 → 리뷰 → 다음 단계**
- **Mom Test → AC → FR → 추적표** 순서 고정
- **PRD 0.2** — SSOT · C2C 추적표 · EXT(P1) 격리 · 한글 간결
- 강의-only → **RED**(U-OUT-01) 또는 **EXT** (cubit · json · 3줄)
- 신규: **Mom Test → PRD → TRACEABILITY → ARRR → TDD**
- **ARRR 종료마다** Report·Transcript 저장
- **프롬프트 템플릿** + **Ground Rule** + **SSOT** (`PRD.md` · `reference.md`)
- **Phase 종료** — Ask 검토 → Agent 수정
- 현업 **C2C·Dual-Track** 반복 적용
