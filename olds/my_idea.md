1. 지원자의 평가는 6개의 주요 지표를 만들것,
  - 다양한 백그라운드의 사람드들이 공정하게 평가받을수 있도록 축을 만들어야해
  - 6개 지표는 모두  0~10점으로 정량 평가되어 최종 대시보드에선는 이 6개의 지표를 6각형으로 시각화해서 비교해줄수 있어야해 + 이에 더해서 해당 지표점수의 근거 내용이 정성적으로 볼수 있어야해
2. Input은 Resume 를 바탕으로할것.

[질문 1: 6개 지표 axis에 대해 정의해줘]

## 답변 1: AI Builder 후보자 평가를 위한 6개 Axis 정의

Resume만을 input으로 사용할 경우, 특정 학교, 회사명, 직함, 연차 같은 표면적 신호에 과도하게 의존하면 다양한 백그라운드의 후보자에게 불리할 수 있다. 따라서 6개 axis는 "어디에서 일했는가"보다 "무엇을 만들었고, 어떤 문제를 어떻게 풀었으며, AI Builder 역할에 필요한 판단을 보여주는가"를 중심으로 설계해야 한다.

각 axis는 0~10점으로 평가하고, 점수만 표시하지 않고 반드시 근거 문장을 함께 저장한다. 최종 대시보드에서는 6개 점수를 radar chart 또는 hexagon chart로 보여주고, 각 축을 클릭하면 AI가 추출한 근거, 불확실성, 사람이 검토해야 할 질문을 확인할 수 있게 한다.

### Axis 1. Problem Framing and Ambiguity Handling

**정의:** 모호하거나 정답이 정해지지 않은 문제를 구조화하고, 해결 가능한 범위로 좁히는 능력이다.

AI Builder는 단순히 주어진 요구사항을 구현하는 사람이 아니라, 불명확한 비즈니스 상황에서 무엇을 만들 가치가 있는지 정의해야 한다. Resume에서 전략 수립, 문제 정의, discovery, stakeholder alignment, product scoping, consulting project, research-to-product 전환 경험 등이 있는지 본다.

**높은 점수 신호:**

- 모호한 비즈니스 문제를 구체적인 제품, 자동화, 모델, 워크플로우로 전환한 경험
- 요구사항이 불완전한 상황에서 가설을 세우고 검증한 경험
- 문제 범위, 성공 기준, 사용자 요구를 직접 정의한 경험
- 컨설팅, 제품 기획, 연구, 운영 개선 등 다양한 맥락에서 문제 구조화 경험

**낮은 점수 신호:**

- 정해진 작업 수행만 있고 문제 정의 과정이 보이지 않음
- 기술 스택 나열은 많지만 왜 만들었는지 설명이 부족함
- 결과물이 어떤 문제를 해결했는지 불명확함

**0~10 점수 기준:**

- 0~2점: 문제 정의 경험이 거의 보이지 않음
- 3~5점: 일부 프로젝트 경험은 있으나 주어진 요구사항 수행 중심
- 6~8점: 문제를 구조화하고 해결 방향을 제안한 경험이 명확함
- 9~10점: 복잡한 이해관계자와 모호한 목표를 다루며 방향 설정과 실행까지 이끈 경험이 강함

### Axis 2. Practical Building and Execution

**정의:** 아이디어를 실제로 작동하는 산출물로 만드는 능력이다.

AI Builder 역할은 개념 설명만 잘하는 사람이 아니라, 빠르게 프로토타입을 만들고 검증 가능한 형태로 구현하는 사람을 필요로 한다. Resume에서 앱, 자동화, 모델, agent, dashboard, API, workflow, internal tool, MVP, production deployment 경험을 본다.

**높은 점수 신호:**

- 실제 사용 가능한 제품, 도구, 자동화, 데이터 파이프라인, AI workflow를 만든 경험
- 프로토타입에서 운영 가능한 시스템으로 발전시킨 경험
- 제한된 시간과 자원 안에서 tangible output을 만든 경험
- GitHub, demo, deployed app, case study, measurable result 등 검토 가능한 산출물

**낮은 점수 신호:**

- 회의, 리서치, 전략 문서 중심이고 구현 경험이 거의 없음
- 사용 기술은 적혀 있으나 실제 완성물이나 결과가 불명확함
- 실험은 했지만 사용자나 비즈니스에 연결된 결과가 없음

