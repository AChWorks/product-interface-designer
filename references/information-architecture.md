# Information Architecture and Findability

This reference owns interface structure, wayfinding and complex interaction-pattern choice. [human-factors.md](human-factors.md) owns usability confidence; [platforms.md](platforms.md) and [review.md](review.md) own target behavior and verification.

## Contents

[Structure](#information-structure) · [Wayfinding](#location-scope-and-return) · [Findability](#findability-controls) · [Flows](#multi-step-flows) · [Widgets](#complex-interaction-patterns)

## Information structure

Resolve the user's objects, tasks and relationships before choosing tabs, sidebars, cards or menus. Distinguish hierarchy from peers, stable global destinations from local/contextual ones, and utility/account/help from the task structure.

Give important concepts a stable home and predictable domain labels. Cross-links can provide alternative paths without contradictory taxonomies. Backend service boundaries do not become navigation merely because they exist.

## Location, scope and return

Use the lightest wayfinding that makes current location, contained information, action/filter scope and return understandable. Stable navigation and active states help peers; breadcrumbs explain meaningful hierarchy; object titles should match navigation language. Contextual return can be more useful than hierarchy when preserving an interrupted task.

Keep browser/system Back useful. Show search/filter scope when users could otherwise misread results, and preserve meaningful position and refinements when returning from an item.

## Findability controls

| Need | Useful choice |
| --- | --- |
| Small understandable set | Browsing may suffice |
| Known-item lookup or large heterogeneous corpus | Search with clear scope and result feedback |
| Narrowing by meaningful attributes | Filters |
| Repeated multi-attribute exploration | Facets when attributes and counts help decisions |
| Change order without excluding items | Sort |
| Repeated return to a useful state | Recent/saved views when persistence saves work |
| Resume discovery | Preserve query, filters, sort and context when safe and expected |

Use domain labels rather than database names. Distinguish an empty corpus from no matches. Expose active constraints and, when complexity warrants it, individual removal and the meaning of combined filters: intersection, alternatives, ranges or another actual model. Metadata alone does not justify a filter. Do not silently reset useful refinement state.

Search indexing, ranking, storage and backend query design remain outside interface ownership. Locale-sensitive matching belongs to [internationalization.md](internationalization.md).

## Multi-step flows

Use steps for meaningful sequence, dependencies or review boundaries; do not fragment a short independent form into a wizard. Keep current progress and remaining shape understandable, permit review/edit of earlier choices where allowed, and preserve valid work across errors and ordinary navigation.

Avoid making users re-enter information the product already has unless actual security/legal/product rules require it. Make branching understandable and distinguish review from irreversible commitment when consequence warrants it. Define the user-facing result of interruption, expiry, partial completion or resumption from known product behavior.

## Complex interaction patterns

Prefer a native control when it expresses the need, then an established platform/accessibility pattern. Custom interaction needs a product reason and proportional usability evidence. Visual resemblance does not establish the correct behavior: selecting a value need not be a menu, tabular data need not be an interactive grid, hierarchy need not be a tree, and a temporary surface need not be modal.

Complex widgets couple semantics, focus, keyboard, state and announcement. Use current target documentation for native controls and current W3C/WAI-ARIA Authoring Practices plus applicable standards for web composite widgets when implementation or review depends on exact behavior. Adding ARIA roles does not repair a wrong interaction model.

For novel patterns, minimize unnecessary novelty and define understandable state, escape and recovery. Drag/drop needs clear selection, destination, outcome, failure/recovery and appropriate keyboard/assistive alternatives. Keep exact keyboard maps, role recipes and platform APIs with their current authority rather than copying them into this Skill.
