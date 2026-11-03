# Sample LLM Response Assessments

## Overview

This document presents illustrative examples of manual LLM response evaluation.

Each assessment includes a task context, relevant reference material or instructions, a generated response, evaluation scores, supporting observations, and recommended improvements.

The examples demonstrate the application of structured evaluation criteria to identify model shortcomings and provide actionable feedback.

These are independently constructed assessment exercises. They are not presented as actual production model outputs or results from a validated evaluation benchmark.

---

## Assessment 1: Knowledge Grounding and Factual Accuracy

### Evaluation Objective

Assess whether a model can answer a question using only the supplied reference material, acknowledge limitations in the available evidence, and avoid introducing unsupported claims.

### Reference Material

The following is an invented procedural rule created solely for this evaluation exercise:

> Section 5: A request for administrative review must be submitted within 14 calendar days after the notice is received. This provision does not specify any extension or exception to the stated period.

### User Query

According to the supplied provision, what is the deadline for submitting a request for administrative review? Does the provision permit an extension?

### Applicable Requirements

- Answer using only the supplied reference material.
- Distinguish between information expressly stated and matters not addressed by the provision.
- Do not introduce unsupported exceptions or additional legal rules.
- Provide a clear and direct response.

### Illustrative Model Response

"The request must be submitted within 30 days of receiving the notice. However, an extension may be granted where the applicant demonstrates sufficient cause for the delay."

### Evaluation

| Evaluation Dimension | Score | Assessment |
|---|---:|---|
| Instruction Following | 1 | The response introduces information not contained in the supplied material. |
| Factuality | 1 | The claims are unsupported by the reference material. |
| Accuracy | 1 | The stated 30-day deadline contradicts the supplied 14-day period. |
| Relevance | 4 | The response addresses both parts of the question. |
| Completeness | 2 | It attempts to address the deadline and extension but does so incorrectly. |
| Response Quality | 4 | The response is clear and grammatically coherent. |
| Format Compliance | 5 | It follows the expected direct-answer presentation. |
| Source Grounding | 1 | Neither the deadline nor the asserted extension is supported by the supplied provision. |

### Identified Shortcomings

1. **Incorrect deadline:** The response gives 30 days instead of the 14 calendar days specified in the reference.
2. **Unsupported exception:** It introduces an extension based on sufficient cause, which is not established by the supplied provision.
3. **Failure to acknowledge limitations:** It does not distinguish between what the provision states and what it leaves unaddressed.

### Recommended Correction

The response should state that the deadline is 14 calendar days after receipt of the notice. It should also clarify that the supplied provision does not specify whether an extension is available.

### Illustrative Improved Response

"Under the supplied provision, a request for administrative review must be submitted within 14 calendar days after receiving the notice. The provision does not specify whether this period can be extended."

### Evaluation Conclusion

The response is fluent and relevant but fails important requirements concerning accuracy, instruction following, and source grounding.

This example demonstrates why response fluency should not be mistaken for factual reliability.

---

## Assessment 2: Judicial Decision Interpretation

### Evaluation Objective

Assess whether a model can distinguish between a litigant's arguments and the court's actual decision when analysing a judicial proceeding.

### Reference Material

The following is an invented case summary created solely for this evaluation exercise:

**Example Holdings Ltd v Sample Authority**

- The claimant argued that the notice issued by the authority was invalid.
- The court did not determine the validity of the notice.
- The court dismissed the claim because it was filed outside the applicable 30-day period.
- The validity of the notice was therefore not determined in the proceeding.

### User Query

What was the claimant's argument, and what did the court actually decide?

### Applicable Requirements

- Distinguish the claimant's argument from the court's determination.
- Report the court's decision accurately.
- Do not attribute an argument to the court.
- Do not infer findings that are absent from the reference material.

### Illustrative Model Response

"The court held that the notice issued by the authority was invalid and ruled in favour of the claimant. It therefore established that the authority's notice could not stand."

### Evaluation

| Evaluation Dimension | Score | Assessment |
|---|---:|---|
| Instruction Following | 1 | The response fails to distinguish the claimant's argument from the court's decision. |
| Factuality | 1 | Its central claims are unsupported by the case summary. |
| Accuracy | 1 | It misrepresents the court's actual disposition. |
| Relevance | 3 | It addresses the subject but does not answer it correctly. |
| Completeness | 2 | It omits the claimant's actual argument and the procedural reason for dismissal. |
| Response Quality | 3 | The response is understandable but substantively misleading. |
| Format Compliance | 5 | It does not violate a specific formatting requirement. |
| Source Grounding | 1 | The asserted judicial finding contradicts the supplied case summary. |

