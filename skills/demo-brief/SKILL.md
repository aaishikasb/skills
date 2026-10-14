---
name: demo-brief
description: Plan and scope a developer demo for edge AI, hardware, or robotics, with a learning outcome, feasible setup, and observable success criteria. Use before building or reshaping a demo.
license: MIT
---

# Demo brief

Turn an idea into the smallest demonstration that lets a particular developer observe and understand one useful capability.

## Establish the teaching goal

Read the supplied project, event requirements, and existing notes first. Establish the audience's starting knowledge, the capability they should leave with, the format and time available, and the hardware and software already chosen. Infer reversible details and label assumptions; ask only for missing decisions that would materially change the demo.

Express the outcome as something the developer can explain or do after watching. Translate a feature list into one developer problem and one visible result. Keep the user's chosen platform unless evidence exposes a conflict; explain that conflict before proposing a replacement.

## Design the demonstration

- Build a short sequence: starting condition, developer action, visible result, and explanation. Every beat must serve the learning outcome.
- Identify the smallest implementation and the inputs it needs. Separate essential work from optional polish and state what is out of scope.
- Record the target board and revision when known, peripherals, model or runtime, network dependencies, and setup constraints. Distinguish existing equipment and verified capabilities from proposed purchases or untested compatibility.
- For each success criterion, specify an observable check and where its evidence will come from. Treat desired latency, accuracy, and power figures as targets until measured under stated conditions.
- Plan a reset and a recovery path appropriate to the format. Label prerecorded or simulated fallbacks so they cannot be mistaken for a live hardware result. Carry important limitations into the teaching narrative.
- For demos with moving hardware, include the operating boundary, supervision, and stopping procedure that must be established before testing. Planning does not authorize actuation or firmware changes.

When feasibility is uncertain, identify the smallest experiment that resolves the uncertainty before the main build. A successful desktop prototype alone does not establish on-device feasibility.

## Deliver

Write a concise brief in the user's requested location or format; otherwise return it in the conversation. Include:

- Audience, learning outcome, and developer problem.
- Demo sequence, minimal build scope, and known setup.
- Success criteria and their verification methods.
- Reset/fallback plan and unresolved feasibility questions, each with a next check.

The brief is complete when each essential demo beat has an observable result and every assumption that could invalidate the demo has a named verification step. Acknowledge unresolved facts without inventing specifications. Continue into implementation only when it is part of the user's request.
