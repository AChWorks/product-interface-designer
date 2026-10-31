# Adaptive Contexts

Use this depth when resize, windowing, posture, restoration or input changes alter task structure, continuity or composition. Ordinary breakpoint styling can stay with local design/platform work. [platforms.md](platforms.md) owns target conventions and exact platform mechanisms.

## Contents

[Space](#available-space-and-current-state) · [Continuity](#task-and-navigation-continuity) · [Input](#input-transitions)

## Available space and current state

Compose from usable space, content, input and task, not device labels. A large screen may contain a small window; a foldable has no single fixed posture. Preserve authoritative project thresholds unless the accepted work changes them, and favor content/intrinsic thresholds over a device catalog.

Panels, columns, navigation and supporting content may recompose while retaining meaning and the primary task. Treat window/posture geometry as current state rather than a permanent product mode. Keep indispensable content and controls out of known occluded regions, hinges or seams; retain a viable compact layout instead of squeezing a wide one indefinitely.

Use current platform/browser authority for material windowing, geometry, inset, lifecycle and input APIs. The implementation owner selects and verifies the supported mechanism.

## Task and navigation continuity

Preserve meaningful object, selection, draft, filters, reading/scroll position, focus and navigation state through transitions when product/platform behavior permits. Resize should not arbitrarily dismiss ongoing work, duplicate input or discard it. If exact presentation cannot survive, preserve the task and make the new presentation understandable.

Relocation is not navigation: keep destination identity, return expectations and multi-pane selection coherent as panes collapse or expand, without duplicate histories. Different windows may legitimately show different objects; do not force mirroring without product authority.

Restore only state the product can still validate. If staleness, permission change or other invalidation prevents safe continuity, expose the new state and recovery. Shared-state interaction between windows belongs to [collaboration-concurrency.md](collaboration-concurrency.md).

## Input transitions

Actual input capability can change while the product remains open; viewport size does not establish it. Required actions need a usable path for the inputs the product supports, with pointer/touch efficiency and logical keyboard focus as regions move.

Hover can enrich but cannot carry essential information when other supported inputs need it. Provide an alternative when another supported input cannot perform a drag or gesture, unless that interaction is essential to the task; introduce pen, remote/gamepad or other behavior only when supported and useful. Use reliable platform signals for input hints rather than guessing from a device category.

When continuity is impossible or unsafe, make that limitation and the next useful action clear instead of pretending the previous interaction remains valid.
