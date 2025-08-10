# Test Basis — Metal Head (itch.io, Windows Prototype)

<br>

## 출처(명시적 근거)
- 페이지 요약: "2D platformer demo level", 싱글플레이, 짧은 데모, 레벨 끝 도달
- 메타: Published 2025-01-03 / Status Prototype / Platform Windows / Author LukeTC
- 설치: 압축 해제 → "Metal Head" 실행 파일 실행
- 조작키
  - A : 왼쪽으로 이동
  - D : 오른쪽으로 이동
  - SpaceBar : 점프
  - ctrl : 공격
  - Spacebar Double tap : 2단 점프 **_※1단계 업그레이드시 해금※_**
  - Left Shift : 대쉬 **_※2단계 업그레이드시 해금※_**
- 스샷: (Week01/evidence/screenshots)

<br>

## 장르·플랫폼 컨벤션(암묵적)
- Platformer: 이동/점프 즉시 반응, 가장자리 충돌, 낙사/리스폰, 체크포인트
- Windows: ESC=Pause, Alt+Enter=창↔전체

<br>

## 핵심 검증 포인트
- C1 : 2D 플랫폼 컨벤션(이동, 점프, 낙사, 리스폰)
- C2 : 전투 상호작용 (데몬과 전투)
- C3 : 성장/업그레이드 시스템 (성장을 하며 따르는 새로운 스킬/UI 확인)
- C4 : 스테이지 완주(진행 차단 없음)
- C5 : 옵션 및 종료 정상

<br>

## 리스크(우선순위)
1) 진행 차단
2) 충돌
3) 카메라
4) 전투 판정
5) 옵션 미반영
6) 창↔전체 포커스
7) 크래시

<br>

## 이번 세션 범위/비범위
- In
  - 실행 ~ 1스테이지
  - 조작
  - 전투
  - 성장/업그레이드 시스템
  - 체크포인트
  - 옵션
  - 창↔전체
- Out: 장시간 안정성, 세부 패드 호환, 밸런스 평

<br>

## 오라클
- 명시적: 제품 설명+튜토리얼 / 암묵적: 컨벤션 / 경험: Assumption로 표기