**0~10 점수 기준:**

- 0~2점: 실제 build 경험이 거의 없음
- 3~5점: 학습용 또는 제한적 프로젝트 경험은 있으나 실사용 맥락이 약함
- 6~8점: 작동하는 도구나 시스템을 여러 번 만든 경험이 있음
- 9~10점: 복잡한 문제를 실제 사용자 또는 조직이 쓰는 산출물로 만든 경험이 강함

### Axis 3. AI Leverage and Technical Fluency

**정의:** AI 도구, 모델, 프롬프트, 데이터, automation을 목적에 맞게 사용하고 그 한계를 이해하는 능력이다.

AI Builder는 반드시 PhD-level ML researcher일 필요는 없지만, AI를 단순 유행어로 쓰는 것이 아니라 실제 workflow 안에 적용할 수 있어야 한다. Resume에서 LLM, RAG, agents, prompt engineering, evaluation, automation, model integration, API usage, ML/analytics, AI governance 관련 경험을 본다.

**높은 점수 신호:**

- LLM 또는 AI API를 활용해 실제 workflow를 개선한 경험
- RAG, agent, prompt evaluation, model comparison, human review loop 등 AI 시스템 설계 경험
- AI의 한계, hallucination, evaluation, data quality에 대한 언급
- AI를 기술 자체가 아니라 사용자 문제 해결에 연결한 경험

**낮은 점수 신호:**

- AI 관련 키워드는 많지만 구체적 사용 사례가 없음
- ChatGPT 사용 경험 정도만 있고 시스템화 경험이 부족함
- 모델 성능 검증이나 위험 관리에 대한 인식이 보이지 않음

**0~10 점수 기준:**

- 0~2점: AI 활용 경험이 거의 없음
- 3~5점: 개인 생산성 또는 단순 실험 수준의 AI 사용 경험
- 6~8점: AI를 제품, 업무 자동화, 분석, 의사결정 workflow에 적용한 경험
- 9~10점: AI 시스템을 설계, 평가, 운영하거나 조직 내 adoption까지 연결한 경험

### Axis 4. Enterprise Judgment and Governance

**정의:** 기업 환경에서 필요한 보안, 개인정보, 리스크, 확장성, 운영 가능성, 거버넌스를 고려하는 능력이다.

KPMG 같은 조직에서는 빠르게 만드는 능력만큼이나 안전하게 적용하는 판단이 중요하다. Resume에서 regulated industry, security, privacy, compliance, risk management, auditability, deployment process, MLOps, DevOps, stakeholder approval 경험을 본다.

**높은 점수 신호:**

- 보안, 개인정보, compliance, audit, governance를 고려한 프로젝트 경험
- enterprise client 또는 복잡한 조직 환경에서 솔루션을 만든 경험
- 운영, 유지보수, 확장성, monitoring, documentation을 고려한 경험
- 빠른 실험과 리스크 관리 사이의 균형을 잡은 사례

**낮은 점수 신호:**

- 개인 프로젝트나 실험은 많지만 기업 적용 가능성 설명이 부족함
- 데이터 보안, privacy, governance에 대한 언급이 없음
- production 또는 운영 경험이 전혀 보이지 않음

**0~10 점수 기준:**

- 0~2점: enterprise risk 인식이 거의 없음
- 3~5점: 제한적 운영 경험은 있으나 governance 관점이 약함
- 6~8점: 기업 환경에서의 운영, 보안, 협업 경험이 명확함
- 9~10점: 복잡한 enterprise 환경에서 혁신과 리스크 관리를 함께 다룬 경험이 강함

### Axis 5. Stakeholder and User-Centered Thinking

**정의:** 사용자, 비즈니스 리더, 운영팀, 기술팀, 리스크 담당자 등 다양한 이해관계자의 요구를 균형 있게 이해하는 능력이다.

AI Builder는 혼자 모델을 만드는 역할이 아니라, 여러 stakeholder가 실제로 사용할 수 있는 솔루션을 만들어야 한다. Resume에서 user research, client-facing work, workshop, consulting, cross-functional collaboration, product management, change management 경험을 본다.

**높은 점수 신호:**

