# Instruction Architecture and Skill Composition

Status: **AUTHORITATIVE AUTHORING DESIGN**

This document defines how Product Interface Designer instructions should be structured so another AI can discover, reason with, and compose the Skill reliably. It is a project-authoring specification, not part of the distributable runtime unless a rule is promoted into `SKILL.md` or a runtime reference.

## 1. Design objective

Optimize for **decision clarity per context token**.

Assume a capable AI. State the outcome, decision-changing constraints, important exceptions and sufficient evidence; leave ordinary execution choices to professional judgment. An instruction earns its place when removing it would change a relevant decision, weaken a real boundary or leave meaningful ambiguity.

Make that guidance easy to select at its canonical owner. Use sections within a reference when a bounded task needs only part of the domain. The goal is a correct, useful result with less unnecessary instruction work, not the fewest words or the most explicit steps.

## 2. Runtime topology

The metadata activates the Skill. `SKILL.md` resolves authority and selects direct references; those references support the interface decision, implementation or review. In composed work, the bounded result returns to the caller and its established implementation owner.

Rules:

- Keep `SKILL.md` as the control plane, not a knowledge dump.
- Keep runtime references one level deep from `SKILL.md`.
- Give each durable concern one canonical runtime owner.
- Load conditional domains only when relevant.
- Do not create a new reference merely because a topic has many notes; create it when it represents a distinct recurring decision domain.

## 3. Choose representation by reasoning shape

| Reasoning need | Preferred representation | Avoid |
|---|---|---|
| authority/conflict resolution | short ordered precedence | prose that hides which rule wins |
| conditional routing | decision table or compact decision tree | long narrative branches |
| ownership/composition | table with one owner per concern | overlapping prose in several files |
| necessary ordering or state transition | compact flow only when order/state changes correctness | obvious step sequences or ceremonial phases |
| heuristics/principles | concise prose + bullets | fake algorithmic precision |
| evidence levels | ordered scale/table | mixing observed and assumed evidence |
| comparisons/trade-offs | table only when dimensions are stable and comparable | tables used merely for visual formatting |
| exceptions/edge conditions | local rule next to the parent decision | distant catch-all exceptions |
| examples | a minimal observation, decision and evidence example where ambiguity remains | catalogs or examples that become mandatory templates |

### Decision-tree rule

Use a tree only when:

- the branch condition is observable;
- branches materially change behavior;
- the tree reduces ambiguity more than ordinary prose.

Do not encode subjective continuous design judgment into artificial yes/no trees. A paragraph is preferable when context and exceptions are the substance; a table is preferable when distinct conditions change the decision. Authoring structure does not require the same structure in the agent's answer.

## 4. Canonical ownership and duplication control

Before adding a rule:

1. identify the decision it changes;
2. identify the canonical owner reference;
3. check whether an existing rule already yields the same decision;
4. merge/refine the existing rule when possible;
5. create a new owner only when the concern has a distinct trigger, evidence model, or decision surface.

Other references may point to the owner but should not restate its rule set.

## 5. Decision precedence

Runtime precedence must distinguish **desired outcome/preferences** from **non-negotiable applicable constraints**.

The control plane should make conflicts resolvable without forcing the AI to infer policy from paragraph order.

Keep the ordered runtime precedence in `SKILL.md`. It must prevent an aesthetic/user preference from silently overriding an applicable legal, safety, accessibility or platform requirement, and preserve authoritative product/design truth above optional domain or stylistic advice.

## 6. Specialist composition model

Product Interface Designer is a **consulted specialist**, not a nested project Master.

### Generic composed flow

