# KPT 회고

## K — Keep (유지할 것)

- **단계별 커밋 리뷰**로 실습 코드만으로는 부족했던 구조·의도 이해가 가능했다.
- **ARRR**(문제 정의 → 요구 → 구현 → 검증) 사이클의 중요성을 체감했다.
- **C2C 추적성**: 프롬프트 한 줄이 아니라 **PRD·Rules + 테스트 하네스**가 있어야 개념이 코드까지 이어진다.
- **구조화된 프롬프트**: Phase/Layer/Track, 슬래시 커맨드, 제약(코드 수정 금지, `tests/`만 변경, Golden Master 불변) 명시.
- **범위 제한**: 리팩터 시 대상·방법·Budget(파일·클래스·메서드 상한)으로 public API·회귀 통과가 안정적.
- **지시 체계**: `.cursorrules`, Skill, Hook, `reference.md`로 짧은 지시(`/green-minimal` 등)도 일관된 결과.
- **Ask 모드 + 「수정 없음」 검토**: 구현 전·후 점검 분리가 효과적.
- **pytest Green + Golden Master 불변**: REFACTOR·GUI 변경 시에도 회귀 기준이 명확해 구조 개선에 자신감을 준다.

## P — Problem (문제·어려움)

- 리뷰 요청이 몰려 **일부 리뷰 미완료**.
- **PRD 보완 지연**으로 구현·검증까지 이어가지 못함.
- **개념 없이 실습 시작** → 개념 이해와 강의 진행을 동시에 하기 어려움.
- C2C·TDD·ECB 등 **핵심 개념 선행 숙지 부족**으로 실습 깊이 제한.
- AI가 간단한 프롬프트에도 답해 **구체적 프롬프트 작성 연습**이 어려움.
- TDD·ECB·Dual-Track·Golden Master 이해가 얕으면 **계약·레이어 위반**(naming drift, 함수명 혼동, GM 범위 오해 등) 발생.
- AI 문서 완성도가 높아 **교차 검증 필수**이나, 문서 증가 시 **검증 피로** 커짐.
- **프로젝트 고유 Ground Rule**(PR base 브랜치, 폴더명 등)을 프롬프트에 넣지 않으면 AI가 추론 못 해 **후속 수정 반복**.

## T — Try (다음에 시도할 것)

- **리뷰 완료 시한** 설정, 펜딩 축소.
- **커밋 → 리뷰 완료 → 다음 단계** 순서 고정.
- 본업 복귀 후 **C2C·ARRR·ECB·Dual-Track TDD**를 실제 프로젝트에 반복 적용.
- 하반기 신규 프로젝트: **Mom Test → PRD → TRACEABILITY → ARRR → TDD** 순 계획·꼼꼼 리뷰.
- ARRR 종료마다 **Report·Transcript 저장**으로 개념~결과 추적 기록.
- **프롬프트 표준화**: 대상 / 방법 / Budget / 게이트 템플릿 기본 적용.
- **팀 Ground Rule**을 프롬프트·PR에 명시(phase별 base 브랜치, Summary/Test plan/pytest, GM·assert 완화·skip 금지, 변경 범위·Budget).
- **Phase 종료 루틴**: GREEN·REFACTOR 직후 Ask 검토 → Agent 수정 2단계.
- 작업 전 **SSOT 참조**(`reference.md`, `PRD.md`, `golden/manifest` 등).
- 설계 의견을 프롬프트에 명시(레이어 배치 이유, 유지 계약, 비수정 범위).

---

## 한눈에 보기

| | 요약 |
|---|---|
| **K** | 단계별 커밋 리뷰 · ARRR · C2C(PRD+Rules+테스트) · 구조화 프롬프트 · Ask 검토 · pytest+GM |
| **P** | 리뷰·PRD 지연 · 개념 선행 부족 · 프롬프트·개념·교차검증 피로 · Ground Rule 누락 |
| **T** | 리뷰 시한 · 커밋–리뷰–다음단계 · ARRR·추적 기록 · 프롬프트·SSOT·2단계 루틴 표준화 |
