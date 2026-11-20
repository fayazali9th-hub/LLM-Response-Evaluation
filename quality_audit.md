# Quality Audit

## Structural validation
- Number of paired examples: 20
- Unique example IDs: 20
- Missing required fields: 0
- Scores outside 1–5: 0
- Invalid preference labels: 0
- Missing rationales: 0

## Preference distribution
All 20 examples prefer response A. This is a deliberate limitation of this starter set: it makes the examples easy to inspect but creates a position/label imbalance. It should not be used to train a preference model or claim unbiased evaluation performance.

## Quality limitations
- Synthetic examples and responses; no live model outputs.
- Scores and preferences are author-created illustrative judgments.
- No second annotator or adjudication pass.
- No inter-annotator agreement statistic.
- Response A is always preferred; response order is not randomized.
- Coverage is broad but small and not statistically representative.

## Recommended next iteration
1. Add examples where B is clearly preferred.
2. Randomize A/B order before annotation.
3. Add a `tie_or_uncertain` option.
4. Collect independent labels from at least two annotators.
5. Adjudicate disagreements and calculate Cohen's kappa (or another suitable agreement measure).
6. Expand coverage with domain-specific and adversarial cases.
