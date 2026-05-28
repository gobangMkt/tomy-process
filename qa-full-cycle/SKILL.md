---
name: qa-full-cycle
description: TC 작성부터 Playwright E2E 실행까지 전체 QA 워크플로우를 자동화한다. "QA 해줘", "테스트 해줘", "E2E 돌려줘", "TC 작성해줘", "테스트 케이스", /qa 키워드가 나오면 반드시 트리거. URL이나 기능명만 있어도 TC 설계 → 사용자 승인 → Playwright 실행 → PASS/FAIL 리포트까지 원스톱 처리. test-case-creation + e2e-testing-patterns 두 스킬을 통합한 풀사이클 QA 스킬.
---

# QA Full Cycle

TC 설계 → 사용자 승인 → Playwright E2E 실행 → 결과 리포트. 단계를 건너뛰지 않는다.

## 워크플로우 (5단계 순서 절대 준수)

### 1단계: 분석

테스트 대상을 파악한다. 없으면 묻는다.
- 확인 항목: URL / 기능명 / 요구사항 / 사전 로그인 여부

### 2단계: TC 작성

| 필드 | 내용 |
|---|---|
| ID | TC-001 형식 |
| 제목 | 한 줄 요약 (동사 + 대상) |
| Preconditions | 테스트 시작 전 필요한 상태 |
| Steps | 번호 매긴 액션 |
| Test Data | 실제 사용할 값 |
| Expected Result | 구체적인 기대 결과 |

4가지 유형: Happy Path / Negative Path / Edge Case / Business Logic

### 3단계: 사용자 확인 ← **이 단계 없이 실행 절대 금지**

TC 목록을 표로 보여주고 명시적 승인을 받는다.

### 4단계: E2E 실행 (Playwright MCP)

**셀렉터 우선순위:**
1. `getByRole('button', { name: '...' })`
2. `getByLabel('...')`
3. `getByText('...')`
4. `locator('[data-testid="..."]')`
5. CSS 클래스 — 최후의 수단

**실행 규칙:**
- 고정 `sleep` 금지 → 이벤트 기반 대기 사용
- 각 TC는 독립적으로 실행
- 실패 시: 스크린샷 캡처 후 다음 TC 계속 진행

### 5단계: 결과 리포트

```markdown
## QA 결과 리포트 — {기능명} ({날짜})

| TC ID | 제목 | 유형 | 결과 | 비고 |
|-------|------|------|------|------|
| TC-001 | ... | Happy Path | ✅ PASS | |
| TC-002 | ... | Negative | ❌ FAIL | 에러 메시지 미노출 |

**총 요약:** {N}개 중 {M}개 통과 ({%}%)
```

## 빠른 참조

- **TC 없이 E2E 실행** → 금지
- **승인 없이 4단계 진입** → 금지
- **고정 sleep** → 금지
- **실패 시 즉시 중단** → 금지, 계속 진행
