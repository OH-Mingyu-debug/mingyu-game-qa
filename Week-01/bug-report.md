# Week-01(MetalHead) Bug Report

<br>

## BUG-01 : 사망UI 내에서 옵션 열람 시, UI고정/진행 불가

- **테스팅 환경(Test Case)** : TC-01/TC-03  |  **검증포인트(Coverage Point)** : C5  |  **리스크(Risk)** : 진행 차단

- **심각도(Severity)** : 매우 심각(Fatal)  |  **우선순위(Priority)** : 즉시 해결(Resolve immediately)

- **Steps to Reproduce** : 
1. 캐릭터 조작으로 옆 구멍으로 낙하
2. 사망UI에서 ESC키 눌러, 옵션 활성화
3. 게임 재개 버튼 클릭

- **예상결과(Expected Result)** : 사망UI로 돌아와서 UI버튼 정상작동(리스폰/게임종료)

- **실제결과(Actual Result)** : 사망UI 마우스 커서 사라짐/미동작/고정 및 사망 음향 출력

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-01](evidence/videos/W01_BUG_01.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-02 : 종료 후 itch-setup.exe에서 재실행 오류

- **테스팅 환경(Test Case)** : TC-01  |  **검증포인트(Coverage Point)** : C5  |  **리스크(Risk)** : 진행차단/크래시

- **심각도(Severity)** : 매우 심각(Fatal)  |  **우선순위(Priority)** : 주의 요망(Give high attention)

- **Steps to Reproduce** : 
1. itch-setup.exe로 게임 실행 후 메인화면에서 종료버튼 클릭
2. 다시 실행

- **예상결과(Expected Result)** : 게임 정상 실행

- **실제결과(Actual Result)** : 실행 중 오류 팝업창 발생

- **발현빈도(Repro Rate)** : 3/5

- **스크린샷/로그(Evidence)** : [BUG-02](evidence/screenshots/W01_BUG_02.png)

<br>

## BUG-03 : 데몬(적) 추적 시스템 오류

- **테스팅 환경(Test Case)** : TC-04  |  **검증포인트(Coverage Point)** : C2/C4  |  **리스크(Risk)** : 전투판정/진행차단

- **심각도(Severity)** : 심각(No Workaround)  |  **우선순위(Priority)** : 주의 요망(Give high attention)

- **Steps to Reproduce** : 
1. 게임 실행 후 진행
2. 데몬(적)과 조우
3. 데몬(적)의 추격 범위 내에서 옆 발판으로 점프

- **예상결과(Expected Result)** : 데몬(적)이 추격 도중 낙하 구간에서 정지

- **실제결과(Actual Result)** : 낙하 구간 무시 후 계속해서 캐릭터 방향으로 이동 및 진행 방향 차단

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-03](evidence/screenshots/W01_BUG_03.png)

<br>

## BUG-04 : 플랫폼 충돌 판정 오류

- **테스팅 환경(Test Case)** : TC-02  |  **검증포인트(Coverage Point)** : C1  |  **리스크(Risk)** : 충돌

- **심각도(Severity)** : 보통(Workaround)  |  **우선순위(Priority)** : 대기(Normal queue)
- **Steps to Reproduce** : 
1. A/D 방향키로 조작
2. 플랫폼 끝에 안착 후 낙하까지 계속 일정거리씩 이동

- **예상결과(Expected Result)** : 눈에 보이는 낙하구간부터는 바로 낙하

- **실제결과(Actual Result)** : 실제 보이는 낙하구간보다 많은 거리 이동 가능

- **발현빈도(Repro Rate)** : 3/5

- **스크린샷/로그(Evidence)** : [BUG-04](evidence/screenshots/W01_BUG_04.png)

<br>

## BUG-05 : 낙하 모션 발동 오류

- **테스팅 환경(Test Case)** : TC-02  |  **검증포인트(Coverage Point)** : C1  |  **리스크(Risk)** : 충돌

- **심각도(Severity)** : 보통(Workaround)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. A/D 방향키로 조작
2. 플랫폼 끝에 안착 후 조금 더 이동

- **예상결과(Expected Result)** : 낙하 전에는 서있는 모션, 낙하 시작 후에 낙하 모션으로 변경
- **실제결과(Actual Result)** : 플랫폼에 서 있음에도 낙하 시작 전에 낙하 모션 발동

