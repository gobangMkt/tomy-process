# tommy-process

고방 마케팅 개발 프로세스 스킬 패키지.

## 포함 스킬 (18개)

| 스킬 | 설명 |
|------|------|
| `icon-design` | TOSSFACE 스타일 플랫 SVG 아이콘 가이드 |
| `grill-me` | 스펙 빈틈 채우는 릴렌틀리스 인터뷰 |
| `grill-with-docs` | 도메인 모델 기반 스펙 검증 |
| `tdd` | Red→Green→Refactor TDD 루프 |
| `to-issues` | 스펙→수직 슬라이스 이슈 분할 |
| `to-prd` | 대화 컨텍스트→PRD 자동 작성 |
| `triage` | 이슈 트래커 트리아지 워크플로우 |
| `prototype` | 빠른 검증용 throwaway 프로토타입 |
| `diagnose` | 하드 버그 6단계 진단 루프 |
| `handoff` | 대화 컨텍스트→핸드오프 문서 |
| `improve-codebase-architecture` | 아키텍처 개선 기회 발굴 |
| `caveman` | 토큰 75% 절약 압축 응답 모드 |
| `zoom-out` | 코드베이스 상위 레벨 맥락 파악 |
| `qa-full-cycle` | TC 작성→Playwright E2E→PASS/FAIL 리포트 |
| `e2e-testing-patterns` | Playwright/Cypress E2E 테스트 패턴 |
| `test-case-creation` | 요구사항→TC 작성 가이드 |
| `elite-powerpoint-designer` | Apple/Google 수준 PPT 제작 |
| `prototype` | throwaway 프로토타입 빌드 |

## 팀 세팅 (3단계)

```bash
# 1. 프로젝트 클론 (CLAUDE.md 자동 적용)
git clone https://github.com/gobangMkt/my-claude-project

# 2. 커스텀 스킬 패키지 설치 (이 레포)
npx skills add gobangMkt/tommy-process -g --all

# 3. ui-ux-pro-max 설치
npx skills add nextlevelbuilder/ui-ux-pro-max-skill --skill ui-ux-pro-max -g
```

이후 Claude Code `/plugin`에서 GitHub · Figma · Playwright MCP 서버 설치 (개인 API 키 필요).
