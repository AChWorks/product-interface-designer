# Core Interface Design

Use the relevant sections for product-interface decisions. Change scope and authority come from SKILL.md; platform, locale and verification detail remain with their dedicated owners.

## Contents

[Scope](#change-scope) · [Direction](#product-direction) · [Fidelity](#reference-fidelity) · [Hierarchy/layout](#hierarchy-and-layout) · [Typography/visual roles](#typography-and-visual-roles) · [Controls/copy](#controls-and-interface-copy) · [Data](#data-presentation) · [Feedback/states](#feedback-and-non-ideal-states) · [Reuse/refinement](#reuse-and-refinement)

## Change scope

| Accepted work | Design decision |
| --- | --- |
| New interface or surface | Derive direction from the product, task and content. A new surface can still belong to an established product; recover its design truth first. Establish only enough shared visual language for coherence. |
| Targeted modification | Preserve incumbent tokens, type, components, information architecture, interaction vocabulary and terminology except where the accepted change requires adjustment. Make the smallest coherent change. |
| Redesign | Deliberately reconsider composition, type, color, density, imagery, component expression and motion. Retain product capabilities, content semantics, validated terminology, business rules, integrations and mandatory constraints unless their authoritative owner changes them. Recoloring the old layout may not solve the accepted problem. |

## Product direction

Let the user task, content, usage frequency, consequence of mistakes, available brand evidence and actual input context determine the design. An operations screen may need stable comparison and low interruption; an introduction surface may give imagery and sequencing more room. These are task priorities, not fixed page genres.

Use the product's own language, materials, data and imagery to establish character. Prefer real content when available; clearly representative content can expose wrapping, density and state problems during exploration. A short direction is useful when several decisions need a shared rationale, not as a compulsory preliminary document.

Density, distinctiveness, contrast, ornament and motion are independent choices. A dense interface can be distinctive; expressive typography does not require animated decoration. Common conventions remain valuable when they support the task.

For a strong visual device, identify what product meaning, hierarchy, state, interaction or intentional character it contributes. If it could move unchanged to an unrelated product, reconsider whether it is doing useful work. Keep established expression and familiar conventions when justified; do not manufacture novelty or remove an intentional identity cue merely because it is common elsewhere.

## Reference fidelity

| Role of the reference | What to carry into the result |
| --- | --- |
| Close or high-fidelity implementation | Treat observable geometry, hierarchy, density, type character, color relationships and interaction cues as accepted requirements, subject to stronger product or mandatory constraints. Verify material fidelity against rendered evidence when available. |
| Inspiration | Extract useful rhythm, hierarchy, character, imagery treatment or interaction principles, then adapt them to the actual product. |
| Partial visual evidence | Use only what it shows. A screenshot does not establish hidden behavior, data rules, responsive states, factual claims or platform semantics. |

Preserve authoritative product content, terminology and identity when the reference contains unrelated placeholders. [review.md](review.md) owns evidence appropriate to fidelity claims.

## Hierarchy and layout

Make the intended reading and action order apparent through information order, grouping, alignment, type, spacing and emphasis. Containers, cards, borders, labels and badges should express grouping, state, sequence or affordance. Equal visual weight implies equal importance; repeated cards are useful only when that relationship is real.

When a surface is confusing, first remove competing actions, redundant labels or weak grouping. Keep one dominant action in a decision area unless the task has genuinely co-equal outcomes. Adding another border or heading will not repair an unclear decision model.

Choose composition and density from the content and task. Keep actions near the information that justifies them, preserve readable line widths, and use repetition to establish rhythm with meaningful exceptions. Empty space can serve composition; it should not hide a weak information structure. Exercise short, typical and long content rather than protecting one ideal string.

Secondary complexity can be disclosed when needed. In-context interaction usually preserves orientation better than interruption, but the significance of a decision governs the final choice. Responsive composition may reorder or transform content; it is not merely a scaled-down desktop layout.

## Typography and visual roles

Use incumbent typefaces for bounded changes. For new work, choose for content, script coverage, intended character, platform and delivery cost; verify availability, licensing and the actual weights/scripts that can ship. Keep an intentional scale and weight range, with readable body text and clear labels at the real density. Additional families or display treatments need a useful role. Script shaping, bidi and locale-specific typography belong to the relevant locale guidance.

Build color from semantic roles: surface, text, action, focus/selection, status and data. Reuse project tokens; place accents where attention or identity is earned. Essential meaning needs a channel beyond color. Themes need deliberate role relationships, not mechanical inversion.

Shape, border, shadow, blur and elevation should make relationships understandable. Coherence does not require applying the same treatment to every object; nested shapes should be optically related. Use a coherent icon language to clarify actions and categories, with directional meaning appropriate to the actual interface. Imagery should explain, orient, demonstrate or express the product, with deliberate cropping, aspect ratio and treatment.

## Controls and interface copy

Controls should expose what will happen and the state needed to decide. Use specific action or destination labels and consistent vocabulary across the action, progress, success and failure. Give prominence according to actual priority and consequence.

Group form fields by the user's task rather than the backend schema. Use persistent meaningful labels, explain requirements where they matter, preserve recoverable input and make irreversible outcomes explicit. Do not collect data before the product needs it. Navigation should make location, destination and return predictable; additional navigation levels need an information-architecture reason.

Write in the user's domain language while preserving authoritative technical terms and identifiers where simplification would lose accuracy. Put decision-relevant information first. If lengthy instructions mainly explain ordinary controls, simplify the interaction before adding prose. Error, empty, blocked and permission states should offer the next useful step when one exists, without blame. Keep guidance beside its decision and use calm, unambiguous language where consequence or stress matters.

Write complete localizable messages with variables/counts separate from sentence structure; allow reordering and expansion instead of assembling fragments or abbreviating to protect a brittle layout. Locale-specific wording belongs to the locale owner.

## Data presentation

Choose the representation from the question the data answers.

| Question | Useful representation |
| --- | --- |
| Exact values, aligned comparison, dense scanning or sorting | Table; also useful as an accessible equivalent |
| Repeated entities with a dominant reading order | List |
| Compare discrete magnitudes | Bars |
| Change over time | Lines |
| Spread and outliers | Distribution plot |
| Relationships between continuous variables | Scatter-style view |
| Rough share of a whole with few categories | Part-to-whole chart; use bars/table for precise comparison |

Maps, funnels, networks, gauges and similar specialized forms need a matching data structure or task. Provide direct labels, a table or a meaningful summary when exact interpretation or non-visual access requires it. Avoid ornamental charts or motion that makes comparison harder.

## Feedback and non-ideal states

Choose feedback by significance, persistence, scope, actionability and interruption cost.

| User need | Appropriate starting point |
| --- | --- |
| Understand or repair a local condition | Feedback beside the affected object/control |
| Notice a routine confirmation that can safely disappear | Transient feedback |
| Understand an ongoing condition affecting current work | Persistent surface-level message |
| Make an immediate decision whose consequence warrants blocking context | Alert or modal-style decision |
| Receive timely, useful information while away from the product | System notification, subject to target-platform behavior and permission |

Do not bury a material failure or recovery action in a disappearing message, or turn routine success into repeated interruption. Exact delivery behavior belongs to the platform; consequential choice and consent belong to [trust-agency.md](trust-agency.md).

Cover the states the flow actually supports: loading/progressive arrival, empty or partial data, overflow, validation/failure/retry, access limits, offline work, unsaved changes, unavailable actions, success and destructive recovery. Explain what happened and the next possible action without inventing backend behavior, permissions or undo.

For first use, get users to a meaningful action and teach features where they become useful. Empty states or working examples may orient better than a tour. Let experienced users skip education unless a real setup or safety requirement prevents it; do not force an educational sequence before ordinary access.

## Reuse and refinement

Reuse authoritative tokens, components and patterns; make only the coherent extension the current task needs. Keep local exceptions local. A new taxonomy, component library or governance process is justified by continuing reuse, not by a single surface needing consistency. [design-systems.md](design-systems.md) owns system-level contracts and migration.

Refine against the product task: clear hierarchy, coherent expression, realistic content/states and the accepted scope. Remove unhelpful competition before adding detail. A generic component pattern should not substitute for information architecture, and a local correction should not redesign neighboring surfaces. When the requested result is supported, further novelty or visible change is unnecessary.