- 비기술 사용자와 협업하거나 요구사항을 수집한 경험
- 다양한 팀과 함께 제품 또는 workflow를 만든 경험
- 사용자 adoption, training, documentation, feedback loop 경험
- 비즈니스 가치와 사용자 경험을 함께 고려한 사례

**낮은 점수 신호:**

- 기술 구현 경험은 있으나 사용자가 누구인지 불명확함
- 혼자 수행한 프로젝트 위주이고 협업 맥락이 부족함
- stakeholder conflict 또는 tradeoff를 다룬 경험이 보이지 않음

**0~10 점수 기준:**

- 0~2점: 사용자나 stakeholder 관점이 거의 없음
- 3~5점: 협업 경험은 있으나 주도적 stakeholder 관리 경험은 약함
- 6~8점: 다양한 stakeholder와 협업하며 요구를 제품에 반영한 경험
- 9~10점: 복잡한 이해관계자 환경에서 alignment를 만들고 adoption까지 이끈 경험

### Axis 6. Communication, Learning Agility, and Evidence of Growth

**정의:** 자신의 판단, 결과, 한계, 학습 과정을 명확히 설명하고 새로운 도메인에 빠르게 적응하는 능력이다.

AI Builder 후보자는 다양한 배경에서 올 수 있기 때문에, 특정 전공이나 커리어 경로보다 학습 속도와 설명 능력이 중요하다. Resume에서 domain switching, self-taught projects, public writing, teaching, presentations, leadership, career transition, fast upskilling 경험을 본다.

**높은 점수 신호:**

- 새로운 기술이나 도메인을 빠르게 배워 적용한 경험
- 복잡한 내용을 비기술자에게 설명한 경험
- 문서화, 발표, 교육, thought leadership, portfolio evidence
- 실패나 한계를 인식하고 개선한 경험

**낮은 점수 신호:**

- 경험 나열은 있으나 본인의 역할과 배운 점이 불명확함
- 커뮤니케이션, 문서화, 설명 관련 증거가 부족함
- 변화하는 환경에서 학습한 흔적이 적음

**0~10 점수 기준:**

- 0~2점: 커뮤니케이션과 학습 민첩성 증거가 거의 없음
- 3~5점: 일부 학습 또는 설명 경험은 있으나 구체성이 약함
- 6~8점: 새로운 문제를 배우고 설명하며 결과로 연결한 경험이 명확함
- 9~10점: 다양한 도메인을 넘나들며 빠르게 학습하고 다른 사람까지 이끈 경험이 강함

## 6개 Axis 요약

| Axis | 평가 초점 | Resume에서 찾을 핵심 근거 |
| --- | --- | --- |
| Problem Framing and Ambiguity Handling | 모호한 문제를 구조화하는 능력 | discovery, strategy, scoping, problem definition |
| Practical Building and Execution | 실제 산출물을 만드는 능력 | prototype, app, workflow, automation, deployment |
| AI Leverage and Technical Fluency | AI를 실용적으로 적용하는 능력 | LLM, RAG, agent, prompt, evaluation, AI workflow |
| Enterprise Judgment and Governance | 기업 환경의 리스크 판단 | security, privacy, compliance, MLOps, auditability |
| Stakeholder and User-Centered Thinking | 여러 이해관계자를 고려하는 능력 | client-facing, UX, workshops, cross-functional work |
| Communication, Learning Agility, and Growth | 설명력과 학습 속도 | writing, presentation, self-taught, domain transition |

## 공정성을 위한 중요한 설계 원칙

- 학교명, 회사 브랜드, 나이, 성별, 국적, 사진, 주소 같은 요소는 평가 점수에 직접 반영하지 않는다.
- Resume의 빈틈을 자동으로 낮은 점수로 해석하지 않는다. 정보가 부족하면 "unknown" 또는 "needs follow-up"으로 표시한다.
- 비전통적 경력, self-taught path, operations/product/UX/consulting background도 점수를 받을 수 있도록 각 axis의 evidence type을 넓게 설계한다.
- 최종 의사결정은 AI 점수만으로 하지 않고, reviewer가 근거와 후속 질문을 확인한 뒤 결정한다.
- 각 점수에는 반드시 evidence quote 또는 extracted rationale을 붙여 audit 가능하게 만든다.

---

파이프라인

1. 지원자가 Apply 
2. 해당 정보를 6개 주요 지표 하에 정성적으로 산출됨
3. 해당 내용을 기존 산출된 평가지표에 따라 점수 산출

