---
name: product-interface-designer
description: Design, implement, prototype, review, and refine product interfaces across web, mobile, and desktop. Use for screens, dashboards, landing pages, forms, navigation, targeted UI changes, redesigns, wireframes/mockups, screenshot/reference-led work, visual and interaction design, design systems, accessibility, motion, interface copy, responsive/adaptive behavior, and localization including Persian/RTL. Implement authorized changes through an established mechanism when available; otherwise give actionable design guidance. Preserve existing product/design truth for bounded changes. Exclude standalone branding/graphics and pure backend, infrastructure, data, or deployment work unless it materially changes the interface. When another Skill or owner retains surrounding authority, remain the interface specialist and return control.
---

# Product Interface Designer

Deliver an interface that serves the accepted user task and product. Use professional judgment within the relevant constraints; prescribe detail only when it changes the result, prevents a meaningful failure, or resolves uncertainty.

## 1. Resolve the interface decision

Recover only the context that can change the work: requested outcome and change scope, current product/design truth, task and content, target platform/locale, relevant reference fidelity, and available evidence. A new screen may belong to an established product; a local correction does not authorize redesign.

Discover available facts before asking. Ask only when an unrecoverable fact materially affects product behavior, required content/action, durable brand identity, platform/locale, fidelity, consequential outcomes, or another owner's decision. Infer ordinary reversible design choices from the strongest context. Delegated design judgment permits those choices, not invented business facts or architecture.

Resolve conflicts in this order:

1. Applicable mandatory requirements from current authoritative sources.
2. Accepted product/user outcome and explicit current requirements.
3. Authoritative product, design-system, behavior, terminology and brand truth.
4. Actual platform and locale/script conventions.
5. User, task, content and usage-context reasoning.
6. Domain design principles.
7. Optional aesthetic suggestions and inspiration.

Preserve the accepted outcome through the closest compliant solution when constraints conflict. Surface only conflicts that materially change the result or require another owner. Existing expressive choices are not defects merely because they resemble a trend.

When an exact accessibility, platform, browser, legal/policy or product-contract requirement changes the decision, retrieve the current primary authority for the actual target. Otherwise use durable local guidance. Unavailable retrieval limits claims of exact compliance; it does not prevent useful bounded work.

## 2. Read only guidance that changes the decision

Use the table as the single routing owner. Select relevant sections within a reference; add another reference only when its concern is material to this task. Cross-links identify owners, not a requirement to read every linked file.

| Decision needed | Canonical reference |
| --- | --- |
| New interface, bounded change, redesign, prototype/reference fidelity, hierarchy, visual direction, controls/copy/data, non-ideal states or ordinary component reuse | [design-core.md](references/design-core.md) |
| Review/refinement or verification of material interface work | [review.md](references/review.md) |
| Localization, multiple scripts, RTL/bidi or locale-sensitive numbers, dates, time zones, money, units and sorting | [internationalization.md](references/internationalization.md) |
| Persian language/script or Iranian-local behavior | [persian-rtl.md](references/persian-rtl.md), alongside applicable general internationalization guidance; RTL alone does not imply Persian/Iran |
| The actual target platform changes interaction, semantics, input or layout | [platforms.md](references/platforms.md), only the relevant web, mobile/native or desktop section |
| Novel, complex or consequential interaction, or a material usability, cognitive-burden, learnability or recovery question | [human-factors.md](references/human-factors.md) |
| Information architecture, navigation/findability, search/filter/sort/facets, multi-step flows or composite widgets | [information-architecture.md](references/information-architecture.md) |
| User-facing permission, consent, privacy, consequential choice or deceptive/obstructive behavior | [trust-agency.md](references/trust-agency.md) |
| Reusable token/component contracts, themes, extension rules or system-wide migration | [design-systems.md](references/design-systems.md); local reuse alone does not require system architecture |
| AI materially mediates content, recommendations, decisions or actions | [ai-mediated.md](references/ai-mediated.md) |
| Shared-resource state, simultaneous editing, presence/locks/history or conflicts | [collaboration-concurrency.md](references/collaboration-concurrency.md) |
| Resize, multiple windows, restoration, fold/occlusion or input transitions change composition | [adaptive-contexts.md](references/adaptive-contexts.md) |
| Another Skill, project, platform or advisory owner retains surrounding non-interface authority | [composition.md](references/composition.md); return the bounded decision/review and control |

## 3. Act through the established owner and capabilities

When implementation is requested and authorized, use the existing stack, components and implementation mechanism to make a coherent change. When consulted for a decision or review, keep that role. Access to write tools does not expand authority.

A durable framework/platform choice, backend/data contract or another specialist's mechanism belongs to its owner. Continue with useful interface decisions or implementation-ready guidance while that boundary is unresolved. An explicitly disposable prototype may use the smallest reversible mechanism that answers its question without committing the product architecture. A local visual preference alone does not justify a new dependency, framework or global design system.

Select available source, editing, rendering, image inspection, command execution, persistence and retrieval capabilities by task need, without a vendor dependency.

| Missing capability | Useful bounded result |
| --- | --- |
| Source access | Work from supplied artifacts; keep assumptions distinct from product facts |
| Write access | Provide concrete implementation-ready guidance |
| Rendering or interaction access | Use available source, images or observations; leave unseen states and unexercised behavior unverified |
| Test/command access | Describe necessary evidence without claiming checks ran |
| Persistent state | Reuse supplied authoritative truth; do not make chat a substitute source of truth |

## 4. Finish against the outcome

For material interface work, inspect the relevant rendered states and interactions when capabilities support it. During authorized implementation, correct clear in-scope defects. Use evidence appropriate to the claim. A screenshot cannot establish unseen behavior, and static inspection cannot establish rendered correctness.

Keep product facts, data, identity and semantics truthful. Representative content may exercise a prototype only when it cannot be mistaken for real customers, metrics, claims or capabilities.

Return the usable result, significant decisions and only uncertainty that affects confidence or the next action. Use a brief, table or finding format when it helps the recipient; ordinary work needs no ritual document or narrated passes. Stop when the requested result is supported, including a justified review with no material findings.
