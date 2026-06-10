# Evaluation Pipeline Reference

## Overall Pipeline

1. Candidate Apply
2. Resume Intake and Pre-processing
3. Sensitive or Irrelevant Information Filtering
4. Evidence Extraction by Axis
5. Qualitative Assessment Generation
6. Quantitative Scoring
7. Confidence and Risk Flagging
8. Reviewer Dashboard Visualization
9. Human Review and Calibration
10. Final Evaluation Summary and Follow-up Questions

## Step 1. Candidate Apply

The candidate submits a resume. In a real product, the system could accept PDF, DOCX, LinkedIn exports, and portfolio links. For this 3-hour prototype, it is enough to use a PDF upload or sample resume text.

**Input data:**

- Candidate name or anonymous candidate ID
- Resume text
- Optional portfolio link, GitHub link, or personal website
- Optional candidate background category, used only for diversity monitoring or calibration, not direct scoring

**Important principles:**

- The prototype should use only synthetic resumes.
- Personal information should not be stored. For the demo, mock data should be used.
- Reviewers should be able to see both the original resume text and the AI-generated summary.

## Step 2. Resume Intake and Pre-processing

The resume is converted into an evaluation-friendly structure. This step should not score the document directly. Instead, it separates the resume into signals such as projects, roles, skills, outcomes, domains, and collaboration experience.

**Processing tasks:**

- Clean resume text
- Split text into bullet-level or sentence-level chunks
- Classify sections such as projects, experience, skills, education, certifications, and outcomes
- Remove duplicate statements
- Flag short or information-sparse sections

**Example output structure:**

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

## Step 3. Sensitive or Irrelevant Information Filtering

To support fairness, the system should separate information that should not directly influence scoring. Resumes may contain information that is irrelevant or could introduce bias.

**Information that should not directly affect scoring:**

- Name
- Photo
- Address
- Gender
- Age
- Nationality
- School prestige
- Company brand prestige
- Graduation year or other age-proxy information

**Important note:**

This does not mean school or company experience should be ignored completely. The evaluation should focus on what the candidate did, not where they did it. For example, the fact that a candidate worked at a famous company should matter less than the problem they solved, the system they built, and the ownership they demonstrated.

## Step 4. Evidence Extraction by Axis

For each evaluation axis, the system extracts relevant evidence from the resume. The key idea is to gather evidence first before generating a score.

**Examples:**

### Problem Framing Evidence

- "Defined roadmap for ambiguous internal AI adoption initiative"
- "Led discovery workshops with business stakeholders"
- "Scoped MVP from broad operational pain point"

### Practical Building Evidence

- "Built prototype dashboard"
- "Deployed automation workflow"
- "Created API integration"

### AI Leverage Evidence

- "Implemented RAG system"
- "Used LLM API to summarize documents"
- "Evaluated prompt performance"

### Enterprise Judgment Evidence

- "Handled privacy-sensitive data"
- "Designed approval workflow"
- "Worked in regulated environment"

### Stakeholder Thinking Evidence

- "Collaborated with legal, IT, and operations"
- "Ran user interviews"
- "Trained business users"

### Communication and Growth Evidence

- "Presented to executives"
- "Documented technical workflow"
- "Self-taught ML and shipped project"

**Output format for each axis:**

- Extracted evidence
- Why the evidence matters
- Missing information
- Suggested follow-up question

## Step 5. Qualitative Assessment Generation

The system generates a qualitative assessment for each axis based on the extracted evidence. This helps the reviewer quickly understand the basis for the score.

**Each axis assessment should include:**

- Summary: The core capability shown by the candidate on this axis
- Evidence: Resume-based evidence supporting the assessment
- Concern: Missing or uncertain information
- Follow-up Question: A question to ask during the interview

**Example:**

```text
Axis: AI Leverage and Technical Fluency
Summary: Candidate shows practical experience applying LLMs to document workflows, with evidence of API integration and prompt iteration.
Evidence: Resume mentions building an internal document summarization workflow using LLM APIs.
Concern: Resume does not explain how output quality was evaluated or monitored.
Follow-up Question: How did you measure whether the AI-generated summaries were reliable enough for users?
```

## Step 6. Quantitative Scoring

The system generates a 0-10 score based on the qualitative assessment. The score should be based on evidence strength and specificity, not simple keyword matching.

**Scoring criteria:**

- Evidence Strength: Is the evidence specific?
- Role Ownership: Did the candidate clearly own the work?
- Practical Impact: Was there a tangible artifact or measurable impact?
- Relevance: Is the experience relevant to the AI Builder role?
- Complexity: Did the work involve ambiguity or enterprise complexity?
- Recency: Is the experience recent?

**Example scoring logic:**

```text
Base score starts at 0.
+2 if relevant experience exists.
+2 if the candidate clearly owned the work.
+2 if the work produced a tangible artifact.
+1.5 if there is measurable user or business impact.
+1.5 if the context involved ambiguity or enterprise complexity.
+1 if the resume includes evidence of reflection, evaluation, or improvement.
Cap score at 10.
```

**Important:**

- If information is missing, the system should lower confidence rather than automatically assigning a low score.
- For example, if the resume mentions AI experience in only one short sentence, the AI Leverage score may be moderate or low, but the system should mark the axis as needs follow-up.
- The score should be used as a review aid, not as a hiring decision.

## Step 7. Confidence and Risk Flagging

The system should display the confidence level of the AI-generated score. A resume cannot fully represent a candidate's ability, so scores without confidence indicators can be misleading.

**Confidence levels:**

- High: The resume includes specific experience, role, outcome, technology, and impact
- Medium: Relevant experience exists, but the candidate's role or result is partly unclear
- Low: Keywords exist, but specific evidence is weak

**Example risk flags:**

- Evidence too vague
- Possible keyword stuffing
- Strong technical profile but weak stakeholder evidence
- Strong strategy profile but limited hands-on build evidence
- Missing AI governance evidence
- Resume too sparse for reliable scoring

## Step 8. Reviewer Dashboard Visualization

The dashboard should help reviewers understand the candidate quickly while still showing the evidence behind each score.

**Dashboard components:**

- Candidate summary card
- Six-axis hexagon or radar chart
- 0-10 score for each axis
- Confidence indicator
- Qualitative rationale
- Evidence snippets
- Concerns and follow-up questions
- Final reviewer notes
- Recommendation: Strong Yes, Yes, Maybe, or No

**Screen flow:**

1. Left area: Resume source text or summary
2. Center area: Six-axis radar or hexagon chart
3. Right area: Evidence and questions by axis
4. Bottom area: Reviewer final decision and notes

## Step 9. Human Review and Calibration

AI-generated scores should not be final decisions. Reviewers must be able to adjust scores and leave comments.

**Human review functions:**

- View AI-suggested score
- Enter reviewer-adjusted score
- Record reason for adjustment
- Select or edit follow-up interview questions
- Select final recommendation status

**Calibration methods:**

- Compare scoring patterns against synthetic candidates on the same axis
- Check whether any axis disadvantages candidates from specific backgrounds
- Regularly adjust scoring standards using example pass and no-pass profiles

## Step 10. Final Evaluation Summary

The system should generate a final evaluation summary for each candidate.

**The final summary should include:**

- Overall recommendation
- Six-axis score table
- Top two strengths
- Top two concerns
- Interview follow-up questions
- AI-generated notes and human reviewer adjustments
- Confidence level
- Fairness or governance warning, if applicable