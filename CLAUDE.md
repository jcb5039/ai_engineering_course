# todo_lab — 프로젝트 규칙

## 프로젝트 개요
- Flutter 학습용 할 일(Todo) 앱. 데이터는 메모리에만 저장한다(앱을 끄면 사라짐).
- 실행 확인 대상: Chrome(웹), macOS 데스크톱.

## 폴더 구조
- `lib/todo_list.dart` : 할 일 규칙(비즈니스 로직). 순수 Dart만 사용하고 `package:flutter`를 import하지 않는다.
- `lib/main.dart` : 화면(UI). 규칙은 todo_list.dart를 호출만 한다.
- `test/` : 단위 테스트(`*_test.dart`)와 위젯 테스트(`widget_test.dart`).
- `docs/specs/` : 기능 명세서. 모든 작업은 명세서를 기준으로 한다.
- `harness/` : 자동 개발·검증 스크립트(DAY 5부터). 사람이 요청하지 않으면 수정하지 않는다. (하네스 실행 중에는 `lib/`, `test/` 밖의 변경을 하네스가 기계적으로 거부한다)

## 명령어
- 정적 분석: `flutter analyze` (info 수준 문제도 실패로 처리된다)
- 테스트: `flutter test`
- 포맷: `dart format lib test`
- 실행: `flutter run -d chrome`

## 코딩 규칙
- 사용자에게 보이는 문구는 한국어로 쓴다.
- 위젯 테스트에서 찾아야 하는 위젯에는 명세서에 적힌 `Key('...')`를 붙인다.
- 입력 검증 규칙(길이, 빈 값, 중복)은 로직 파일에 두고, 화면은 예외 메시지를 보여 주기만 한다.

## 작업 방식
- 작업 전에 관련 명세서(`docs/specs/`)를 읽는다. 명세서에 없는 기능은 만들지 않는다.
- 명세가 애매하면 구현 전에 질문한다. 질문할 수 없는 자동 실행이면 가장 단순한 해석을 택하고 "가정"으로 보고한다.
- 요구사항마다 테스트를 작성하고, 테스트 이름에 요구사항 ID(예: R1-2)를 넣는다.
- 완료 보고 전에 `flutter analyze`와 `flutter test`를 실행하고, 결과를 요약하지 말고 통과/실패 개수를 그대로 보고한다.
- 테스트를 삭제·skip하거나 기대값을 바꿔서 통과시키지 않는다.

## 하지 말 것
- `pubspec.yaml`에 패키지 추가 (필요하면 이유와 함께 먼저 물어본다)
- `git push`, `git reset --hard`, 브랜치 삭제
- `.env` 등 비밀값 파일 읽기·생성, API 키를 코드에 쓰기
- `android/`, `ios/`, `macos/`, `web/`, `windows/`, `linux/` 플랫폼 폴더 수정
