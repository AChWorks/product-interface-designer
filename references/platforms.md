# Platform Guidance

Use the section for the actual target, established by the request or product/repository evidence rather than appearance. If an unresolved target materially changes the decision, recover or return that fact; otherwise work at the shared layer.

## Contents

[Shared intent](#shared-product-intent) · [Web](#web) · [Mobile/native](#mobile--native) · [Desktop](#desktop)

## Shared product intent

Keep product concepts and terminology coherent while adapting navigation, composition, density, input, feedback and lifecycle behavior. Shared semantics do not require identical component markup or one platform's presentation as the source of truth.

Use the project's established component system. Account for actual pointer, touch, keyboard, pen, remote/gamepad or assistive input, supported safe areas, text scaling, high contrast and reduced motion. Reuse visual tokens where they remain usable on the target.

When supported and useful, haptic/audio feedback can reinforce input or state. Essential meaning needs another suitable channel; respect user/system preferences such as mute or reduced haptics and current platform capabilities. Do not add these channels as decoration.

For multiple targets, preserve shared intent and verify material platform-specific behavior on each; native conventions can legitimately produce different interfaces.

## Web

Use navigation semantics for navigation and controls for actions. Preserve browser link opening, history, refresh, Back/Forward, selection, copy/paste and zoom. Deep-link meaningful state where sharing, refresh or history continuity matters. Prefer semantic document/control structure before ARIA augmentation.

Support keyboard and pointer as appropriate; required actions cannot depend on hover alone. Forms should cooperate with autofill, password managers, input modes, paste and validation. Do not disable zoom to hide layout problems. On mobile Safari, avoid input styling that causes unwanted focus zoom/readability issues; retrieve current guidance if an exact threshold matters.

Prefer intrinsic responsive layout across the supported viewport range. Account for reflow, zoom, dynamic viewport behavior, scrollbars and safe-area insets where relevant. Preserve focus and reading context during async changes and make optimistic, saved/unsaved, in-flight, error and retry state truthful. Framework-specific behavior follows the established stack.

## Mobile / native

Respect the target's navigation, presentation, system bars/insets and restoration model. Touch targets and spacing must be usable without hover; critical gesture-only actions need an accessible alternative. Consider reach and system areas where they change use.

Text scaling and translation must not hide primary actions. Use native accessibility semantics through the actual framework. Forms need to survive keyboard appearance, viewport reduction, field scrolling, next/submit actions, dismissal, autofill, OTP and password-manager behavior.

| Target | Distinctions that can change the design |
| --- | --- |
| iOS/iPadOS | Preserve native back/navigation gestures, safe areas and Dynamic Type. Use semantic system colors/materials and established controls when suitable; respect Reduce Motion and the native navigation model. Retrieve current Apple guidance for exact target sizes or capabilities. |
| Android | Respect system Back/predictive Back, edge-to-edge/window and IME insets. Adapt navigation to available window size, support system text/accessibility settings and reduced animation, and use semantic theme/Material or native roles when suitable. Retrieve current Android/Material guidance for exact requirements. |

Do not create a pseudo-native hybrid when conventions materially differ, or import browser chrome and desktop menu behavior without a product reason.

## Desktop

Use windows, keyboard, pointer precision and dense workflows where they help the task. macOS, Windows, Linux/desktop environments and cross-platform shells can differ in menus, chrome, commands, document/file behavior, accessibility and lifecycle. Use the actual target's current authority for exact conventions.

Handle resize, useful panel/content limits, state restoration, display scaling and multiple monitors where supported. Shortcuts, command palettes, multi-select and context actions need discoverability and must respect system commands. Drag/drop, selection ranges and resize handles can use pointer precision without hiding essential meaning in hover.

Use native menus/dialogs/chrome when the framework and product call for them. Product-specific shell chrome is valid when window controls, focus, modality and system shortcuts still behave correctly.