### Identified Shortcomings

1. **Misattribution:** The response attributes the claimant's argument to the court.
2. **Incorrect disposition:** It says the court ruled in favour of the claimant when the claim was dismissed.
3. **Invented judicial finding:** It suggests that the court determined the notice was invalid, although the summary expressly states that this question was not decided.

### Recommended Correction

The response should separately identify the claimant's position and the court's determination. It should also explain that the court dismissed the claim on procedural grounds without determining the validity of the notice.

### Illustrative Improved Response

"The claimant argued that the authority's notice was invalid. However, the court did not determine that issue. It dismissed the claim because it was filed outside the applicable 30-day period."

### Evaluation Conclusion

The response demonstrates a serious failure in judicial decision interpretation.

This assessment illustrates the importance of distinguishing parties' submissions from judicial findings and the actual outcome of a proceeding.

---

## Assessment 3: Instruction Following and Format Compliance

### Evaluation Objective

Assess whether a model can comply with explicit output requirements and avoid unnecessary additions.

### User Query

Explain the purpose of response evaluation using exactly three bullet points.

Each bullet point must address one of the following:

- Identifying instruction-following failures.
- Detecting factual or accuracy problems.
- Supporting improvements in model behaviour.

Do not include an introduction or conclusion.

### Applicable Requirements

- Provide exactly three bullet points.
- Address all three specified subjects.
- Do not include an introduction.
- Do not include a conclusion.
- Keep the response focused on the requested task.

### Illustrative Model Response

"Response evaluation is an important part of improving AI systems.

1. It helps identify whether a model follows instructions.
2. It can reveal factual errors and inaccurate information.
3. It provides feedback that can support improvements in model behaviour.
4. It helps organisations improve overall AI performance.

In conclusion, evaluation makes AI systems more reliable and useful."

### Evaluation

| Evaluation Dimension | Score | Assessment |
|---|---:|---|
| Instruction Following | 2 | The response addresses the requested topics but violates explicit structural requirements. |
| Factuality | N/A | The assessment does not depend on verifying external factual claims. |
| Accuracy | 4 | The explanations are generally consistent with the requested subjects. |
| Relevance | 4 | The content is relevant to the task. |
| Completeness | 5 | All three requested subjects are addressed. |
| Response Quality | 3 | The response is understandable but contains unnecessary material. |
| Format Compliance | 1 | It includes an introduction, a conclusion, and four numbered items instead of exactly three bullet points. |
| Source Grounding | N/A | No external reference material or retrieval-grounding requirement applies. |

### Identified Shortcomings

1. **Incorrect list structure:** The model uses numbered items instead of bullet points.
2. **Incorrect item count:** It provides four items instead of exactly three.
3. **Unrequested introduction:** It adds introductory text despite the explicit restriction.
4. **Unrequested conclusion:** It adds a concluding statement that was expressly prohibited.

### Recommended Correction

Remove the introductory and concluding statements, use bullet points instead of numbered items, and retain exactly three items corresponding to the requested subjects.

### Illustrative Improved Response

- **Instruction-following assessment:** Identifies whether a model complies with applicable instructions and task requirements.
- **Error detection:** Helps identify factual errors, inaccurate interpretations, and unsupported claims.
- **Behavioural improvement:** Provides actionable feedback that can guide subsequent improvements in model behaviour.

### Evaluation Conclusion

The response demonstrates that a model can communicate relevant information while still failing explicit task requirements.

This illustrates why semantic correctness and instruction compliance should be evaluated independently.

---

## General Assessment Principles

The examples above illustrate several important evaluation principles:

1. A fluent response is not necessarily accurate or factually reliable.
2. Relevant information does not compensate for significant instruction-following failures.
3. Claims must be assessed against the applicable reference material when a task requires source-based responses.
4. Evaluation scores should be supported by specific observations.
5. Recommended corrections should address the identified shortcomings rather than merely describe them.
6. A response may perform well on some evaluation dimensions while failing others.

## Scope and Limitations

These assessments are illustrative exercises based on independently constructed examples.

Their scores demonstrate how the proposed evaluation rubric can be applied. They should not be interpreted as empirical model performance results or as evidence of evaluations conducted on a particular production model.

Actual assessments should be based on the relevant task instructions, model outputs, and supporting reference materials.
