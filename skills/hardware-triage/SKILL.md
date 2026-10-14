---
name: hardware-triage
description: Diagnose unreliable edge-AI devices, sensors, and robotics setups from symptoms, logs, wiring references, and configuration. Use to rank plausible causes and choose the next discriminating experiment.
license: MIT
---

# Hardware triage

Reduce uncertainty about a hardware-related failure with the smallest safe experiment that can distinguish likely causes.

## Establish the failure

Read the supplied logs, code, configuration, and hardware notes. Capture expected versus observed behavior, a minimal reproduction, device and board revision, power source, connected peripherals, firmware/OS/runtime/model versions, and the last known good state. Separate observed facts from the user's interpretation. Ask only for missing facts that affect the next decision.

Preserve logs and configuration before changes. Locate the failure relative to power-up, enumeration, data capture, inference, communication, and actuation; investigate the layers implicated by evidence rather than requiring a universal checklist.

## Rank hypotheses

Use timing, error messages, recent changes, and known-good comparisons to propose a short ranked list. For each hypothesis give supporting evidence, conflicting evidence, and a check that would distinguish it from alternatives. Use qualitative confidence tied to evidence rather than invented probabilities.

A correlation is a lead, not a diagnosis. For example, a device disconnect during motor startup could implicate power or interference, but logs alone may not distinguish them. An inference failure can also originate upstream in capture or preprocessing. Prefer read-only inspection and existing logs before interventions.

For pin assignments, voltage compatibility, firmware behavior, or device-specific procedures, consult authoritative documentation for the exact model and revision. If the mapping is unresolved, request the identifier or document; do not invent a pinout or substitute a similar board's electrical limits.

## Choose the next experiment

Specify one useful next experiment, with prerequisites, the variable being changed, observations to capture, expected outcomes for competing hypotheses, and how each result changes the next step. Keep the original condition as a baseline and include rollback where applicable. Separate a proposed experiment from one actually performed.

Honor existing authorization, but diagnosis alone does not authorize flashing, erasing storage, changing voltage or wiring, bypassing interlocks, or starting moving hardware. Before such an intervention, establish device-specific limits, a safe operating state, and explicit authorization for the action if it is not already covered. When those prerequisites are absent, continue noninvasive analysis and identify exactly what is needed.

Pause physical testing if evidence indicates overheating, damaged power hardware, unexpected motion, or an unknown electrical boundary. Preserve the safe state and refer hands-on work to a qualified operator when the situation requires it. Do not prescribe live wiring changes or guessed electrical settings.

## Deliver and close

Report the observed failure, ranked hypotheses, and next experiment with its decision branches. If the device is unavailable, provide this diagnostic plan and state the verification limit; do not claim a cause or fix was confirmed.

After an authorized fix, repeat the original failure trigger under the relevant conditions and check affected functionality. Report the actual observation period and remaining limits. Close as resolved only with confirming evidence; otherwise keep the diagnosis provisional and name the next useful observation. Avoid stacking changes that make the result impossible to attribute.
