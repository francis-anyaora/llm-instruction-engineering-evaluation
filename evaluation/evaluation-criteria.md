# LLM Evaluation Criteria and Scoring Rubric

## Overview

This document establishes a structured framework for assessing large language model responses across different dimensions of quality, instruction compliance, and factual reliability.

The framework is intended to support consistent evaluation, identify specific model response shortcomings, and provide actionable feedback for improvement.

Evaluation criteria should be selected according to the requirements of the task. Not every criterion will apply equally to every response.

## 1. Scoring Scale

Each applicable evaluation dimension is assessed using the following five-point scale.

| Score | Rating | Description |
|---|---|---|
| 5 | Excellent | Fully satisfies the evaluation requirements without any significant shortcomings. |
| 4 | Good | Meets the requirements with only minor deficiencies that do not materially affect the response. |
| 3 | Satisfactory | Meets the principal requirements but contains noticeable shortcomings requiring improvement. |
| 2 | Poor | Demonstrates significant deficiencies that undermine the quality or reliability of the response. |
| 1 | Very Poor | Fails to satisfy essential requirements or contains serious errors or violations. |
| N/A | Not Applicable | The evaluation dimension is not relevant to the task being assessed. |

## 2. Evaluation Dimensions

### A. Instruction Following

**Objective:** Determine whether the model correctly interprets and complies with applicable instructions.

Assessment considerations:
- Compliance with explicit instructions and task requirements.
- Adherence to specified constraints and operational boundaries.
- Appropriate handling of conditional instructions.
- Compliance with required response structures.
- Avoidance of prohibited or unintended behaviour.

A response may be relevant and factually correct but still receive a low score if it violates important instructions.

### B. Factuality

**Objective:** Assess whether claims made in the response are supported by available evidence.

Assessment considerations:
- Whether factual assertions have adequate supporting evidence.
- Whether the response introduces unsupported claims.
- Whether uncertainty is appropriately acknowledged.
- Whether claims are consistent with the available reference material.

### C. Accuracy

**Objective:** Determine whether the information and conclusions presented are correct in relation to the task and its subject matter.

Assessment considerations:
- Correctness of factual statements.
- Proper interpretation of supplied information.
- Accuracy of explanations and conclusions.
- Absence of material errors or misrepresentations.

### D. Relevance

**Objective:** Determine whether the response addresses the user's actual request.

Assessment considerations:
- Alignment with the user's intent.
- Relevance of the information presented.
- Avoidance of unnecessary digressions.
- Appropriate focus on the requested subject.

### E. Completeness

**Objective:** Assess whether the response adequately addresses the requirements of the task.

Assessment considerations:
- Coverage of the principal aspects of the request.
- Inclusion of necessary explanations or supporting details.
- Absence of significant omissions.
- Appropriate level of detail.

### F. Response Quality

**Objective:** Evaluate the overall clarity, coherence, and usefulness of the generated response.

Assessment considerations:
- Logical organization and flow.
- Clarity of expression.
- Appropriate terminology.
- Readability and coherence.
- Consistency throughout the response.

### G. Format Compliance

**Objective:** Determine whether the response follows prescribed presentation and formatting requirements.

Assessment considerations:
- Compliance with the required output structure.
- Correct use of headings, lists, tables, or other specified formats.
- Appropriate citation presentation.
- Consistent terminology and formatting.
- Avoidance of unwanted internal artifacts or implementation details.

### H. Source Grounding

**Objective:** Evaluate whether the response appropriately relies on the designated information sources.

Assessment considerations:
- Whether relevant retrieved information supports the response.
- Whether generated claims can be traced to the supporting material.
- Whether citations accurately correspond to their referenced sources.
- Whether the response introduces information unsupported by the retrieved material.
- Whether limitations in the available evidence are appropriately recognized.

## 3. Recording Evaluation Results

Each evaluation should record the following:

| Field | Description |
|---|---|
| Task or Query | The instruction or user request being evaluated. |
| Evaluation Dimension | The criterion being assessed. |
| Score | The assigned rating from 1 to 5, or N/A. |
| Evidence | Specific observations supporting the assessment. |
| Identified Shortcoming | The particular issue detected, where applicable. |
| Recommended Improvement | An actionable recommendation addressing the issue. |

## 4. Evaluation and Critical Failures

An overall assessment should consider the nature and severity of identified shortcomings rather than relying exclusively on an average score.

Some failures may be sufficiently serious to undermine an otherwise strong response.

Examples include:
- Materially violating an essential system instruction.
- Presenting fabricated or unsupported information as established fact.
- Misrepresenting the contents of a reference source.
- Providing citations that do not support the associated claims.
- Disclosing information prohibited by applicable instructions.

Such failures should be explicitly documented and considered when determining the overall assessment.

## 5. Evaluation Principles

- **Consistency:** Apply comparable standards across similar tasks.
- **Objectivity:** Base ratings on observable response behaviour and supporting evidence.
- **Specificity:** Identify the precise shortcoming rather than providing vague criticism.
- **Context awareness:** Interpret response quality in relation to the task and applicable instructions.
- **Actionability:** Provide recommendations that can inform subsequent improvements.

## 6. Scope and Limitations

This framework provides a general-purpose evaluation structure. Individual tasks may require additional criteria, specialized reference materials, or adjusted assessment requirements.

Scores should be supported by specific observations rather than subjective impressions alone.

The framework is intended to support human evaluation and iterative improvement; it does not constitute a validated benchmark or claim that all evaluation dimensions can be measured objectively.

## Conclusion

A structured evaluation framework makes it possible to distinguish different forms of model failure and assess response quality beyond surface-level fluency.

By evaluating instruction compliance, factual support, accuracy, relevance, completeness, and presentation independently, evaluators can provide more precise feedback and identify opportunities for improving model behaviour.
