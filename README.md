# week2_first_app

A new Flutter project.
"# week2_first_app" 

# 2주차 Flutter 앱 구동 및 환경 구축 보고서

## 1. 개발환경 체크리스트
- [x] git --version
- [x] flutter --version
- [x] flutter doctor -v
- [x] flutter devices

### 실행 화면
![1번 과제](./screenshots/2주차%201번%20과제.png)

---

## 2. 첫 앱 실행
* **프로젝트 이름:** week2_first_app
* **실행 명령:** flutter run -d emulator-5554
* **Device ID:** emulator-5554
* **실행 시각:** 2026년 9월 21일

### 실행 화면
![2번 과제](./screenshots/image_a70c03.png)

---

## 3. GitHub 저장소와 첫 commit
* **본인 소유 저장소 링크:** https://github.com/chuns3hun/week2_first_app
* **Commit ID:** `e134646`
* **Commit 메시지:** `chore: verify first Flutter run`

---

## 4. 학습기록

| 항목 | 작성 내용 |
| :--- | :--- |
| **목표** | Windows OS 환경에서 Android 에뮬레이터(`emulator-5554`)를 대상으로 `week2_first_app` 프로젝트를 정상 구동하고 커스텀 UI 문구를 확인하는 것을 목표로 했습니다. |
| **관찰** | `flutter run` 실행 중 `Package ndk not found (28.2.13676358)` 오류 메시지와 함께 Gradle 빌드가 중단되는 현상을 관찰했습니다. |
| **원인** | Gradle 빌드 구성 파일에서 요구하는 NDK 특정 버전이 SDK 경로 내에 설치되어 있지 않아 빌드가 취소되는 연결 문제였습니다. |
| **행동** | Android Studio SDK Manager의 SDK Tools에서 `Show Package Details`를 활성화한 후 `NDK (Side by side) 28.2.13676358` 버전을 수동 설치하고 `flutter run -d emulator-5554` 명령어로 재검증했습니다. |
| **결과** | NDK 설치 전에는 빌드가 실패했으나, 수정 후 에뮬레이터 화면에 수정한 `Hello World!` 문구가 오류 없이 정상 출력되었습니다. |
| **다음** | 3주차 위젯 및 상태 관리 학습을 준비하기 위해 Flutter의 Hot Reload 원리와 State 변경 시 UI 렌더링 과정을 추가로 살펴볼 예정입니다. |