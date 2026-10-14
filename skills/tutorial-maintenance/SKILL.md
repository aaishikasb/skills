---
name: tutorial-maintenance
description: Audit or update a published tutorial against its intended code, dependency, and hardware versions. Use when instructions drift, APIs change, links break, or a tutorial needs a verified refresh.
license: MIT
---

# Tutorial maintenance

Keep a tutorial's promised outcome reproducible while preserving its intended version and teaching path.

## Establish the version contract

Read the tutorial, linked code, dependency locks, setup requirements, prior verification notes, and the user's requested target. Decide whether the work is a repair for the existing supported version or an explicitly requested migration. A newer release alone is not a defect. Preserve the old path if it is still supported and within scope.

Inspect each affected command, API, file path, configuration value, expected result, and hardware assumption against the authoritative source for that version. Follow redirects to see whether the destination still answers the reader's question; an HTTP success alone does not establish a useful link. Record unreachable sources as unverified.

## Identify material drift

Separate broken steps, unsupported claims, changed defaults, stale screenshots, and harmless cosmetic differences. Trace each proposed correction to a source or observed failure. Follow changes through prerequisites, snippets, expected output, troubleshooting, reset/cleanup, and any companion sample; a renamed flag may invalidate several sections.

Keep simulation and target-device verification separate. Hardware revision changes need exact compatibility and wiring evidence. Preserve credentials and user data while testing; avoid exposing values in excerpts or rerunning destructive setup steps merely to check the prose.

## Repair and verify

For an audit, propose the smallest patch without editing. When updates are requested, apply the patch to the authorized files and reuse the project's checks. Prefer a clean environment matching the tutorial to one with hidden cached assets. Re-run the affected reproduction path when feasible and authorized, including a relevant error/recovery step. If execution is unavailable, finish source-backed edits and label the remaining run explicitly.

If a requested migration changes the learning path or removes a capability, explain that effect and preserve a recoverable copy or diff. Do not silently update every dependency or rewrite unrelated sections.

## Deliver

Report each material drift with tutorial location, source version/evidence, proposed or applied correction, and verification status. Distinguish source-inspected, command-tested, and hardware-tested changes. Date the checks actually performed; a newly edited page is not automatically newly tested.

The repair is complete when affected instructions and their dependent explanations agree with the intended version, and executed checks or remaining limits are recorded. Publication and deprecation of old versions require their own user authorization.
