# Instruction Design and Refinement Methodology

## Overview

Effective system instruction engineering involves translating application requirements into precise, structured instructions that guide model behaviour across different tasks and user expectations.

My approach focuses on instruction clarity, behavioural consistency, constraint definition, and iterative refinement.

## 1. Requirements Analysis

The first step is identifying the application's functional requirements and expected model behaviours.

This involves understanding:
- The application's purpose and operational boundaries.
- The types of tasks and queries the model is expected to handle.
- Knowledge-source requirements and information constraints.
- Expected response characteristics and presentation standards.
- Potential conflicting instructions and edge cases.

## 2. Instruction Formulation

Application requirements are translated into explicit instructions that define expected model behaviour.

Particular attention is given to:
- Clear and unambiguous wording.
- Specific behavioural expectations.
- Well-defined operational constraints.
- Consistent terminology.
- Logical organization of instructions.
- Appropriate handling of conditional requirements.

## 3. Instruction Refinement

Initial instructions are reviewed and refined to address ambiguity, inconsistencies, and undesirable model behaviour.

Refinement considerations include:
- Replacing ambiguous expressions with more precise instructions.
- Removing unnecessary or repetitive wording.
- Clarifying the relationship between general and task-specific requirements.
- Resolving conflicting behavioural expectations.
- Adjusting instruction specificity where model responses fall short of the intended outcome.

## 4. Handling Dynamic Query Requirements

System instructions must accommodate variations in user intent and task requirements without losing consistency.

This involves defining appropriate behavioural expectations for different query types and ensuring that response requirements remain relevant to the task being performed.

## 5. Knowledge-Source Constraints

For Retrieval-Augmented Generation applications, instructions can establish expectations for how retrieved information should inform response generation.

Important considerations include:
- Prioritizing relevant retrieved information.
- Avoiding unsupported claims.
- Recognizing insufficient or inconclusive retrieved evidence.
- Maintaining appropriate source attribution.
- Distinguishing supported information from uncertainty.

## 6. Response Presentation

Instruction engineering also involves controlling how information is presented to users.

Areas of consideration include:
- Response structure and organization.
- Terminology and choice of words.
- Citation presentation.
- Removal of internal retrieval artifacts from user-facing responses.
- Consistency with application-specific formatting requirements.

## 7. Evaluation and Iterative Improvement

Instructions should be evaluated against actual model outputs rather than assumed to be effective simply because they are clearly written.

Observed shortcomings provide a basis for further refinement.

The evaluation process considers instruction compliance, factuality, accuracy, relevance, response quality, and adherence to formatting requirements.

## Conclusion

System instruction engineering is an iterative process that combines requirements analysis, precise instruction formulation, behavioural evaluation, and continuous refinement.

The objective is to develop instructions that consistently guide model behaviour towards the intended application outcomes while respecting defined operational and knowledge-source constraints.

This document describes general professional methodologies and does not disclose proprietary production instructions or application-specific implementation details.
