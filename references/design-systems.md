# Design-System Decision Support

Use this reference for reusable token/component contracts, themes, shared extensions and system-wide migration. [design-core.md](design-core.md) owns ordinary reuse and local interface changes.

## Contents

[Reuse](#earn-the-abstraction) · [Tokens](#token-roles) · [Components](#component-contracts) · [Themes](#themes-and-modes) · [Change](#shared-change-and-durable-artifacts) · [Interop](#interoperability)

## Earn the abstraction

Identify recurring decisions, known consumers, intentional variation and the current source of truth. Existing code, components, tokens and established artifacts can already be the system; absence of a neat document does not justify a replacement.

Reuse an existing contract when it expresses the need. Add the smallest shared abstraction only when recurrence, shared meaning or maintenance cost warrants it. Otherwise keep the exception local, explaining it only when future maintenance needs the reason. A few repeated feature choices may need shared local roles without becoming a global system.

## Token roles

| Useful reasoning layer | Purpose |
| --- | --- |
| Foundational/reference values | Shared raw scales or source values |
| Semantic roles | Meaning such as surface, text, action, focus, status, spacing or typography |
| Component-scoped roles | A reusable component's needs without leaking its implementation globally |

These are optional reasoning layers, not a required taxonomy. Prefer stable names and traceable aliases that preserve meaning across themes, with clear global/component ownership and coherent scales. Avoid near-duplicate values, misleading location/appearance names, deep alias chains and global tokens for one-off tweaks.

Exact accessibility requirements and actual rendered contrast remain decisive; semantic naming alone does not make values usable.

## Component contracts

Define what consumers need to use the component correctly: purpose, anatomy/slots, required content, meaningful states, recurring variants/sizes, composition constraints, copy limits, adaptive/localization behavior and accessibility/interaction intent. Exact platform semantics remain with current authority.

Keep variants independent where practical rather than turning every visual difference into another boolean combination. Similar appearance does not prove a shared semantic component; do not standardize materially different behaviors merely to reduce file count.

## Themes and modes

Map shared semantic roles to supported light/dark, contrast, brand, density or other values. Preserve hierarchy, focus, selection, success and destructive meaning unless a different experience is explicitly intended. Not every token needs an override, and a theme need not duplicate component architecture.

Distinguish system/user preferences from product themes and define fallback when a mode is unavailable or partial. Use current target authority for exact theme/accessibility APIs.

## Shared change and durable artifacts

A small shared edit can affect many consumers. Identify affected surfaces, meaning versus appearance changes, compatibility, needed migration when updates cannot be atomic, and representative visual/accessibility evidence. Do not silently repurpose an established semantic name to a different meaning.

Keep product/repository/version/release coordination with its owner; design guidance supplies the interface contract and migration consequences. Deprecation timing matters only when the surrounding delivery needs it.

Persist only what continuing use requires in the existing source of truth: token mappings, component/state contracts, mode or extension rules, migration notes, or examples that prevent misuse better than prose. A local change obvious from code needs no separate design-system document. The implementation owner chooses package/file/tool structure.

## Interoperability

A token exchange format is useful when actual tools or platforms need interoperable data. Preserve the semantic model and verify current supported specification/tool versions before choosing the Design Tokens Community Group format or another ecosystem format.

Do not migrate merely because a standard exists or copy its specification here. Framework, component library, documentation site and token-tool mechanisms remain with the implementation/platform owner.
