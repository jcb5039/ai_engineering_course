# AI Engineering Course — 학습 기록

Claude Code와 Codex를 써서 **AI와 함께 개발하는 방법**을 7일 과정으로 공부하는 저장소입니다.
AI에게 일을 맡길 때 필요한 컨텍스트, 명세서, 테스트, 검증, 자동화(하네스)를 직접 실습하며 익힙니다.

실습 프로젝트는 Flutter로 만드는 할 일(Todo) 앱 `todo_lab`입니다.

## 진행 현황

- [x] DAY 1: CLAUDE.md와 컨텍스트 엔지니어링
- [ ] DAY 2: 작업 명세서와 완료 조건
- [ ] DAY 3: 자동 테스트와 검증
- [ ] DAY 4: Codex 독립 검증자
- [ ] DAY 5: 하네스 및 루프 엔지니어링
- [ ] DAY 6: 간단한 앱 자동 개발 실험
- [ ] DAY 7: 결과 분석 및 개선

## 주요 파일

| 파일 | 설명 |
|---|---|
| `CLAUDE.md` | AI(Claude)가 이 프로젝트에서 지켜야 할 작업 규칙 |
| `.claude/settings.json` | AI가 절대 하면 안 되는 행동을 막는 권한 설정 |
| `lib/` | 앱 코드 |
| `test/` | 테스트 코드 |

## 실행 방법

```bash
flutter run -d chrome   # 앱 실행
flutter test            # 테스트 실행
```
