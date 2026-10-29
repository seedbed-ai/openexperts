---
name: determine-next-action
description: Determine next best action for a deal based on email classification
inputs:
  - name: classification
    type: object
    description: Output from classify-email-intent
  - name: deal_context
    type: object
    description: Current deal details from CRM
outputs:
  - name: action
    type: string
  - name: reasoning
    type: string
  - name: confidence
    type: string
    enum: [high, medium, low]
tools:
  - crm
knowledge:
  - knowledge/meddpicc.md
  - knowledge/competitive-battle-cards.md
---

## Determine Next Action

Given an email classification and deal context, determine the next best action.

**Knowledge route:** For an unknown economic buyer, start at [qualification topic](../knowledge/topics/qualification.md), read only the relevant [MEDDPICC criteria](../knowledge/meddpicc.md#criteria), and use real deal context before proposing follow-up. For a named competitor or buyer delay, navigate via the [competition topic](../knowledge/topics/competition.md) to the applicable battle-card section. Do not pre-read every competitor or claim market freshness from an index.

**Inputs and authority:** If classification or deal context is missing, ask for it or explain the provisional recommendation. A declared CRM tool is not evidence that a connector is available; draft actions without performing unapproved writes.

### Decision Rules

- For `objection` → prepare a competitive rebuttal and schedule a call.
- For `buying_signal` → advance deal stage and prepare a proposal or next-step email.
- For `churn_risk` → flag deal as at-risk and recommend an executive outreach.
- For `question` → draft an informative reply with relevant materials.
- For `scheduling` → check calendar availability and propose meeting times.

### Output

Return:
- Action description
- Reasoning (1-2 sentences)
- Confidence
