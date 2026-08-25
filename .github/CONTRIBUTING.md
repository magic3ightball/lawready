# 협업 규칙

## 작업 위치

- 제품·기능 문서: `docs/product/`
- 시스템 구조·기술 검토: `docs/architecture/`
- 기획·의사결정 기록: `docs/records/`
- 웹 애플리케이션: `apps/web/`
- API 애플리케이션: `apps/api/`
- 공통 코드: `packages/`
- 저장소 수준 테스트: `tests/`

## 브랜치 이름

- 문서: `docs/<주제>`
- 기능: `feat/<기능>`
- 버그 수정: `fix/<문제>`

한 브랜치에서는 가능한 한 문서 작업과 코드 작업을 섞지 않습니다. 문서와 코드가 함께 바뀌어야 하는 기능은 한 Pull Request에서 변경 이유와 영향을 각각 설명합니다.
