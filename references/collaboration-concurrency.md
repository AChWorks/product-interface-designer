# Collaboration and Shared State

This reference owns what users need to understand and control about shared state. Sync/storage architecture, transactions, CRDT/OT, locking algorithms and authorization enforcement remain with engineering/security owners.

## Contents

[State](#truthful-shared-state) · [Participants](#presence-ownership-and-permission) · [Conflicts](#conflicts-and-recovery) · [Changes during work](#changes-during-a-session)

## Truthful shared state

Use the smallest vocabulary the product can support, distinguishing local unsaved work, client persistence, shared-system acceptance, synchronized/current state, stale versions, pending/failed sync and restrictions when those differences affect use. A generic “saved” or success indicator must not conceal a material sync failure.

Preserve local work and offer retry/recovery when supported. Reconcile remote updates automatically only when local context is safe. If stale data or a remote update changes the meaning of the current action, expose that before commitment; harmless live updates do not need interruption.

## Presence, ownership and permission

| Concept | Meaning |
| --- | --- |
| Presence | A participant/session is known to be active, not necessarily viewing or editing this object |
| Selection/cursor/focus | The interaction scope the product actually tracks |
| Ownership/assignment | Durable role or responsibility, independent of presence |
| Lock | A real restriction imposed by a defined mechanism, not inferred from presence |
| Permission | What the actor is allowed to do, which can change independently |

Use participant identity/state cues only at the precision the product knows and privacy rules allow. Color alone may not distinguish them sufficiently. Transient typing/editing state is not a permanent lock.

## Conflicts and recovery

Explain the decision rather than the merge algorithm. When safe automatic reconciliation is unavailable, show the affected object/field/scope and enough difference for a choice. Preserve current work until resolution where practical.

Name “keep mine,” “use latest,” “merge,” “copy” and “cancel” by actual consequence, including discarded work and available recovery. Newer does not automatically justify destructive overwrite. Safe automatic merging needs no ceremony, but the interface cannot claim a merge that did not succeed. [trust-agency.md](trust-agency.md) owns consequential overwrite transparency.

History can support understanding and recovery when the product provides it. Use authoritative actor/time/version data; distinguish viewing from restoring, copying or reverting. Explain whether restoration creates a version or rewrites history when that affects consequence, and permit inspection before a consequential restore. Do not invent audit guarantees, authorship, timestamps or summaries; retention/audit policy has its own owner.

## Changes during a session

Reflect changed roles, permissions or ownership without leaving stale actions apparently available. Preserve unsent work when safe, explain the new restriction and next step, distinguish permission loss from transient failure, and avoid repeatedly retrying an unauthorized action. For work already in flight, report the actual outcome rather than assuming previous permission guaranteed success.

Keep presence and routine activity quiet; notify explicitly when a change invalidates the task or decision. Preserve reading/editing position, focus and stable controls instead of moving them for low-value live updates or creating toast storms.

If an unknown backend guarantee would change the interface, return that engineering/product fact rather than designing a false shared-state model.
