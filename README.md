# Shattered Pixel Dungeon — 늑대인간 모드

사용자가 제공한 Shattered Pixel Dungeon v4.0.0 소스에 늑대인간 직업을 추가하는 APK 빌드 저장소입니다.

## 빌드

GitHub Actions의 `Build Werewolf APK` 워크플로가 원본 커밋 `2bb34a4e91d29c8785a9363cad6ddfe5122b1d4f`를 받아 `Werewolf-v4.0.0.patch`를 적용합니다. JDK 17과 Android SDK 36을 준비한 뒤 성장 계산, Java 문법, 소스 연결 검사, 게임 객체 통합 검사를 실행하고 설치 가능한 디버그 서명 APK를 빌드합니다.

성공한 실행의 `ShatteredPD-Werewolf-v4.0.0-APK` 아티팩트에서 `ShatteredPD-Werewolf-v4.0.0.apk`, SHA-256 체크섬, 서명 검사 결과를 받을 수 있습니다. APK 생성 여부는 Actions의 실제 실행 결과로 확인합니다.

전사 스프라이트를 재사용합니다. 밸런스 상수는 패치가 추가하는 `WerewolfBalance.java`에 모았습니다.

원본 프로젝트: https://github.com/00-Evan/shattered-pixel-dungeon

