# Persian / Iranian Interface Specialization

Apply this guidance when Persian language/script or Iranian-local product behavior is active. [internationalization.md](internationalization.md) owns the general dimensions. RTL alone does not imply Persian, Iran, Persian digits, Jalali dates or Iranian currency.

Persian copy can use Gregorian dates, Latin digits or non-Iranian currency when required. Apply Persian writing rules without importing Iranian product rules; apply Iranian domain requirements without forcing Persian language. Arabic, Hebrew, Urdu and other RTL contexts retain their own conventions.

## Contents

[Writing/typography](#persian-writing-and-typography) · [Mixed direction](#mixed-direction-content) · [Display choices](#digits-calendar-and-currency) · [Composition](#interface-composition) · [Iranian domain rules](#iranian-product-requirements)

## Persian writing and typography

Use fonts and real weights that support the required Persian glyphs and shaping, with appropriate shipping rights. Preserve joined-script shaping; arbitrary letter spacing and synthetic faces can degrade it. Allow enough line height for glyphs/diacritics, verify fallback and keep labels readable at actual density. Latin runs should coexist deliberately.

Retain meaningful ZWNJ (نیم‌فاصله). Author Persian copy with Persian ی and ک rather than Arabic ي and ك unless authoritative data intentionally preserves another form. Use appropriate Persian punctuation and spacing, including «گیومه»، «،»، «؛» and «؟». Prefer layout-aware clamping over raw-character cuts through joined text; Latin casing rules do not apply.

Keep established terminology and a consistent product-appropriate register, without accidental formal/colloquial verb mixing. Prefer familiar task language over literal translation of implementation terms. Alternate character/digit normalization belongs to the search or validation contract; do not silently rewrite authoritative display content.

## Mixed-direction content

Keep surrounding Persian text RTL while isolating intrinsic LTR runs with the platform's bidi mechanism. Relevant content includes URLs, email, paths, commands, code, IDs, versions, Latin names and phone/account/card/IBAN/OTP sequences. Translating or reversing an identifier can change its meaning.

Check punctuation, parentheses, slashes, hyphens, cursor/selection and copy/paste around Persian/Latin runs. Repair the token's direction instead of switching an entire sentence or form to LTR. Directional navigation follows the actual interaction, not blanket mirroring. Use current platform/Unicode/W3C authority when exact bidi behavior is needed.

## Digits, calendar and currency

| Product choice | Preserve |
| --- | --- |
| Persian digits | Consistent visible presentation while protocol/API/identifier values retain their required format. Accept equivalent Persian/Arabic/Latin input only when permitted, through locale-aware normalization before validation. |
| Persian/Jalali calendar | A maintained calendar implementation, with relevant parsing, ranges, leap behavior, labels, week conventions, time zones and boundaries verified against current product/library/platform evidence. Canonical timestamps remain separate. |
| Iranian money | An unambiguous chosen unit; never silently mix Rial and Toman. Calculations/accounting stay in the authoritative canonical unit. |

None of these choices follows automatically from Persian language or RTL. Keep Gregorian or other required calendars, numbering and currency conventions when the product selects them.

## Interface composition

| Surface | Persian-specific concern |
| --- | --- |
| Forms | Coherent Persian labels with appropriately isolated LTR values; correct prefixes/suffixes, validation association and logical focus order. Check numeric input and OTP/multi-cell order and paste when used. |
| Navigation/overlays | Correct meaning for back/forward, breadcrumbs, pagination, steps, drawers and sheets while preserving platform/system conventions. |
| Tables/charts | Column order serves comparison; Persian labels and mixed-script/numeric cells stay legible. Localize axes, legends, tooltips, dates and numbers only for selected dimensions. |
| Responsive/accessibility | Representative Persian strings at relevant widths, correct language/direction metadata, and logical reading/focus order. Mirrored appearance alone is insufficient. |

[review.md](review.md) owns rendered verification and evidence claims.

## Iranian product requirements

Iranian phone, identity, Sheba/banking/payment, address/postal, shipping or working-week/holiday behavior applies only when the product requires it. Retrieve the current product/domain/legal/platform rule for material formats, checksums, validation or policy. Persian design knowledge does not establish those rules.
