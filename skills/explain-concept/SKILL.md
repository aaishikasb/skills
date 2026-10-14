---
name: explain-concept
description: Teach a difficult developer concept with a precise mental model, worked example, and application check. Use for explanations of edge AI, hardware, robotics, or their underlying software concepts.
license: MIT
---

# Explain a concept

Help the learner use one concept to reason about a new situation, at the depth and length they requested.

## Choose the learning target

Establish the learner's starting knowledge and the question or decision the concept should help them answer. Infer these from the conversation when possible. Ask only when the missing context changes the explanation; do not turn a narrow question into a course-planning interview.

Select the smallest prerequisite set. Define unfamiliar terms at first use and connect the explanation to a concrete task the learner recognizes. If a question contains a misconception, correct it directly and explain the consequence for that task.

## Explain and demonstrate

Start with a precise plain-language model of the mechanism. Use an analogy only if it makes a difficult relationship easier to understand; map it to the real mechanism and state where it stops working.

Work through one representative example with visible intermediate reasoning. Use consistent units, coordinate-frame names, conventions, and assumptions. Check arithmetic or small code examples with available tools when that materially improves confidence. Label hypothetical values; a teaching example is not a benchmark or device specification.

Show a boundary case or counterexample that exposes the most consequential misconception. Distinguish general principles from implementation-dependent behavior. For device limits, pinouts, API behavior, or version-specific claims, consult authoritative sources for that implementation or explicitly leave the claim unresolved.

For example, a lesson about coordinate transforms should make frame direction and units explicit; a lesson about quantization should distinguish representation, task quality, and runtime support. Include only distinctions relevant to the learner's question.

## Check transfer

End with a small application task that changes one meaningful part of the worked example. Ask for a prediction or decision with a reason, not a repeated definition. Give the answer and reasoning separately after the prompt when producing a standalone explanation. In an interactive lesson, wait for the learner's answer before revealing it and adapt to their reasoning. If the user requests only a short explanation, keep the check proportionate or omit it.

Deliver in the requested format. The explanation is complete when the stated question is answered, the example demonstrates the mechanism, and important assumptions and limits are explicit. Describe a transfer task as a proposed check until a learner actually completes it; do not infer comprehension from a polished explanation.