- **발현빈도(Repro Rate)** : 2/5

- **스크린샷/로그(Evidence)** : [BUG-05](evidence/screenshots/W01_BUG_05.png)

<br>

## BUG-06 : 보스맵 무적 자리 존재 및 캐릭터 프레임보다 더 이동 가능

- **테스팅 환경(Test Case)** : TC-04  |  **검증포인트(Coverage Point)** : C2  |  **리스크(Risk)** : 전투판정

- **심각도(Severity)** : 보통(Workaround)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 게임 진행 후 보스맵 입장
2. 오른쪽 끝 또는 왼쪽 끝으로 이동

- **예상결과(Expected Result)** : 보스의 공격이 양 끝까지 도달 / 보이는 프레임 밖으로 이동 불가
- **실제결과(Actual Result)** : 보스의 공격이 끝까지 닿지않음 / 프레임 밖을 지나서 더 이동 가능

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-06](evidence/screenshots/W01_BUG_06.png)

<br>

## BUG-07 : 낙하 사망 후 더블점프 입력 시 음향 출력 및 캐릭터 이동 판정

- **테스팅 환경(Test Case)** : TC-05  |  **검증포인트(Coverage Point)** : C3  |  **리스크(Risk)** : 충돌

- **심각도(Severity)** : 보통(Workaround)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 1단계 업그레이드로 더블점프 해금
2. 낙하로 사망
3. 사망UI 표시 전까지 더블점프 계속하여 입력 

- **예상결과(Expected Result)** : 더블점프 입력 불가
- **실제결과(Actual Result)** : 더블점프 음향 출력 및 캐릭터 이동 판정

- **발현빈도(Repro Rate)** : 4/5

