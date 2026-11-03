# Instruction Refinement Case Study

## Overview

This case study illustrates an approach to identifying instruction-related shortcomings in LLM responses and refining instructions to improve the intended model behaviour.

It demonstrates the relationship between instruction clarity, response evaluation, and iterative improvement.

The example is independently constructed and does not reproduce any proprietary production instructions or confidential application details.

## 1. Problem Identification

In a Retrieval-Augmented Generation (RAG) application, a model may produce plausible information that is not supported by the retrieved material.

This can happen even when the response is coherent, relevant, and confidently presented.

The challenge is to establish clear behavioural expectations for situations where the available evidence does not adequately support a requested conclusion.

## 2. Illustrative Scenario

A user asks:

"Does the supplied policy allow an application deadline to be extended?"

The retrieved reference material states:

"Applications must be submitted within 14 calendar days after receiving the notice."

The material does not address extensions or exceptions.

### Illustrative Model Response

"Applications must be submitted within 14 calendar days. However, applicants may request an extension where they can demonstrate reasonable grounds for the delay."

### Identified Problem

Although the response correctly identifies the stated deadline, it introduces an extension provision that is not supported by the retrieved material.

The model has combined supported information with an unsupported assertion.

## 3. Initial Instruction Assessment

A general instruction to answer questions using retrieved documents may establish a broad knowledge-source expectation without sufficiently clarifying how the model should handle information absent from those documents.

The identified shortcoming is therefore not necessarily a retrieval failure. It may also involve insufficiently precise behavioural instructions.

Relevant considerations include:

- How should the model handle information not addressed by retrieved materials?
- Should it distinguish between explicit provisions and matters left unspecified?
- How should it communicate uncertainty?
- What should prevent it from filling evidentiary gaps with assumptions?

## 4. Instruction Refinement Approach

The refinement process focuses on making the expected behaviour more explicit.

Potential improvements include:

- Clarifying the distinction between supported information and unsupported assumptions.
- Establishing expectations for handling insufficient evidence.
- Discouraging the introduction of exceptions or conditions not established by the available material.
- Requiring appropriate acknowledgement of unresolved questions.
- Preserving the distinction between retrieved evidence and information that has not been established.

The objective is to reduce ambiguity in the applicable instructions without introducing unnecessary repetition or excessive complexity.

## 5. Expected Behaviour After Refinement

Following the proposed refinement, the model should distinguish between the stated deadline and the absence of information about extensions.

### Illustrative Improved Response

"The supplied provision requires applications to be submitted within 14 calendar days after receiving the notice. It does not specify whether an extension is available."

This response addresses the user's question without introducing an unsupported exception.

## 6. Evaluation of the Refinement

The proposed improvement can be assessed using the following criteria:

| Evaluation Dimension | Assessment Expectation |
|---|---|
| Instruction Following | The response adheres to the applicable knowledge-source requirements. |
| Factuality | Claims are supported by the supplied material. |
| Accuracy | The stated deadline is represented correctly. |
| Source Grounding | No unsupported extension provision is introduced. |
| Relevance | Both aspects of the user's question are addressed. |
| Completeness | The limitation of the available information is acknowledged. |
| Response Quality | The answer is clear, direct, and appropriately qualified. |

## 7. Iterative Improvement

Instruction refinement should be treated as an iterative process rather than a one-time exercise.

A proposed improvement should be followed by further evaluation to determine whether the intended behaviour has been achieved.

Where shortcomings persist, additional refinement may be necessary.

The process involves:

1. Identifying an observable model behaviour problem.
2. Determining the likely source of the problem.
3. Reviewing the relevant instruction requirements.
4. Formulating a targeted refinement.
5. Assessing subsequent model responses.
6. Recording the findings and determining whether further improvement is necessary.

Importantly, an improvement should not be assumed merely because an instruction has been rewritten. Its effectiveness should be assessed through subsequent model outputs.

## 8. Key Takeaways

This case study illustrates several principles of system instruction engineering:

- Instruction precision matters when models operate under specific knowledge-source constraints.
- General behavioural expectations may require more explicit clarification.
- Unsupported claims should be evaluated independently of response fluency.
- Instruction refinement should address identified shortcomings rather than introduce unnecessary complexity.
- Subsequent model behaviour should be evaluated before claiming that a refinement was successful.

## Scope and Limitations

This is an illustrative instruction refinement exercise using synthetic reference material and a constructed model response.

It does not represent an actual production model experiment, measured performance improvement, or verified result from a deployed application.

The example demonstrates a general refinement methodology without disclosing proprietary prompts, internal instruction architecture, or confidential implementation details.
