# Game QA Portfolio
민규의 게임 QA 포트폴리오

<br>

> 이 레포는 주차별로 실제 테스트 산출물(근거, 환경, 세션 로그, TC, 버그, 요약)을 기록합니다.

<br>

## 빠른 안내(30초) (Quick Guide)
- **읽는 법(How to read)**: 각 주차의 `summary.md` → 상세 문서로 이동

- **문서 규칙 (Document Rules)**:
  - **파일명(File Name)**: `kebab-case` (예: `test-cases.md`)
  - **ID 규칙(ID Rules)**: `TC-XX`, `BUG-XX` (예: `TC-03`)

- **증거 위치 (Evidence Location)**: `Week-XX/evidence/` (스크린샷·영상·로그)

<br><br>

<details>
<summary><b>문서 구성 (Document Structure)</b></summary>

- `test-basis.md` : 테스트 설계 근거

- `env-matrix.md` : 실행 환경 표(OS/해상도/입력/빌드/버전)

- `session-notes.md` : 세션 차터·타임박스·진행 로그

- `test-cases.md` : 테스트 시나리오

- `bug-report.md` : 결함 원장

- `summary.md` : 주간 요약

</details>

<br><br>

## Weeks

### Week-00 (테스트용 문서)
- [x] [test-basis.md](Week-00/test-basis.md)
- [x] [env-matrix.md](Week-00/env-matrix.md)
- [x] [session-notes.md](Week-00/session-notes.md)
- [x] [test-cases.md](Week-00/test-cases.md)
- [x] [bug-report.md](Week-00/bug-report.md)
- [x] [summary.md](Week-00/summary.md)

### Week-01 (Metal Head)
- [x] [test-basis.md](Week-01/test-basis.md)
- [x] [env-matrix.md](Week-01/env-matrix.md)
- [x] [session-notes.md](Week-01/session-notes.md)
- [x] [test-cases.md](Week-01/test-cases.md)
- [x] [bug-report.md](Week-01/bug-report.md)
- [x] [summary.md](Week-01/summary.md)

<br>

## Conventions
- **TC/BUG ID**: `W01-TC-01`, `W01-BUG-02`

- **심각도(Severity)**: 치명적(show stopper) / 매우 심각(Fatal) / 심각(No Workaround) / 보통(Workaround) / 경미(Cosmetic)

- **우선순위(Priority)**: 즉시 해결(Resolve immediately) / 주의 요망(Give high attention) / 대기(Normal queue) / 낮은 순위(Low priority)
  - **_test-cases에서의 우선순위 : 매우 높음 (very high) / 높음 (high) / 보통 (Medium) / 낮음 (Low)_**

- **증거(Evidence)**: `W01_BUG_02.png`, `W01_TC_04.mp4`

<br>

## Changelog
- 2025-08-09: 초기 구조 정리, 파일명 통일, 주차 링크 추가
- 2025-08-10: Week-01 옆 게임명 추가, test-cases에서의 우선순위 추가, Week-01 test-basis 체크
- 2025-08-11: Week-01 session-notes, Week-01 test-cases 체크 , ID규칙 수정
- 2025-08-12: Week-01 bug-report 체크
- 2025-08-13: Week-01 summart.md 체크
