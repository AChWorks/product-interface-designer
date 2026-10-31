# Interface Review

Review the parts that can change the conclusion. This reference owns evidence, visual/interaction QA, accessibility, motion and obvious interface-performance risks; its sections are selectable concerns, not ordered passes.

## Contents

[Scope and judgment](#scope-and-judgment) · [Evidence](#match-evidence-to-the-claim) · [Rendered behavior](#implementation-and-rendered-behavior) · [Accessibility](#accessibility-and-interaction) · [Motion/performance](#motion-loading-and-performance) · [Diagnosis](#connect-observation-correction-and-evidence) · [Completion](#correct-and-report)

## Scope and judgment

| Change | Sufficient review scope |
| --- | --- |
| Local correction | Changed control/surface and affected states |
| Material surface change | Representative content, sizes, interactions and accessibility concerns |
| Shared system or redesign | Representative surfaces, shared patterns and cross-surface effects |

Judge against the accepted outcome, product/design truth, actual platform/locale and change scope. Separate a **defect** that contradicts these requirements or breaks use, a **risk** that needs stronger evidence, and a **subjective alternative** that is another defensible choice. A preferred style is not evidence that intentional product character is wrong.

## Match evidence to the claim

| Evidence | What it can establish |
| --- | --- |
| Authoritative requirements, tokens, components and behavior | The intended result and constraints |
| Source, styles, structure, state logic and fixtures | Implementation facts and likely failure points |
| Running UI, screenshots and exercised interactions | Observed layout or behavior at those states and sizes |
| Measurement, accessibility tools and actual assistive/input exercise | Findings within the method and coverage used |
| Actual user/task evidence | Usability observations within the tested users, tasks and context |

These evidence types answer different questions. A screenshot cannot prove unseen interactions; source cannot prove rendered typography or overflow. Automated accessibility checks do not establish full accessibility, and a working render does not establish usability. [human-factors.md](human-factors.md) owns deeper task evidence when material.

Use representative content and supported sizes. When exact coverage is unknown, choose compositions that expose likely changes without calling them exhaustive certification. Missing capability narrows the conclusion rather than stopping useful review.

## Implementation and rendered behavior

Static inspection can reveal unreachable conditional states, inappropriate semantics, fragile fixed dimensions, inconsistent shared patterns or missing async/recovery handling. A fixed size or absolute position is a risk only when it conflicts with the actual content or behavior; confirm rendering-dependent conclusions when possible.

In the running result, inspect what the change can affect:

- **Hierarchy and density:** the intended task is visible; grouping, action priority and spacing support it; decorative containers do not obscure structure.
- **Typography and visual states:** real fonts/weights load, fallback and mixed scripts remain usable, labels and wrapping fit actual content, and focus/selection/status remain distinct in supported themes.
- **Layout and reflow:** long content, localization, zoom/text scaling and narrow/wide compositions do not lose required information or operation. Check relevant navigation changes, scrolling, overlay bounds, cropping and sticky/fixed content that can obscure focus.
- **State continuity:** loading, empty/partial data, failure/retry, access limits, unavailable actions, success, unsaved work and destructive recovery behave as the product promises. Async refresh or hydration must not erase input or orientation.

Test affected size/orientation/input transitions where the product supports them. Recomposition can change navigation, content order and data presentation; device labels alone do not define the behavior. Locale, platform and adaptive details remain with their respective owners.

## Accessibility and interaction

Use the applicable target-platform accessibility model and current authority for exact requirements. Focus the review on relevant perception, operation and semantics: contrast and non-color meaning, media alternatives, text reflow, meaningful names/roles/states, logical focus order, visible unobscured focus, usable targets, associated errors and exposed status updates.

Exercise required actions with the actual keyboard, touch or assistive paths available. Essential information must not depend on hover alone. Gesture/drag-only operations need an alternative unless the gesture is genuinely essential. Dialogs, sheets and overlays must handle focus entry, containment and restoration appropriately for their platform without trapping users behind visual layers.

Check the interaction states that exist on the target: focus, hover, pressed, selected, unavailable, in-flight, success, failure and recovery. Look for dead clickable areas, changed action meaning during loading, or disabled actions whose material reason/recovery cannot be found. Do not infer these behaviors from appearance alone.

## Motion, loading and performance

Motion should explain cause/effect, preserve orientation, confirm state or serve intentional product character. Keep frequent interactions calm enough for repeated use; rare meaningful moments may support more expression. Reuse recognizable motion for the same meaning, with movement connected to the control/state users track.

Verify immediacy for direct manipulation, appropriate timing/easing, understandable choreography and interruption by new input. Respect reduced-motion preferences and applicable pause/stop requirements. Avoid rigid external timing presets and nonessential autoplay that competes with the task.

Fast operations should not flicker; slow operations should show real progress without invented certainty. Preserve action context and user input, reserve space to limit layout shift, keep recovery available, and avoid blocking the whole interface for a local busy region.

Flag evident UI cost such as oversized media, excessive font/asset loading, unbounded large lists, repeated layout measurement, expensive animation or gratuitous dependencies. Prefer efficient transformations where practical, but use measurement for quantitative performance claims. Backend/system performance remains with its owner.

## Connect observation, correction and evidence

Diagnose a concrete failure and choose the smallest correction that serves the task. Examples clarify that relationship; they are neither a required output table nor universal style rules.

| Observation | Decision | Evidence that matters |
| --- | --- | --- |
| Long translated labels overlap an action at a supported narrow width | Let content grow or recompose the affected control group; preserve meaningful labels | Render relevant long content at that width and with supported text scaling |
| Routine and destructive actions compete equally in a dense work queue | Set prominence from the actual task and consequence; keep genuinely co-equal choices when appropriate | Inspect the rendered hierarchy and exercise the affected action/state paths |
| An approved expressive brand remains legible and supports the task | Preserve it; resemblance to a trend is not a defect | Authoritative design intent and the relevant rendered result |

A visual correction cannot resolve unknown product behavior. Return that material decision to its owner instead of designing around an invented rule.

## Correct and report

During authorized implementation, correct clear in-scope defects before completion. A consulted reviewer returns findings and control; write capability alone does not authorize fixes. Stop when the requested quality bar is supported, without expanding into unrelated redesign or manufacturing findings.

Prioritize user harm or blocked tasks, accessibility/interaction failures, broken layout/state behavior, contradictions with product truth, then material polish. Keep subjective alternatives distinct.

A useful finding connects the affected surface, observation, user consequence, smallest justified correction and supporting evidence. Mention missing authority or evidence only when it changes confidence or the next action. A supported review with no material findings is valid.
