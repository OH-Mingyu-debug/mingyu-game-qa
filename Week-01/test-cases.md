# Week-01(Metal Head) Test Cases

<br>

### TC-01 : 실행/종료 스모크 (루프 진입/이탈)


**검증 포인트(Coverage)** : C5  |  **리스크(Risk)** : 진행차단/크래시  |  **우선순위(Priority)** : 매우 높음(very high)

**전제(pre-condition)** : 게임 설치 완료, 실행 파일 경로 확인, 게임 실행

**Steps** :
1. 게임 실행 → 메인 화면 진입
2. 'Start' 클릭 → 10초 조작
3. ESC로 옵션 열기 → 'Abandon Hope' 선택 → 게임 종료

**예상 결과(Expected Result)** : 실행/로딩 크래시 없음 / ESC옵션 정상 작동 /종료 시 프로세스 정상 종료

**상태(Status)** : Not Run

<br>

### TC-02 : 조작(이동/점프) 반응 & 가장자리 충돌 & 맵 이동 시 충돌 및 카메라 무브


**검증 포인트(Coverage)** : C1  |  **리스크(Risk)** : 진행차단/충돌/카메라  |  **우선순위(Priority)** : 매우 높음(very high)

**전제(pre-condition)** : 튜토리얼 종료

**Steps** :
1. A/D로 좌우 이동 반복(평지/가장자리에서)
2. Space로 점프 반복(정지/이동/가장자리에서)
3. 좌우 이동으로 옆 맵 이동
4. 점프로 옆 맵 이동

**예상 결과(Expected Result)** : 입력 즉시 반응 / 딜레이 미미 / 가장자리에서 끼임 및 충돌 없음 / 맵 이동 시 충돌 없음 및 프레임 드랍 미미

**상태(Status)** : Not Run

<br>

### TC-03 : 낙사/리스폰 & 체크포인트


**검증 포인트(Coverage)** : C1  |  **리스크(Risk)** : 진행차단  |  **우선순위(Priority)** : 매우 높음(very high)

**전제(pre-condition)** : 스테이지 밑으로 낙하

**Steps** :
1. 사망 시 사망UI 확인
2. 리스폰 버튼 클릭 → 리스폰 동작 확인
3. 체크포인트 통과 후 낙하 재시도 → 리스폰 재시도

**예상 결과(Expected Result)** : 사망 시 사망UI 표시 / 리스폰 버튼 클릭시 리스폰 동작 / 체크포인트 기준으로 리스폰, 상태 초기화 확인

**상태(Status)** : Not Run

<br>

### TC-04 : 공격 히트 / 시각 및 음향 피드백 / 적 사망 / 피격


**검증 포인트(Coverage)** : C2  |  **리스크(Risk)** : 진행차단/전투 판정  |  **우선순위(Priority)** : 매우 높음(very high)

**전제(pre-condition)** : 데몬(몬스터)와 대면, ctrl 공격

**Steps** :
1. Ctrl 공격으로 적 타격(제자리/이동/점프 중)
2. 연속 공격 시 히트 누락 여부 관찰
3. 적에게 피격 → HP 소진
4. 적 사망까지 타격

**예상 결과(Expected Result)** : 히트 시 시각 및 음향 피드백 / 허공 히트 미판정 / 점프와 이동 공격시에도 판정 인정 / 일정 히트 시 적 사망 /피격 시 HP 소진 / 피격으로 HP 다 소진 시 사망

**상태(Status)** : Not Run

<br>

### TC-05 : 1단계 업그레이드 해금 (더블 점프)


**검증 포인트(Coverage)** : C3  |  **리스크(Risk)** : 충돌  |  **우선순위(Priority)** : 높음(high)

**전제(pre-condition)** : 1단계 업그레이드 해금

**Steps** :
1. 1차 업그레이드 해금 과제 달성
2. Space bar 더블 탭 입력(제자리/이동/맵 경계)

**예상 결과(Expected Result)** : Space bar 더블 탭 입력 시 더블점프 / 쿨타임 중에는 실행 불가 / 입력 타이밍 허용 범위 합리적 / 플랫폼 및 벽 관통 없음 / 2단 점프 중 카메라 떨림 및 시야 이탈 없음

**상태(Status)** : Not Run

<br>

### TC-06 : 2단계 업그레이드 해금 (대쉬)


**검증 포인트(Coverage)** : C3  |  **리스크(Risk)** : 충돌  |  **우선순위(Priority)** : 높음(high)

**전제(pre-condition)** : 2단계 업그레이드 해금

**Steps** :
1. 2차 업그레이드 해금 과제 달성
2. Left Shift 입력(제자리/이동/점프/맵 경계)

**예상 결과(Expected Result)** : Left Shift 입력 시 대쉬 / 쿨타임 중에는 실행 불가 / 플랫폼 및 벽 관통 없음 / 대쉬 중 카메라 떨림 및 시야 이탈 없음

**상태(Status)** : Not Run

<br>

### TC-07 : 스테이지 완주/엔드 트리거


**검증 포인트(Coverage)** : C4  |  **리스크(Risk)** : 진행차단  |  **우선순위(Priority)** : 매우 높음(very high)

**전제(pre-condition)** : 스테이지의 마지막 맵으로 이동 후, 보스 격파

**Steps** :
1. 스테이지 마지막 맵 도달
2. 보스 격파
3. 엔드 트리거 확인

**예상 결과(Expected Result)** : 엔드 트리거 안정 작동 / 클리어 UI 표시 / 클리어 UI에서 메인화면으로 이동

**상태(Status)** : Not Run

<br>

### TC-08 : 창↔전체 & 포커스 전환 안정성


**검증 포인트(Coverage)** : C5  |  **리스크(Risk)** : 창↔전체 포커스/크래시  |  **우선순위(Priority)** : 중간(Medium)

**전제(pre-condition)** : 메인화면에서 게임 시작 → 튜토리얼 종료

**Steps** :
1. Alt+Enter 3회 반복(플레이 중)
2. Alt+Tab 3회 반복 후 게임 복귀
3. 전환 직후 이동/점프/사운드 확인

**예상 결과(Expected Result)** : 조작키 입력 및 오디오 정상 / 블랙스크린, 크래시 없음 / 전환 후 프레임 및 카메라 이상 없음

**상태(Status)** : Not Run

<br>
