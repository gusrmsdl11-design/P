# Shattered Pixel Dungeon — 늑대인간 모드 v2

사용자가 제공한 Shattered Pixel Dungeon v4.0.0 소스에 늑대인간 직업을 추가한 Android 모드입니다. 전사 스프라이트를 재사용합니다.

## APK 다운로드

- [ShatteredPD-Werewolf-v2.apk](https://github.com/gusrmsdl11-design/P/releases/download/v4.0.0-werewolf.2/ShatteredPD-Werewolf-v2.apk)
- [v2 배포 페이지](https://github.com/gusrmsdl11-design/P/releases/tag/v4.0.0-werewolf.2)
- [구현·검증 보고서](https://github.com/gusrmsdl11-design/P/releases/download/v4.0.0-werewolf.2/WEREWOLF_UPDATE_V2_KO.md)

Android 5.0 이상, ARM 32/64비트 및 x86을 지원합니다. 개발 서명 APK입니다.

기존 버전의 임시 서명키가 남아 있지 않아 **Shattered PD Werewolf 2**라는 별도 앱으로 설치됩니다. 기존 앱을 삭제할 필요는 없으며 기존 저장은 자동 이동되지 않습니다. v2부터 보관한 개발 서명키를 사용합니다.

## v2 변경 사항

- 심장찌르기의 최대 충전량은 기본 3이며, 발톱 강화 +2마다 +1 증가합니다. 성장 상한은 없습니다.
- 날고기 성장 보상 간격을 10킬에서 20킬로 변경했습니다.
- 3티어 특성을 3단계, 4티어 특성을 4단계로 세분화했습니다.
- 달려들기는 암살자와 같은 화면 행동 버튼과 대상 선택을 사용하며 충전 횟수를 표시합니다.
- 철가루 3개를 정제된 철 1개로 변환합니다. 정제된 철 3개와 연금술 에너지 6으로 발톱 숫돌 1개를 제작합니다.
- 소환수와 소환 출처가 표시된 적은 영구 성장 킬에서 제외합니다.

밸런스 상수는 패치가 추가하는 `WerewolfBalance.java`에 모았습니다. 변경 파일 목록, 단계별 수치, 저장 호환과 제한 사항은 배포 보고서에 있습니다.

## 빌드와 검증

`Build Werewolf APK` 워크플로는 원본 커밋 `2bb34a4e91d29c8785a9363cad6ddfe5122b1d4f`를 받아 `Werewolf-v4.0.0.patch`를 적용합니다. JDK 17과 Android SDK 36으로 검사와 APK 빌드를 실행합니다. Actions의 후보 APK는 실행마다 임시 서명되므로 배포 페이지의 최종 APK를 받으세요.

- [성공한 게임 빌드](https://github.com/gusrmsdl11-design/P/actions/runs/37200418799)
- [최종 APK 검증·배포](https://github.com/gusrmsdl11-design/P/actions/runs/37208134806)
- 성장 계산 9,277개, 정적·번역 검사 552개, 실제 게임 객체 검사 283개 통과
- Java 1,315개 파일 문법 오류 0, Android 빌드 성공
- 최종 APK 서명 v1·v2·v3 검증 통과
- 실기기 플레이와 화면 렌더링은 미검증

APK SHA-256: `639170ac5bda8b2edc96998ce52922cabf15caa54d98109648ff77644b9bf33d`

원본 프로젝트: https://github.com/00-Evan/shattered-pixel-dungeon