Consult Product Interface Designer for a materially unresolved interface decision or requested review, then return the bounded result and control. The caller continues its workflow through the existing implementation owner when execution is applicable. Follow the runtime [reuse and re-entry contract](../references/composition.md#reuse-and-re-entry); another implementation step does not by itself require consultation.

The caller remains authoritative for its own workflow. Project/platform/implementation owners retain their existing authorities; composition does not create a nested Master or transfer repository/integration/release ownership.

### Interface decision packet

The runtime [interface-decision packet](../references/composition.md#interface-decision-packet) owns the six information fields and their semantics. Return only the information the caller needs, including evidence actually used and material limitations; do not maintain a second field definition here.

These are information needs, not mandatory headings or a requirement to repeat known facts or empty fields. Do not return a second project plan, repository workflow, release plan, or implementation mechanism owned by another Skill.

## 7. Composition with AChWorks Skills

| Active Skill | Product Interface Designer owns | Other Skill retains |
|---|---|---|
| GitHub Project Orchestrator | material UI/UX decision, design constraints, interface review | outcome/scope, repository/task coordination, implementation strategy ownership, integration, CI, release, continuity |
| WP Native Builder | user-facing hierarchy, interaction, visual/UX/accessibility/locale intent | WordPress/Gutenberg/theme/plugin/WooCommerce owner/mechanism, serialization/lifecycle safety, publication |
| ACh Idea Advisor | interface implications after product outcome is sufficiently defined | whether/why to build, product outcome, product capability reuse, product-local/Foundation/project placement, evidence-backed idea maturation |

### Escalation back to the caller

Return control instead of guessing when the unresolved choice materially changes:

- product/business behavior rather than interface expression;
- project/repository scope or priority;
- platform architecture/mechanism ownership;
- security/privacy/data policy outside user-facing presentation;
- legal/compliance policy;
- another owner's durable contract.

Ordinary reversible interface decisions remain inside Product Interface Designer.

## 8. Evidence discipline

The Skill should distinguish at least:

- authoritative product/design facts;
- inferred design hypotheses;
- static implementation evidence;
- rendered interaction/visual evidence;
- measured/assistive evidence;
- actual user/task evidence when available.

Do not call a design “validated” merely because it renders correctly or passes an accessibility scan.

For material new interaction models, unusual navigation, complex workflows, or consequential redesigns, the Skill should know when user/task evidence may be needed while remaining useful when such evidence is unavailable.

## 9. Current-authority routing

Durable principles belong in the Skill. Exact version-sensitive requirements belong to the current authoritative source.

Runtime guidance should tell the AI to consult current official documentation when exact behavior materially depends on:

- accessibility standards/patterns;
- native platform conventions;
- browser/platform APIs;
- legal/regulatory requirements;
- another authoritative product/platform contract.

Do not vendor entire standards merely to avoid current retrieval.

## 10. Context-budget rules

- Prefer one high-signal rule over several synonyms.
- Keep routing/authority near the entrypoint.
- Move detailed domain knowledge out of `SKILL.md`.
- Select relevant sections; do not load unrelated locale/platform/advanced guidance or follow cross-links automatically.
- Avoid catalog-style lists unless lookup itself is the capability.
- Avoid “always check everything” wording; activate concerns by materiality.
- Use tables only when scanning relationships is faster than prose.
- Use prose when nuance or professional judgment matters.
- Use examples sparingly and never let examples silently become mandatory templates.

## 11. Review standard for future Skill edits

Before integrating a Skill-content change, ask:

1. Does it close an evidenced decision gap?
2. Is this Product Interface Designer's responsibility?
3. Is the rule non-obvious enough to earn context?
4. Does it have one canonical owner?
5. Is the chosen representation appropriate for how an AI must reason with it?
6. Does it conflict with or duplicate another AChWorks Skill?
7. Does it preserve standalone usefulness?
8. Does it preserve composed usefulness?
9. Does it need current external authority instead of frozen local detail?
10. Can any existing instruction be removed or simplified because of this change?

For semantic changes, trace the materially affected cases in [THEORETICAL-SCENARIOS.md](THEORETICAL-SCENARIOS.md), including adjacent routing, ownership, questioning, evidence or composition effects. Use a few short probes only when they resolve a remaining ambiguity; no behavioral multi-model/harness program is required. Record the exact reviewed change and evidence in its PR. Theoretical coherence and text reduction do not establish measured model performance or UI quality.
