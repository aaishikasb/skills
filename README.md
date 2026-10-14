# Skills for everyday DevRel

Agent skills for the work between a product and the developers trying to use it: quickstarts, technical articles, tutorials, workshops, talks, and community feedback.

These thirteen skills give your agent a specific job and a concrete deliverable: fixes to a quickstart, an article brief, a tutorial draft, or issues backed by developer reports.

*The collection also includes specialist tools for edge AI, hardware, and robotics.*

## Try it on your quickstart

Start with `developer-friction`. It reviews your onboarding path from a new developer's starting point.

```sh
npx skills add aaishikasb/skills --skill developer-friction
```

Choose your agent in the installer, open the project you want reviewed, and ask:

> Use developer-friction to review this quickstart for a developer using our SDK for the first time. Follow the documented setup through the first useful result. Find hidden prerequisites, missing success signals, and steps that require insider knowledge. Give me the smallest fixes, with file and section references.

You get findings tied to the developer's path: what blocks progress, what causes a detour, and what needs a clearer explanation. The review distinguishes steps it ran from gaps found by reading the source.

## What these skills help you ship

### What comes next

For the itch to keep improving after a milestone. Look across the project, its audience, and the work around it to find the next worthwhile investment.

| Skill                                  | When to use it                                                              | What you get                                                                                                                          |
| -------------------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| [what-else](skills/what-else/SKILL.md) | You've built or shipped something and want to know what else is worth doing | A cross-domain table of next moves, impact, urgency, need, priority, and bandwidth—with evidence, a recommendation, and what can wait |

### Content and feedback

Use these when deciding what to write, improving onboarding, or bringing developer evidence back to the product team.

| Skill                                                        | When to use it                                                           | What you get                                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| [developer-friction](skills/developer-friction/SKILL.md)     | A quickstart or sample needs a fresh pair of eyes                        | Prioritized onboarding problems with evidence and concrete fixes                          |
| [content-angle](skills/content-angle/SKILL.md)               | You have release notes, a project, or recurring questions to write about | A reader problem, defensible article premise, title, and outline                          |
| [developer-feedback](skills/developer-feedback/SKILL.md)     | Support threads, community comments, and event notes are piling up       | Themes that separate independent incidents from reposts, plus actionable issue drafts     |
| [tutorial-maintenance](skills/tutorial-maintenance/SKILL.md) | An SDK release or API change has made an existing guide drift            | Version-specific corrections across commands, expected output, links, and troubleshooting |

### Demos and teaching

Use these to turn technical work into an explanation, a reproducible example, or a session with a clear learning outcome. The demo and workshop skills include detailed checks for device-based projects.

| Skill                                                | When to use it                                              | What you get                                                                                       |
| ---------------------------------------------------- | ----------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| [demo-to-tutorial](skills/demo-to-tutorial/SKILL.md) | A working sample needs to become a tutorial                 | A draft grounded in the implementation, with setup, checkpoints, explanations, and troubleshooting |
| [explain-concept](skills/explain-concept/SKILL.md)   | A technical idea keeps confusing your audience              | A precise mental model, worked example, and a question that checks understanding                   |
| [talk-builder](skills/talk-builder/SKILL.md)         | A conference proposal or technical talk needs a clear story | A focused proposal or timed narrative, with demo cues and a recovery plan                          |
| [workshop-builder](skills/workshop-builder/SKILL.md) | A working project needs hands-on exercises                  | A timed agenda, learner checkpoints, instructor notes, and recovery paths                          |
| [demo-brief](skills/demo-brief/SKILL.md)             | An edge AI or hardware demo is still an idea                | A teaching goal, minimal build scope, setup constraints, and observable success criteria           |
| [demo-proof](skills/demo-proof/SKILL.md)             | A device demo or its performance claims need review         | An evidence assessment, reproduction blockers, and prioritized fixes                               |

### Edge AI and hardware

For work where device limits, physical setup, and measured behavior affect the outcome.

| Skill                                                | When to use it                                             | What you get                                                                            |
| ---------------------------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| [edge-feasibility](skills/edge-feasibility/SKILL.md) | You need to decide whether a use case fits a target device | A constraint budget, conditional go/no-go decision, and the experiment needed to decide |
| [hardware-triage](skills/hardware-triage/SKILL.md)   | A device, sensor, or robotics setup behaves inconsistently | Ranked possible causes and a check that distinguishes them                              |

## Put them to work this week

**Decide what deserves your next afternoon.** Give `what-else` the project, its intended outcome, feedback, and the time you have:

> Use what-else to review this SDK demo and tutorial. I have six hours before the launch. Look across the developer experience, teaching, distribution, and maintenance. Show impact, urgency, need, priority, and bandwidth in a table. Recommend what fits, what can wait, and one promising stretch idea if the evidence supports it.

It can recommend a clearer example, a distribution experiment, or removing unnecessary work. It checks whether additions serve your goal and makes room for ambitious ideas without treating every possibility as a requirement.

**Turn a sample repo into a tutorial.** Use `demo-to-tutorial` to draft the guide from its implementation and run notes. Then use `developer-friction` to review the path a newcomer will follow. When the SDK changes, use `tutorial-maintenance` to check what needs updating.

**Turn recurring questions into useful content.** Give `developer-feedback` the relevant threads to identify the underlying problem. Pass those findings to `content-angle` to scope an article that addresses it.

**Prepare a talk from a project you've built.** Give `talk-builder` your project notes, audience, slot length, and submission requirements:

> Use talk-builder to turn this SDK integration into a 20-minute talk for backend developers, including 3 minutes of Q&A. Build it around one useful takeaway. Include a fallback if the live service is unavailable.

Each skill works independently. Pass the source material and findings between tasks when you want to combine them.

## Install more skills

The [skills CLI](https://www.skills.sh/docs/cli) lets you browse the collection and choose what to install:

```sh
npx skills add aaishikasb/skills --list
npx skills add aaishikasb/skills
```

Use `--agent codex` or `--agent claude-code` to select an agent directly. Add `--global` for a user-wide installation. To install all thirteen for Codex in the current project:

```sh
npx skills add aaishikasb/skills --skill '*' --agent codex
```

The CLI requires Node.js 22.20+ with npm. For a local checkout before publication, replace `aaishikasb/skills` with `.` and run from this repository.

The skills follow the [Agent Skills format](https://agentskills.io/specification). Each folder can also be copied into your agent's skills directory, including its license, metadata, and references. They need no separate service or API key to load; provide the project files and access needed for the task you ask them to do.

## Contributing

Keep each skill focused on one decision or deliverable. Include a realistic example when proposing a change, keep install names stable, and update the catalog and [skills.sh grouping](skills.sh.json) when adding a skill.

## License

[MIT](LICENSE). Each skill includes its own copy of the license notice.
