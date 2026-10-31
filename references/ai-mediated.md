# AI-Mediated Interfaces

This reference owns the user-facing contract when AI materially shapes content, recommendations, decisions or actions. Model/provider choice, prompts, training, evaluation infrastructure, enforcement and risk/legal/data policy remain with their owners.

## Contents

[Expectations](#expectations-and-uncertainty) · [Control/actions](#correction-and-consequential-actions) · [Progress/failure](#progress-failure-and-recovery) · [Feedback/data](#feedback-and-data-choices)

## Expectations and uncertainty

Make AI involvement legible when it changes how users interpret accuracy, authorship, variation, personalization, responsibility or the need to review. Otherwise use task language rather than ubiquitous AI branding.

Explain capability and material limits in terms of the job and context the system actually receives. Distinguish advice or a generated draft from a committed record or human-approved result. Do not imply expert authorship, human review, determinism, reliable uncertainty detection or verification without product evidence. A demonstration is not performance evidence, and generic warning copy does not repair a risky decision.

Prefer actionable uncertainty or alternatives over misleading precision. Show a numeric confidence only when it exists, is meaningful/calibrated for the decision, and the product defines its interpretation. Wording, token probabilities or model self-assessment do not justify inventing a percentage.

Distinguish authoritative source material from generated synthesis where verification matters. Absent provenance cannot be replaced by citation-like UI. Exact audit, retention or explanation obligations remain with current product/policy authority.

## Correction and consequential actions

Offer the controls the task and product support: edit, refine context, retry/regenerate, choose alternatives, dismiss, restore/undo or use a manual path. Preserve useful edits and context during retry unless a fresh start is required. Retrying generation must not silently repeat a consequential external action.

Separate proposing from committing when effects are materially financial, destructive, external, privacy-sensitive, permission-related or otherwise consequential. Make scope and consequence understandable and preserve review/edit/confirm/cancel control unless authoritative product/policy rules establish a different safe mechanism. Examples include publishing, sending, overwriting, purchasing, permission changes and bulk actions.

[trust-agency.md](trust-agency.md) owns transparent choice and consent; backend authorization, idempotency and transaction safety remain with implementation/security. AI attribution does not remove meaningful user control.

## Progress, failure and recovery

Reflect states the product can know: queued, generating, executing a tool/action, complete, cancelled or failed. Streaming content may still be incomplete or changing; animation is not evidence of progress, and unknown completion cannot support a deterministic percentage.

Provide stop/cancel when supported and useful, retain safe useful partial output, and make long-running work's status and re-entry understandable if users leave the surface.

Distinguish unsupported input, authoritative low-confidence/incomplete signals, generation failure, downstream action failure, product-rule rejection and cancellation when actual evidence allows. Offer the relevant next step: revise input, retry safely, inspect partial output, take a manual path or return later. Avoid raw provider errors unless technical users need them.

Generated text saying an action succeeded is not evidence that the external action succeeded. Report the product's actual outcome.

## Feedback and data choices

Separate editing the current result from sending product/model feedback when consequences differ. Explain feedback's useful purpose without implying training or personalization unless the product actually provides it. Optional quality feedback should not obstruct task completion without an authoritative requirement; reporting a problem should not demand unnecessary private content.

For files/history, sensitive context, personalization/memory or external-tool access, explain scope, effect and supported control/revocation from known policy. Distinguish temporary task context from durable memory/history where the product does. Do not invent retention, training exclusions, encryption or third-party data guarantees.

Use [trust-agency.md](trust-agency.md) for user-facing disclosure and its policy owners for enforcement. Exact AI policy/risk/legal/platform requirements come from current authority when material, not frozen model capability tables or regulatory catalogs.
