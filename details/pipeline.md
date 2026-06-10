
[평가 Step 별 참고사항]

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