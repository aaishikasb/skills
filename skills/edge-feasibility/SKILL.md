---
name: edge-feasibility
description: Assess whether an AI use case can run on a target device within latency, memory, power, quality, and connectivity constraints. Use before committing to an edge deployment or choosing between candidate configurations.
license: MIT
---

# Edge feasibility

Produce a conditional go/no-go decision and the smallest experiment needed to resolve the decisive uncertainty.

## Define the operating envelope

Read the use case and available device/model evidence. Identify the task-quality threshold, input rate/shape, latency boundary and percentile, memory limit, power source, duty cycle, connectivity, deployment environment, and budget. Include only constraints that matter to this decision. Preserve the user's hardware choice unless a documented constraint rules it out.

Separate requirements, vendor specifications, measured results, estimates, and unknowns. Verify implementation-specific support against authoritative documentation for the exact device, runtime, model operators, and versions. A supported model format alone does not establish accelerator coverage; fallback operators may change feasibility.

## Account for the whole path

- Trace capture → preprocessing → transfers → inference → postprocessing → output or control. Align timings with the requested end-to-end boundary. Explain concurrency and queueing assumptions rather than summing or inverting unrelated numbers.
- Budget memory for weights, activations, runtime/workspace, input buffers, and the host system where they share a limit. A model fitting on disk does not prove it fits at runtime. Keep arithmetic units explicit.
- Evaluate task quality on representative inputs separately from throughput. Compression or reduced precision is a candidate to measure, not a guaranteed free improvement.
- Check startup/download requirements, warm operation, thermal behavior, power mode, and update/rollback needs when relevant. A short warm inference run does not establish sustained offline or battery operation.

Reject only what the evidence rules out. A violated hard bound can establish infeasibility under stated assumptions; absent measurements normally justify a provisional decision, not a confident no. Avoid shopping lists when a single targeted test can decide the current option.

## Design the deciding experiment

Specify target configuration, representative input, measurement boundary, warmup and observation duration appropriate to the claim, required telemetry, and predeclared pass/fail thresholds. Choose the experiment that could change the decision soonest. State what remains untested even if it passes.

For robotics, separate advisory inference from the validated control and stopping mechanisms. A feasibility estimate does not authorize deployment or movement.

## Deliver

Provide a constraint/evidence/status table, checked calculations, a decision of feasible within tested conditions, infeasible under stated bounds, or unresolved, and the next experiment. Keep estimates visibly labeled and preserve uncertainty in recommendations. Do not invent benchmarks or certify real-time guarantees from average latency.
