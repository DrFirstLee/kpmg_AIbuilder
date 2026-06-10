

[평가의 6개 축]
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