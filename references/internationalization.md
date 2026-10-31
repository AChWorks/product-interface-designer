# Internationalization and Localization

This reference owns general language, script, direction and locale-sensitive interface behavior. [persian-rtl.md](persian-rtl.md) adds Persian/Iran-specific guidance only when that context is active.

## Contents

[Dimensions](#independent-dimensions) · [Messages/scripts](#messages-and-script-variation) · [Formatting/data](#formatting-and-canonical-data) · [Direction](#direction-and-bidirectional-text) · [Search/sort](#search-and-sorting)

## Independent dimensions

| Dimension | Decision |
| --- | --- |
| Language | Labels, messages, content and assistive text |
| Script | Glyph coverage, shaping and typography |
| Direction | Base direction and mixed-direction runs |
| Locale/region | Required formatting and regional conventions |
| Numbering system | Visible digits, grouping, decimal, percent and signs |
| Calendar/date/time | Calendar, patterns, hour cycle and time zone |
| Currency/units | Semantic unit and its display |
| Names/addresses/domain data | Valid field shapes, order and labels |
| Collation/search | Expected sorting, matching and normalization |

Evidence for one dimension does not settle another. Arabic-derived script does not establish Persian, Iran, a calendar or a numbering system; RTL does not establish a currency or address format. One language can serve several regions, and a product can support multiple combinations. Follow actual product requirements.

## Messages and script variation

Write complete translatable messages with variables structurally separate so grammar can reorder them. Use the localization system's plural/select capabilities for count, gender, case or other relevant categories; English sentence structure is not a universal grammar. Preserve established terminology and technical identifiers whose translation would change meaning.

Allow expansion, wrapping, different word boundaries and glyph metrics. Avoid essential text embedded in images, Latin-only capitalization/letter-spacing assumptions and abbreviations that merely protect a brittle layout. Fonts and real weights must cover active scripts and shaping; verify fallback and dense controls with representative localized content. Preserve language metadata where the platform needs it for rendering or accessibility.

## Formatting and canonical data

Localize display without silently changing meaning or machine data. Visible numbers, dates, intervals, time zones, currency and units may differ from storage/API formats. Parse accepted localized input through maintained locale-aware implementations and established product rules, not ad-hoc replacement.

A language does not choose a currency, direction does not choose a calendar, and regional familiarity does not authorize semantic unit conversion. Show the relevant time zone or instant when ambiguity would change a decision. Names and addresses are domain data; collect only required fields and use the active locale's actual product requirements.

Regional identity, banking, payment, tax, shipping, calendar and work-week behavior must come from current product/domain authority. Do not invent formats, checksums or legal requirements from a locale label.

Use maintained platform/locale implementations for formatting, calendars, pluralization and collation. When exact behavior matters, consult current product/platform, Unicode CLDR, Unicode, W3C or applicable domain authority; large locale tables and algorithms do not belong in this Skill.

## Direction and bidirectional text

Apply base direction at the correct surface or string scope, separately from language. Use logical start/end for reading-flow-relative spacing, alignment and borders, while retaining physical left/right for genuinely spatial meaning. Keep source and focus order semantically meaningful instead of reversing controls to imitate RTL.

Isolate intrinsic opposite-direction runs—URLs, email, code, identifiers, phone/account numbers and mixed-script user content—with the target platform's bidi mechanisms. Check punctuation, parentheses, slashes, neutral characters, selection, copy/paste and editing where they affect use. Use current Unicode/W3C/platform guidance for exact controls rather than inventing bidi recipes.

Mirror an icon or transition only when its meaning follows reading direction. Global mirroring can reverse physical, media or identity meaning incorrectly. Reflow localized content at realistic widths instead of treating mirroring as proof of usability.

## Search and sorting

Use locale-aware collation when alphabetical order matters; Unicode code-point order or ASCII case-folding may not match users' expectations. Matching can account for diacritics, script variants, alternate digits, punctuation, whitespace or transliteration when the product's content and users warrant it.

Keep matching/normalization separate from displayed authoritative content. Normalize only forms the product/search contract permits, preserving identifiers and original data as required. Product-critical matching needs representative-data evidence; one language or query does not establish coverage. Indexing, ranking and backend search architecture remain with their engineering owner.
