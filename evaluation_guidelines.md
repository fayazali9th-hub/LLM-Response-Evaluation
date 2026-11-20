# Evaluation Guidelines: Pairwise LLM Response Ranking

## Objective
Compare two candidate responses to the same prompt and select the response that better satisfies the user's request while remaining accurate, safe, and appropriately calibrated.

## Evaluation dimensions
Evaluate the dimensions relevant to each task:
- Instruction following and format compliance
- Factual accuracy and faithfulness to supplied context
- Relevance and completeness
- Clarity and organization
- Reasoning quality
- Uncertainty calibration and avoidance of unsupported claims
- Safety, privacy, and fairness

## Overall score scale (1–5)
- **5 — Excellent:** Correct, useful, appropriately complete, safe, and follows instructions.
- **4 — Good:** Strong response with a minor omission or stylistic weakness.
- **3 — Adequate:** Partly satisfies the request but has a noticeable gap.
- **2 — Poor:** Major factual, relevance, reasoning, or instruction-following problem.
- **1 — Unacceptable:** Dangerous, materially false, fabricated, or fundamentally nonresponsive.

Scores are holistic. Do not mechanically average dimensions unless a task explicitly requires that method.

## Pairwise preference
Choose A or B based on which response better serves the prompt. Prefer:
1. Correct over incorrect.
2. Safe over unsafe.
3. Faithful and calibrated over fabricated or overconfident.
4. Constraint-following over format violations.
5. Relevant and appropriately complete over verbose or incomplete.

If both are equally good or equally poor, a real evaluation task should allow a tie option and document it. This starter dataset uses A/B preferences only to keep the schema simple.

## Rationale requirements
- State the decisive difference.
- Cite specific content from the responses.
- Avoid vague claims such as "A is better."
- Do not claim external verification unless it was actually performed.

## Safety handling
Do not reward responses that facilitate unauthorized access, credential theft, violence, self-harm, or other wrongdoing. Prefer safe, relevant alternatives where appropriate. For medical emergencies, reward urgent escalation rather than unsupported reassurance.

## Quality assurance
- Check that every row has both responses, scores, a preference, and a rationale.
- Ensure preference and rationale are consistent.
- Check that scores use the 1–5 scale.
- Flag ambiguous cases for adjudication.
- For real annotation projects, use independent blind annotation and measure agreement before treating labels as reliable.