[질문 2: 해당 파이프라인을 체계적으로 구현해줘]

## 답변 2: Resume 기반 AI Builder 후보자 평가 파이프라인 설계

이 파이프라인의 목적은 Resume를 자동으로 단순 합격/불합격 처리하는 것이 아니라, reviewer가 더 일관되고 근거 있는 판단을 하도록 돕는 것이다. 따라서 시스템은 "AI-assisted evaluation workbench"로 설계한다. AI는 Resume에서 관련 근거를 추출하고 6개 axis별 예비 점수와 설명을 제공하지만, 최종 판단은 사람이 검토한다.

## 전체 파이프라인 개요

1. Candidate Apply
2. Resume Intake and Pre-processing
3. Sensitive/Irrelevant Information Filtering
4. Evidence Extraction by Axis
5. Qualitative Assessment Generation
6. Quantitative Scoring
7. Confidence and Risk Flagging
8. Reviewer Dashboard Visualization
9. Human Review and Calibration
10. Final Evaluation Summary and Follow-up Questions

## Step 1. Candidate Apply

지원자는 Resume를 제출한다. 실제 제품이라면 PDF, DOCX, LinkedIn export, portfolio link 등을 받을 수 있지만, 이번 3시간 prototype에서는 sample resume text를 textarea에 붙여넣는 방식으로 구현해도 충분하다.

**입력 데이터:**

- 후보자 이름 또는 익명 ID
- Resume text
- 선택 입력: portfolio link, GitHub link, personal website
- 선택 입력: candidate background category는 평가에 직접 쓰지 않고 diversity monitoring 또는 calibration 용도로만 사용

**중요한 원칙:**

- 과제 prototype에서는 synthetic resume만 사용한다.
- 개인정보는 저장하지 않거나, demo에서는 mock data로만 처리한다.
- 평가자는 Resume 원문과 AI 요약을 함께 볼 수 있어야 한다.

## Step 2. Resume Intake and Pre-processing

Resume를 평가 가능한 구조로 변환한다. 이 단계에서는 문서를 그대로 점수화하지 않고, 프로젝트, 역할, 기술, 성과, 도메인, 협업 경험 등 평가에 필요한 단서로 분리한다.

**처리 내용:**

- Resume text 정리
- bullet point 단위로 분해
- 프로젝트/경험/기술/성과/교육/자격 등 섹션 분류
- 중복 문장 제거
- 너무 짧거나 정보가 부족한 항목 표시

**예시 출력 구조:**

```json
{
  "candidate_id": "sample-001",
  "experiences": [
    {
      "title": "Built internal LLM workflow for document review",
      "context": "consulting operations",
      "signals": ["AI workflow", "stakeholder collaboration", "automation"]
    }
  ],
  "skills": ["Python", "LLM", "workflow automation", "stakeholder management"],
  "evidence_notes": ["Built prototype", "Worked with non-technical users"]
}
```

## Step 3. Sensitive/Irrelevant Information Filtering

공정성을 위해 점수 산출에 직접 쓰지 않을 정보를 분리한다. Resume에는 평가에 불필요하거나 편향을 만들 수 있는 정보가 포함될 수 있다.

**점수에 직접 반영하지 않을 정보:**

- 이름
- 사진
- 주소
- 성별
- 나이
- 국적
- 학교명 자체의 prestige
- 회사명 자체의 brand value
- 졸업연도처럼 나이를 추정할 수 있는 정보

**주의:**

학교나 회사 경험 전체를 무시하는 것은 아니다. 대신 "어디였는가"보다 "무엇을 했는가"를 본다. 예를 들어 Big Tech 출신이라는 사실보다, 그 안에서 어떤 문제를 정의했고 어떤 시스템을 만들었는지가 평가 근거가 되어야 한다.

## Step 4. Evidence Extraction by Axis

각 axis별로 Resume에서 관련 근거를 추출한다. 이 단계의 핵심은 바로 점수를 매기는 것이 아니라, 점수의 근거가 될 수 있는 evidence를 먼저 모으는 것이다.

**예시:**

### Problem Framing evidence

- "Defined roadmap for ambiguous internal AI adoption initiative"
- "Led discovery workshops with business stakeholders"
- "Scoped MVP from broad operational pain point"

