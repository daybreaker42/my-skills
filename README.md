# AI-Native Hackathon Codex Skills

AI 코딩 과제에서 **문제 정의 → 계획 → 구현 → 검증 → 근거 설명**을 일관되게 수행하도록 돕는 독립형 Codex Skill 5종입니다.

## 구성

| Skill | 목적 | 권장 사용 시점 |
|---|---|---|
| `ideation` | 요구사항 해석, 해결안 비교, 선택 근거 | 과제 직후 |
| `planning` | MVP·작업 분해·완료 조건·우선순위 | 구현 직전 |
| `implementation` | 기존 코드 기반의 최소 변경 및 실행 | 구현 중 |
| `verification` | 테스트·경계값·회귀·제출 판정 | 구현 직후/제출 전 |
| `evidence-rationale` | 선택 근거·코드·실행 결과의 추적 | 작업 전반 |

## 설치

### 방법 A: 프로젝트별 설치
이 저장소의 `.agents/skills/` 디렉터리를 **작업 프로젝트 루트**에 복사합니다.

```text
project/
└── .agents/
    └── skills/
        ├── ideation/SKILL.md
        ├── planning/SKILL.md
        ├── implementation/SKILL.md
        ├── verification/SKILL.md
        └── evidence-rationale/SKILL.md
```

### 방법 B: 개인 환경 설치
각 Skill 디렉터리를 사용자 홈의 `~/.agents/skills/` 아래에 복사합니다. 대회용 격리 환경에서는 개인 설정을 수정하기보다 **허용된 경우에 한해** 프로젝트별 설치를 권장합니다.

Codex에서 Skill이 발견되면 `$ideation`, `$planning`, `$implementation`, `$verification`, `$evidence-rationale`처럼 명시적으로 요청할 수 있습니다. 실제 지원 경로/발견 방식은 제공된 Codex 버전과 환경에 따라 확인하세요.

## 추천 사용 예시

```text
$ideation 과제 명세를 분석해 요구사항, 가정, 성공 기준을 정리하고 2~3개 해결안을 비교해줘.
$planning 선택한 해결안으로 MVP와 구현·검증 계획을 만들어줘.
$implementation 계획의 첫 번째 작업을 구현하고 실행 가능한 검증을 수행해줘.
$verification 요구사항별로 테스트하고 실제 실행 근거를 보여줘.
$evidence-rationale 지금까지의 선택 근거, 변경 파일, 테스트 결과, 남은 한계를 정리해줘.
```

**운영 팁:** `evidence-rationale`는 마지막에만 사용하는 것이 아니라 중요한 선택과 테스트 직후에도 호출하면 좋습니다. 한 번에 모든 스킬을 무조건 호출하기보다 실제 작업 단계에 맞게 사용하세요.

## 대회 규정 관련 주의

- 이 저장소는 `SKILL.md` 텍스트 지침만 포함합니다. Hook, 실행 스크립트, MCP 서버, 외부 모델 호출, 모델 라우팅, Codex 설정 변경 코드는 포함하지 않습니다.
- **GitHub 공개 = 대회 사용 허가**는 아닙니다. 사전 작성 Skill의 반입 및 외부 GitHub 저장소 사용이 허용되는지 운영진 규정을 확인해야 합니다.
- 시험 플랫폼 설정·모니터링·제한을 변경하거나 우회하지 마세요.
- 시험에서 개인 파일 업로드, 외부 전송, AI 사용 금지 구간 등이 있다면 해당 규정이 이 지침보다 우선합니다.
- 스킬은 평가 결과를 보장하지 않으며 실제 실행/검증을 대신하지 않습니다.

## 라이선스

공개 배포 시에는 본인이 선택한 라이선스를 별도로 추가하세요. 현재 패키지는 라이선스 파일을 포함하지 않습니다.
