---
name: developer-friction
description: Evaluate a quickstart, onboarding guide, or sample repository from a new developer's perspective. Use to find first-run blockers, hidden prerequisites, unclear success signals, and concrete documentation fixes.
license: MIT
---

# Developer friction

Follow the advertised path to the first useful result with the knowledge and environment of the intended newcomer.

## Establish the starting point

Read the entry page and promised outcome before exploring implementation details. Identify the intended audience, starting environment, and definition of first success. Respect stated prerequisites; a skill the guide explicitly requires is not automatically an onboarding defect.

Use the guide's order and record what a newcomer knows at each step. Inspect repository internals to diagnose a blocker, but count information found only there as a gap if the guide depends on it. Avoid silently using cached credentials, preinstalled packages, hidden environment variables, or prior project knowledge to make the path pass.

## Walk the path

Use a disposable environment when available. Execute safe, in-scope setup and software checks when practical; inspect before running commands that install globally, consume credits, delete data, flash devices, or actuate hardware. Existing authorization still applies. When a step cannot be executed, record the reason and continue with a clearly labeled source walkthrough.

Capture the entry step, expectation, actual observation, and evidence for each point of friction. Distinguish **observed failure**, **source-confirmed gap**, and **untested concern**. An unavailable device or account is a verification limit, not proof that the guide fails.

Look for gaps that change the developer's ability to proceed:

- Unstated dependencies, incompatible versions, working directories, permissions, hardware variants, accounts, and model/data downloads.
- Credentials and configuration placeholders with no acquisition path; successful behavior that depends on cached state.
- Commands or links that contradict the actual project, and branching instructions that fail to say which path applies.
- Missing success signals, confusing intermediate output, or errors without a recovery step.
- Concepts introduced after the reader must already use them, including pin conventions, device selection, or local-versus-target execution.

## Deliver

Lead with whether the advertised first result was reached and the verification environment. List findings in path order, with severity based on impact: **blocker** prevents progress, **detour** requires avoidable discovery, **clarity** increases uncertainty without preventing progress.

For each finding give a file/section or command, evidence, newcomer impact, and the smallest proposed fix. Separate environment limits from guide defects. Offer concrete replacement text where useful; apply fixes only if requested. Avoid rewriting working sections for stylistic preference.

The review is complete when the first-result path and relevant recovery steps have been walked or explicitly marked untested. Report measured time-to-first-result only for an actual run, including setup conditions; a source review cannot supply that metric or certify user success.