### Practical Building evidence

- "Built prototype dashboard"
- "Deployed automation workflow"
- "Created API integration"

### AI Leverage evidence

- "Implemented RAG system"
- "Used LLM API to summarize documents"
- "Evaluated prompt performance"

### Enterprise Judgment evidence

- "Handled privacy-sensitive data"
- "Designed approval workflow"
- "Worked in regulated environment"

### Stakeholder Thinking evidence

- "Collaborated with legal, IT, and operations"
- "Ran user interviews"
- "Trained business users"

### Communication and Growth evidence

- "Presented to executives"
- "Documented technical workflow"
- "Self-taught ML and shipped project"

**출력 형식:**

각 axis별로 아래 내용을 저장한다.

- extracted evidence
- why it matters
- missing information
- suggested follow-up question

## Step 5. Qualitative Assessment Generation

추출된 evidence를 바탕으로 axis별 정성 평가를 생성한다. 이 단계는 dashboard에서 reviewer가 근거를 빠르게 이해하도록 도와준다.

**각 axis별 정성 평가 구성:**

- Summary: 이 후보자가 해당 축에서 보여주는 핵심 역량
- Evidence: Resume에서 확인된 근거
- Concern: 부족하거나 불확실한 부분
- Follow-up Question: 인터뷰에서 확인할 질문

**예시:**

```text
Axis: AI Leverage and Technical Fluency
Summary: Candidate shows practical experience applying LLMs to document workflows, with evidence of API integration and prompt iteration.
Evidence: Resume mentions building an internal document summarization workflow using LLM APIs.
Concern: Resume does not explain how output quality was evaluated or monitored.
Follow-up Question: How did you measure whether the AI-generated summaries were reliable enough for users?
```

## Step 6. Quantitative Scoring

정성 평가를 기반으로 0~10점 점수를 산출한다. 점수는 단순 키워드 매칭이 아니라, evidence의 강도와 구체성을 기준으로 계산한다.

**점수 산출 기준:**

- Evidence Strength: 근거가 구체적인가
- Role Ownership: 후보자가 직접 주도했는가
- Practical Impact: 결과물이 실제로 쓰였거나 measurable impact가 있는가
- Relevance: AI Builder 역할과 얼마나 관련 있는가
- Complexity: 문제의 난이도와 조직 맥락이 복잡했는가
- Recency: 최근 경험인가

**예시 scoring logic:**

```text
Base score starts at 0.
+2 if relevant experience exists.
+2 if the candidate clearly owned the work.
+2 if the work produced a tangible artifact.
+1.5 if there is measurable user/business impact.
+1.5 if the context involved ambiguity or enterprise complexity.
+1 if the resume includes evidence of reflection, evaluation, or improvement.
Cap score at 10.
```

**중요:**

- 정보가 부족하면 낮은 점수를 주기보다 confidence를 낮게 표시한다.
- 예를 들어 Resume에 AI 경험이 짧게 한 줄만 있다면, AI Leverage 점수는 중간 이하일 수 있지만 "needs follow-up"으로 표시해야 한다.
- 점수는 hiring decision이 아니라 review aid로 사용한다.

## Step 7. Confidence and Risk Flagging

AI가 산출한 점수의 신뢰도를 함께 표시한다. Resume는 후보자의 전체 역량을 완벽히 보여주지 못하므로, 점수만 보여주면 위험하다.

**Confidence 기준:**

- High: Resume에 구체적 경험, 역할, 결과, 기술, 영향이 모두 있음
- Medium: 관련 경험은 있으나 역할 또는 결과가 일부 불명확함
- Low: 키워드는 있으나 구체적 근거가 부족함

**Risk flag 예시:**

- Evidence too vague
- Possible keyword stuffing
- Strong technical profile but weak stakeholder evidence
- Strong strategy profile but limited hands-on build evidence
- Missing AI governance evidence
- Resume too sparse for reliable scoring

## Step 8. Reviewer Dashboard Visualization

대시보드는 평가자가 후보자를 빠르게 이해하되, 점수의 근거까지 확인할 수 있게 설계한다.

**대시보드 구성:**

- Candidate summary card
- 6-axis hexagon/radar chart
- 각 axis별 0~10 score
- confidence indicator
- qualitative rationale
- evidence snippets
- concerns and follow-up questions
- final reviewer notes
- recommendation: Strong Yes / Yes / Maybe / No

