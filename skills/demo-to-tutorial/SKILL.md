---
name: demo-to-tutorial
description: Turn an existing demo, repository, and run notes into a developer tutorial. Use when teaching a real implementation with reproducible steps, explanations, expected observations, and troubleshooting.
license: MIT
---

# Demo to tutorial

Teach a developer to reproduce an existing implementation and understand its important decisions.

## Read the implementation

Inspect the entrypoints, configuration, dependency declarations, setup notes, and recorded results before drafting. Establish the audience and learning outcome from the request or existing brief. Ask about missing audience or scope only when it changes the teaching approach.

Identify the tested target, code version, hardware/peripherals, model, software versions, and evidence of a successful run. Attribute supplied results. Separate executed steps from instructions inferred from source, and from steps awaiting verification. An absent run record permits an explicitly unverified draft, not an invented success story.

Use a supplied review or brief if available; neither is a required dependency. Preserve unresolved findings that affect the tutorial. Resolve version-sensitive facts from the project's pinned sources or authoritative documentation rather than substituting the latest API automatically.

## Build the learning path

Open with what the reader will build and learn. State required prior knowledge, equipment, environment, accounts, downloads, and meaningful time or cost constraints when known.

Order the tutorial along an executable path: prepare → install/configure → run → inspect the result → understand the key decision → reset or clean up. Adapt the shape to the task rather than adding empty sections.

- Give each command its working directory and required environment. Derive paths, flags, and imports from the implementation. Make placeholders unmistakable and explain how to obtain their values; keep secrets out of examples and output.
- Explain a choice immediately before it matters. Focus on the parts readers would otherwise cargo-cult; link to maintained source for large code sections instead of duplicating the entire project.
- Pair major steps with an observable checkpoint. Quote actual output only with its provenance; label illustrative output as illustrative and distinguish it from measured results.
- Preserve the boundary between simulation, desktop execution, and target-device execution. Carry performance conditions and limitations alongside the relevant claim.
- For wiring or physical setup, require an authoritative reference for the exact revision. Keep unresolved connections explicit. Include established operating limits and stopping steps for moving hardware; writing the tutorial does not authorize testing them.
- Derive troubleshooting from observed failures or clearly labeled likely causes. Tie each symptom to a discriminating check and recovery action. Include cleanup for resources the tutorial creates, with data-preserving instructions.

## Deliver and check

Write the requested artifact, preserving an existing publication's voice and structure when supplied. Trace its instructions against source files and safe checks available within the authorized environment. State which checks were executed and which were only inspected.

Include a short verification note and any remaining publication blockers. The tutorial is ready to reproduce only when the essential path is backed by a run in the stated environment; otherwise identify the missing run or step prominently as draft status. Do not claim learning effectiveness from prose review alone. Publication is a separate action unless explicitly requested.
