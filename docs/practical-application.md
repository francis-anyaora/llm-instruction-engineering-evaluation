# Practical Application: Instruction Engineering in a RAG Application

## Overview

This document describes practical experience applying system instruction engineering, prompt refinement, and response evaluation during the development of Chat234, a Retrieval-Augmented Generation (RAG) application for legal and civic information.

The application was designed to support queries involving statutory provisions, judicial decisions, legal principles, and legal research.

Developing the application required more than integrating a language model with a knowledge base. It involved defining expected model behaviour, establishing knowledge-source constraints, accommodating different query requirements, and refining response presentation.

## 1. Application Context

Chat234 was developed as a conversational AI application that uses retrieved legal and civic information to support responses to user queries.

Its knowledge base included statutory materials and judicial decisions, requiring the language model to handle different forms of legal information and user expectations.

The application presented several instruction-engineering challenges, particularly around knowledge grounding, response consistency, legal analysis, and the appropriate presentation of supporting sources.

## 2. System Instruction Design

A significant part of the development involved designing structured system instructions to guide the model's behaviour across different query types.

The instructions addressed application identity, operational boundaries, knowledge-source requirements, task-specific expectations, and response presentation.

The design process required translating application requirements into explicit behavioural expectations while maintaining consistency across different interactions.

## 3. Knowledge-Source Constraints

An important design consideration was establishing a retrieval-based knowledge policy.

The instructions were designed to prioritize information retrieved from the application's vector store and discourage unsupported supplementation from general model knowledge.

This involved considering how the model should handle:

- Queries supported by retrieved statutory materials.
- Questions requiring analysis of judicial decisions.
- Requests involving legal principles and precedents.
- Questions for which retrieved information was insufficient.
- Requests combining multiple legal research requirements.

The objective was to improve the relationship between generated responses and the information available through the application's retrieval system.

These instructions established behavioural expectations; they were not a guarantee that the model's pretrained knowledge could be technically eliminated.

## 4. Handling Different Query Requirements

The application needed to accommodate different user intents without relying on a single rigid response pattern.

For example, questions involving statutory provisions could require a different presentation from requests for judgment summaries, ratio analysis, or legal research.

Instruction design therefore required attention to task-specific expectations, response completeness, terminology, and consistency.

The challenge was to accommodate these variations while maintaining the application's defined operational and knowledge-source boundaries.

## 5. Response Presentation and Source Handling

Another important aspect of the work involved controlling how generated information was presented to users.

This included considerations relating to:

- Appropriate response structure.
- Clear and consistent legal terminology.
- User-facing citation presentation.
- Accurate association between claims and supporting sources.
- Avoidance of unnecessary internal retrieval metadata in generated responses.
- Consistency in the presentation of different response types.

The objective was to make responses understandable and useful without exposing implementation-related artifacts.

## 6. Prompt Refinement and Response Evaluation

System instructions were refined iteratively during application development to address observed shortcomings in model behaviour.

This involved reviewing generated responses, identifying deviations from expected behaviour, and adjusting instruction wording where necessary.

The evaluation considerations included:

- Compliance with applicable system instructions.
- Accuracy of explanations and legal interpretations.
- Factual support from retrieved information.
- Relevance to the user's actual query.
- Completeness of the response.
- Consistency with required formatting and source-presentation expectations.

Particular attention was given to distinguishing between responses that were well-written and those that actually satisfied the application's requirements.

## 7. Technical Development Context

Chat234 was developed using a no-code application development environment, workflow automation, and OpenAI API infrastructure.

The development work provided practical exposure to the relationship between application requirements, system instructions, retrieval workflows, and generated model responses.

This experience helped establish an understanding of how instruction engineering contributes to the behaviour and reliability expectations of an AI application.

## 8. Skills Demonstrated

The development experience demonstrates practical capabilities in:

- System instruction design and refinement.
- Prompt engineering for application-specific requirements.
- Knowledge-grounding constraints for RAG applications.
- Handling diverse user intents and task requirements.
- Response structure and formatting control.
- LLM response assessment.
- Identification of instruction-following and factuality issues.
- Iterative improvement of model behaviour.

## 9. Confidentiality

This document describes general development experience and professional capabilities.

It intentionally excludes proprietary production instructions, internal instruction architecture, confidential implementation details, and private application data.

The objective is to demonstrate practical expertise without disclosing the underlying intellectual property of Chat234.

## Conclusion

Developing Chat234 provided a practical environment for applying system instruction engineering and evaluating model behaviour within a Retrieval-Augmented Generation application.

The experience involved translating functional requirements into behavioural instructions, refining model responses against expected outcomes, and addressing the challenges associated with retrieval-based legal and civic information delivery.