**화면 흐름:**

1. 왼쪽: Resume 원문 또는 요약
2. 중앙: 6각형 radar chart
3. 오른쪽: axis별 근거와 질문
4. 하단: reviewer final decision and notes

## Step 9. Human Review and Calibration

AI 점수는 최종 판단이 아니므로 reviewer가 점수를 조정하고 코멘트를 남길 수 있어야 한다.

**Human review 기능:**

- AI suggested score 확인
- reviewer adjusted score 입력
- 조정 이유 기록
- follow-up interview question 선택 또는 수정
- 최종 추천 상태 선택

**Calibration 방법:**

- 같은 sample resume를 여러 reviewer가 평가해 점수 차이를 비교
- 특정 배경 후보자에게 불리한 axis가 있는지 확인
- 합격자/불합격자 예시를 기준으로 점수 기준을 정기적으로 조정

## Step 10. Final Evaluation Summary

최종적으로 후보자별 평가 요약을 생성한다.

**최종 요약에 포함될 내용:**

- Overall recommendation
- 6-axis score table
- Top 2 strengths
- Top 2 concerns
- Interview follow-up questions
- AI-generated notes and human reviewer adjustments
- Confidence level
- Fairness/governance warning if applicable

**예시 최종 요약:**

```text
Candidate shows strong practical building ability and solid AI workflow experience, especially in creating internal automation tools. The main uncertainty is enterprise governance depth: the resume mentions AI implementation but does not explain how quality, privacy, or operational risk were managed. Recommended next step is an interview focused on AI evaluation, stakeholder tradeoffs, and responsible deployment.
```

## Prototype 구현 범위

3시간 과제 안에서는 아래 범위로 구현하는 것이 현실적이다.

**구현할 것:**

- Resume text input
- 6개 axis 정의 표시
- sample resume 불러오기
- axis별 score와 rationale 표시
- radar/hexagon chart
- confidence와 follow-up question 표시
- reviewer가 점수와 코멘트를 수정할 수 있는 UI
- 최종 요약 생성

**구현하지 않을 것:**

- 실제 채용 시스템 연동
- 개인정보 저장
- 로그인
- 실제 resume PDF parser
- 실제 AI API 자동 호출
- 완전 자동 합격/불합격 결정

## 핵심 Architecture

```text
Resume Input
  -> Pre-processing
  -> Sensitive Info Filtering
  -> Axis Evidence Extraction
  -> Qualitative Rationale Generation
  -> 0~10 Scoring per Axis
  -> Confidence and Risk Flags
  -> Hexagon Dashboard
  -> Human Reviewer Adjustment
  -> Final Evaluation Summary
```

## 이 파이프라인의 장점

- 다양한 배경의 후보자를 하나의 직함이나 학력 기준으로 평가하지 않는다.
- 점수와 근거를 함께 보여주므로 평가가 더 투명하다.
- Resume 정보가 부족한 경우 무조건 감점하지 않고 follow-up question으로 연결한다.
- AI를 최종 심판으로 쓰지 않고 reviewer의 판단을 돕는 도구로 사용한다.
- KPMG의 enterprise context에 맞게 speed, innovation, risk, governance의 균형을 보여준다.

## 이 파이프라인의 한계와 리스크

- Resume는 후보자의 실제 역량을 완전히 보여주지 못한다.
- 글을 잘 쓰는 후보자가 실제 역량보다 높게 평가될 수 있다.
- AI가 특정 키워드나 경력 패턴을 과대평가할 수 있다.
- 비전통적 경력의 evidence가 Resume에 잘 표현되지 않으면 낮게 평가될 위험이 있다.
- 따라서 이 도구는 screening automation이 아니라 structured review assistant로 포지셔닝해야 한다.

## 발표에서 강조할 포인트

이 솔루션은 후보자를 자동으로 걸러내는 AI hiring tool이 아니다. 목적은 채용팀이 AI Builder 후보자를 더 일관되고 투명하게 평가하도록 돕는 것이다. Resume에서 6개 역량 축의 근거를 추출하고, 점수와 함께 불확실성, 리스크, 후속 질문을 보여줌으로써 단순 자동화가 아니라 responsible human-in-the-loop evaluation workflow를 만드는 데 초점을 둔다.