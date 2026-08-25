# lawready

글로벌 개인정보 문서 생성·버전관리 서비스의 문서와 애플리케이션 코드를 함께 관리하는 저장소입니다.

## 저장소 구조

```text
lawready/
├── docs/
│   ├── product/        제품 소개와 기능 정의
│   ├── architecture/   시스템 구조와 기술 검토
│   └── records/        기획 대화와 의사결정 기록
├── apps/
│   ├── web/            웹 애플리케이션
│   └── api/            API 애플리케이션
├── packages/           여러 애플리케이션이 공유하는 코드
├── tests/              저장소 수준의 통합·종단간 테스트
└── .github/            협업 규칙과 GitHub 설정
```

문서는 `docs/`, 실행 코드는 `apps/`, 공통 코드는 `packages/`, 저장소 수준 테스트는 `tests/`에서 관리합니다.

## 문서 구성

| 구분 | 파일 | 용도 |
|---|---|---|
| 서비스 소개 | [`docs/product/서비스_소개서.md`](docs/product/서비스_소개서.md) | LawReady가 해결하는 문제, 대상 고객, 사용자 흐름, 제공 범위와 차별점 설명 |
| 기능정의 | `docs/product/기능정의서.docx` | MVP 기능과 완료조건, 공통 발행 차단 규칙 정의 |
| 기능정의 부록 | `docs/architecture/기능정의서_기술검토_부록.docx` | 도메인·상태·비기능·오픈소스·기존 기능 ID 매핑 보관 |
| 시스템 구조도 | [`docs/architecture/lawready-system-architecture.png`](docs/architecture/lawready-system-architecture.png) | 시스템 구성과 주요 처리 흐름 설명 |
| 기획 대화 기록 | [`docs/records/서비스_기획_대화_기록_2026-08-25.md`](docs/records/서비스_기획_대화_기록_2026-08-25.md) | 서비스 범위 결정 배경과 확장 아이디어를 확인하기 위한 참고 기록 |

제품을 처음 이해할 때는 `서비스_소개서.md`를 먼저 확인합니다. 기능 구현 범위는 `기능정의서.docx`를 기준으로 판단합니다. 기술검토 부록은 구현 참고자료이며, 부록의 내용만으로 MVP 범위를 확대하지 않습니다.

## 변경 관리 원칙

1. 문서 변경은 `docs/<주제>`, 코드 기능은 `feat/<기능>`, 버그 수정은 `fix/<문제>` 브랜치에서 작업합니다.
2. 문서를 수정하기 전에 변경 목적과 영향을 `CHANGELOG.md`에 기록합니다.
3. 서비스 범위가 바뀌면 소개서와 기능정의서의 표현이 일치하는지 함께 확인합니다.
4. 기능 추가·삭제 시 기능 ID, 완료조건, 공통 검증 규칙, 기존 ID 매핑을 함께 갱신합니다.
5. 법률 콘텐츠 변경은 국가·기준일·검수자를 남기고 별도 법률 검수를 거칩니다.

자세한 협업 규칙은 [`.github/CONTRIBUTING.md`](.github/CONTRIBUTING.md)를 따릅니다.

## 권장 커밋 메시지

- `docs(intro): 대상 고객과 제공 범위 수정`
- `docs(spec): PUB-03 발행 차단 조건 보완`
- `feat(web): 프로젝트 생성 화면 추가`
- `feat(api): 문서 생성 엔드포인트 추가`
- `fix(api): 발행 검증 누락 수정`