- **스크린샷/로그(Evidence)** : [BUG-07](evidence/videos/W01_BUG_07.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-08 : 낙하 사망 후 대쉬 입력 시 음향 출력 및 캐릭터 이동 판정

- **테스팅 환경(Test Case)** : TC-06  |  **검증포인트(Coverage Point)** : C3  |  **리스크(Risk)** : 충돌

- **심각도(Severity)** : 보통(Workaround)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 2단계 업그레이드로 대쉬 해금
2. 낙하로 사망
3. 사망UI 표시 전까지 대쉬 계속하여 입력 

- **예상결과(Expected Result)** : 대쉬 입력 불가
- **실제결과(Actual Result)** : 대쉬 음향 출력 및 캐릭터 이동 판정

- **발현빈도(Repro Rate)** : 4/5

- **스크린샷/로그(Evidence)** : [BUG-08](evidence/videos/W01_BUG_08.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-09 : 수직 이동형 맵 ↔ 수평 이동형 맵 전환 카메라 떨림

- **테스팅 환경(Test Case)** : TC-02  |  **검증포인트(Coverage Point)** : C1  |  **리스크(Risk)** : 카메라

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 수직 이동형 맵 입장
2. 계속 하강
3. 끝으로 도달 후, 수평 이동형 맵으로 전환
4. 다시 돌아가서 수평 이동형 맵 ↔ 수직 이동형 맵 전환 반복

- **예상결과(Expected Result)** : 부드러운 카메라 전환
- **실제결과(Actual Result)** : 부자연스러운 카메라 전환

- **발현빈도(Repro Rate)** : 5/5

- **스크린샷/로그(Evidence)** : [BUG-09](evidence/videos/W01_BUG_09.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-10 : 사망 후 공격 음향 출력 오류

- **테스팅 환경(Test Case)** : TC-04  |  **검증포인트(Coverage Point)** : C2  |  **리스크(Risk)** : 전투판정

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 데몬(적)과 전투
2. 데몬(적)에게 2번 피격 후 사망
3. 사망UI 표시 전에 Ctrl 눌러 공격 입력

- **예상결과(Expected Result)** : 공격 음향 미출력
- **실제결과(Actual Result)** : 공격 음향 출력

- **발현빈도(Repro Rate)** : 5/5

- **스크린샷/로그(Evidence)** : [BUG-10](evidence/videos/W01_BUG_10.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-11 : 데몬(적) 위로 점프 시, 낙하 모션 실행

- **테스팅 환경(Test Case)** : TC-04  |  **검증포인트(Coverage Point)** : C2  |  **리스크(Risk)** : 전투판정

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 데몬(적)과 전투
2. 점프로 데몬(적) 위로 올라감

- **예상결과(Expected Result)** : HP감소 등 이벤트 동작
- **실제결과(Actual Result)** : 데몬(적)의 움직임이 멈추며 낙하 모션 실행

- **발현빈도(Repro Rate)** : 5/5

- **스크린샷/로그(Evidence)** : [BUG-11](evidence/screenshots/W01_BUG_11.png)

<br>

## BUG-12 : 데몬(적) 특정거리 이동 시 버벅거림

- **테스팅 환경(Test Case)** : TC-04  |  **검증포인트(Coverage Point)** : C2  |  **리스크(Risk)** : 전투판정

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 대기(Normal queue)

- **Steps to Reproduce** : 
1. 데몬(적)과 조우
2. 데몬(적)의 추격 범위 내에서 계속하여 왼쪽 또는 오른쪽으로 이동

- **예상결과(Expected Result)** : 데몬이 자연스럽게 계속 추적
- **실제결과(Actual Result)** : 데몬(적)이 일정거리 이동 시, 버벅거림 발생

- **발현빈도(Repro Rate)** : 2/5

- **스크린샷/로그(Evidence)** : [BUG-12](evidence/videos/W01_BUG_12.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-13 : 1단계 업그레이드 해금 후 안내창 오류

- **테스팅 환경(Test Case)** : TC-05  |  **검증포인트(Coverage Point)** : C3  |  **리스크(Risk)** : 진행차단

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 낮은 순위(Low priority)

- **Steps to Reproduce** : 
1. 1단계 업그레이드 해금
2. 해금 후 나오는 안내창 닫지않고 이동
3. 낙하로 인한 사망
4. 사망 UI에서 리스폰

- **예상결과(Expected Result)** : 사망 후 리스폰을 하면 안내창을 닫지 않아도 자동으로 닫힘
- **실제결과(Actual Result)** : F키를 이용해서 안내창을 닫지 않는 이상, 계속해서 안내창이 떠 있음

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-13](evidence/videos/W01_BUG_13.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-14 : 2단계 업그레이드 해금 후 안내창 오류

- **테스팅 환경(Test Case)** : TC-06  |  **검증포인트(Coverage Point)** : C3  |  **리스크(Risk)** : 진행차단

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 낮은 순위(Low priority)

- **Steps to Reproduce** : 
1. 2단계 업그레이드 해금
2. 해금 후 나오는 안내창 닫지않고 이동
3. 낙하로 인한 사망
4. 사망 UI에서 리스폰

- **예상결과(Expected Result)** : 사망 후 리스폰을 하면 안내창을 닫지 않아도 자동으로 닫힘
- **실제결과(Actual Result)** : F키를 이용해서 안내창을 닫지 않는 이상, 계속해서 안내창이 떠 있음

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-14](evidence/videos/W01_BUG_14.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

## BUG-15 : 클리어 후, 엔딩 크레딧에서 조작 음향 출력

- **테스팅 환경(Test Case)** : TC-07  |  **검증포인트(Coverage Point)** : C4  |  **리스크(Risk)** : 진행차단

- **심각도(Severity)** : 경미(Cosmetic)  |  **우선순위(Priority)** : 낮은 순위(Low priority)

- **Steps to Reproduce** : 
1. 게임 클리어 후 엔드 트리거 발동
2. 엔딩 크레딧
3. 엔딩 크레딧이 떠 있는 상태로 점프, 대쉬, 공격 등 조작

- **예상결과(Expected Result)** : 엔딩 크레딧에서 조작 불가로 인한 음향 미출력
- **실제결과(Actual Result)** : 점프, 대쉬, 공격을 입력하면 음향 출력

- **발현빈도(Repro Rate)** : 3/3

- **스크린샷/로그(Evidence)** : [BUG-15](evidence/videos/W01_BUG_15.mp4)
  **※mp4 문서 증거는 용량 상의 문제로 미리보기 불가함※**

<br>

