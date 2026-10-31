# Human Factors and Usability Evidence

Use this depth for a material question about understanding, learning, memory, error or task completion. Familiar, reversible, low-consequence interactions can use ordinary design and review. Novel models, compounded repeated friction, interruption, stress or costly mistakes warrant closer scrutiny.

## Contents

[Mental model](#predictability-and-task-context) · [Recovery/help](#control-recovery-and-help) · [Evidence](#usability-evidence) · [Fidelity](#prototype-fidelity) · [Uncertainty](#proportional-uncertainty)

## Predictability and task context

Use domain language and mappings users can predict, with consistent concepts and visible cause/effect. Preserve useful transfer from established patterns. A backend model is not automatically the user's mental model; introduce unfamiliar concepts progressively. Controls that look alike should not conceal materially different behavior.

Prefer recognition to recall. Keep choices, constraints, prior selections and comparison information available where decisions depend on them. Preserve valid work and orientation across errors, navigation or interruption when product rules allow. Chunk work only when it helps the task; hiding essential context or adding steps can increase burden despite a cleaner screen.

Defaults, recent values, autofill and suggestions help when trustworthy and controllable. After state changes, make the current status and next meaningful action understandable without reconstructing the whole history. Evaluate completion, failure and resumption, not just the appearance of one screen.

## Control, recovery and help

Make action effects stable and explainable. Prevent avoidable errors through appropriate constraints and sequencing, then preserve valid work and expose useful cancel, edit, back, retry or undo paths when the product supports them. Consequential actions need understandable scope and an appropriate commitment/recovery model, not confirmation for every action.

Place help where it changes the next action; keep recurring help discoverable. Reveal advanced detail without hiding required information or making the capability undiscoverable when needed. Explain a genuinely new control near first use, but prefer an established one when novelty adds no value. Tours should not compensate for unclear everyday controls or repeatedly obstruct experienced users.

## Usability evidence

[review.md](review.md) owns static, rendered, measured and assistive review evidence. For usability claims, retain these distinctions:

| Evidence | Confidence boundary |
| --- | --- |
| Product facts and reasoned design hypothesis | Establish context or a prediction, not observed task success |
| Rendered/interaction or measured accessibility evidence | Establish the exercised behavior/properties, not representative users' understanding |
| Funnels, errors, support reports or abandonment | Reveal observed behavior/problems, not necessarily their cause |
| Actual user/task observations | Support conclusions about the tested participants, tasks and context, not untested populations or universal usability |

A novel interaction remains a hypothesis without relevant evidence. Preference polling does not substitute for task observation when completion is the question; visual polish does not establish usability.

## Prototype fidelity

Use the smallest fidelity that makes the actual uncertainty observable.

| Question | Needed fidelity |
| --- | --- |
| Structure, sequencing, labels or broad task flow | Rough wireflow or minimally interactive prototype may suffice |
| Hierarchy, density, typography, wrapping, brand or reference fidelity | Enough visual/content fidelity to judge those properties |
| Timing, focus/keyboard, motion, adaptive transitions, device/input or assistive behavior | Functional/platform fidelity sufficient to exercise the behavior |

Add realistic content and state complexity when it can change the answer. More polish is not stronger evidence by itself; a static mock cannot establish an interaction.

## Proportional uncertainty

Identify the decision-sensitive assumption. Use stronger evidence when it could materially change that decision, choosing the cheapest credible source: existing product behavior, support/analytics, a prototype/task observation or suitable research. This does not make research a prerequisite for ordinary work.

When direct user evidence is unavailable, continue with familiar, reversible, clearly signposted interaction and lower error cost where compatible with the outcome. State only the material assumption and the specific task/question future evidence should resolve. Return an unresolved choice to its owner only when it changes accepted product behavior, material risk or that owner's boundary.
