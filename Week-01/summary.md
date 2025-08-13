# Week-01 (Metal Head) — Summary

※비디오(mp4) 증거는 용량 상의 문제로 미리보기 지원불가함※

<br>

## 개요 (Overview)
- **빌드/버전 (Build/Version)**: 2025-01-03 itch-setup.exe build

- **플랫폼 (Platform)**: Windows (itch.io)

- **타임박스 (Timebox)**: 2025-08-11 19:30–21:00 (90m) (+2m 초과)

- **차터 (Charter)**: 실행→1스테이지→클리어→종료 루프, 조작, 전투, 성장/업그레이드, 체크포인트, 옵션, 창↔전체

<br>

## 커버리지 및 결과 (Coverage & Results)
| TC | Title (요약) | Status | Linked Bugs |
|---|---|---|---|
| TC-01 | 실행/종료 스모크 | **Fail** | BUG-01, BUG-02 |
| TC-02 | 이동/점프/가장자리/카메라 | **Fail** | BUG-04, BUG-05, BUG-09 |
| TC-03 | 낙사/리스폰/체크포인트 | **Fail** | BUG-01 |
| TC-04 | 전투(공격/피격/AI) | **Fail** | BUG-03, BUG-06, BUG-10, BUG-11, BUG-12 |
| TC-05 | 1단 업그레이드(더블점프) | **Fail** | BUG-07, BUG-13 |
| TC-06 | 2단 업그레이드(대쉬) | **Fail** | BUG-08, BUG-14 |
| TC-07 | 스테이지 완주/엔드 트리거 | **Pass w/ Issues** | BUG-15 |
| TC-08 | 창↔전체/포커스 | **Pass** | — |

<br>

## 상위 5개 이슈 (Top 5 Issues) (Risk-ordered)
| ID | Risk | Severity | Repro | Impact (요약) | Evidence |
|---|---|---|---|---|---|
| BUG-01 | 진행 차단 | 매우 심각(Fatal) | 3/3 | 사망 UI→옵션 후 “다시 실행” 시 진행 불가 | `evidence/videos/W01_BUG_01.mp4` |
| BUG-02 | 크래시 | 매우 심각(Fatal) | 3/5 | 종료 후 itch 재실행 오류 | `evidence/videos/W01_BUG_02.png` |
| BUG-03 | 진행 차단 | 심각(No Workaround) | 3/3 | 데몬(적) 추적 시스템 오류 | `evidence/videos/W01_BUG_03.png` |
| BUG-04 | 충돌 | 보통(Workaround) | 3/5 | 가장자리 낙하 판정 모호 | `evidence/screenshots/W01_BUG_04.png` |
| BUG-06 | 전투판정 | 보통(Workaround) | 3/3 | 보스전 가장자리에서 공격 무효/화면 이탈 | `evidence/videos/W01_BUG_06.png` |

<br>

## 하이라이트 (Highlights) (Good/Bad)
- **Good**: Alt+Enter/Alt+Tab 포커스 안정적(TC-08 Pass), 전투 기본 히트/사운드 피드백 확인
- **Bad**: Death-state 게이팅 다수, 보스전 가장자리 익스플로잇, 리런치 오류

<br>

## 프로젝트 상태 (Project Status) (종료)
- 상태 (State): Completed (향후 테스트 계획 X)
- 타임박스 (Timebox): 2025-08-11 19:30–21:00 (90m) (+2m 초과)
- 커버리지 범위 (Scope Covered): TC-01~08
- 인수인계 (Hand-off): 문서/증거 경로 유지, 재현 절차 각 BUG 리포트에 포함

<br>

## 제안 수정 초점 (Suggested Fix Focus, Optional)
> Risk → Severity → Repro 기준 Top 5

1) **BUG-01** — 사망 UI→옵션 후 “다시 실행” 진행 불가 **[매우 심각(Fatal), Repro 3/3]**  
   - Acceptance: “다시 실행” 즉시 인게임 복귀, UI/입력/사운드 잔존 없음  Evidence: `evidence/videos/W01_BUG_01.mp4`

2) **BUG-02** — 종료 후 itch 재실행 오류 **[매우 심각(Fatal), Repro 3/5]**  
   - Acceptance: 정상 종료 뒤 재실행 시 메인 화면 진입, 오류 로그 없음  Evidence: `evidence/videos/W01_BUG_02.png`

3) **BUG-03** — 데몬(적) 추적 시스템 오류 **[심각(No Workaround, Repro 3/3]**  
   - Acceptance: 정상 추적 시스템, 발판 없을 시 추격 불가  Evidence: `evidence/videos/W01_BUG_03.png`

4) **BUG-04** — 가장자리 낙하 판정 모호 **[심각(No Workaround, Repro 3/5]**  
   - Acceptance: 에지 끼임/허공 낙하/관통 없음(이동·점프·대쉬 포함)  Evidence: `evidence/screenshots/W01_BUG_04.png`

5) **BUG-06** — 보스전 가장자리에서 공격 무효/화면 이탈 **[보통(Workaround), Repro 3/3]**  
   - Acceptance: 경계에서 충돌·공격·카메라 정상, 화면 밖 이탈 불가  Evidence: `evidence/videos/W01_BUG_06.png`

<br>

## 링크 (Links) (Week-01 Docs)
- [test-basis.md](./test-basis.md)
- [env-matrix.md](./env-matrix.md)
- [session-notes.md](./session-notes.md)
- [test-cases.md](./test-cases.md)
- [bug-report.md](./bug-report.md)

<br>

## 증거 목록 (Evidence Index)
- Screenshots: `Week-01/evidence/screenshots/`
- Videos: `Week-01/evidence/videos/`

<br>
