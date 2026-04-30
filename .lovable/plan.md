# Responsive Layout Testing Plan

Visual verification of all four pages across desktop, tablet, and mobile viewports in both portrait and landscape orientations. Read-only — no code changes unless you approve fixes after the audit.

## Pages tested
1. Home (`/`)
2. Services (`/services`)
3. About (`/about`)
4. Contact (`/contact`)

## Viewports per page (6 sizes)

| Class | Portrait | Landscape |
|-------|----------|-----------|
| Desktop | 1920×1080 | 1366×768 |
| Tablet | 820×1180 (iPad Air) | 1180×820 |
| Mobile | 390×844 (iPhone 14) | 844×390 |

Total: **4 pages × 6 viewports = 24 screenshots**

## What I'll inspect on each capture

- **Navbar**: logo + phone number + nav links alignment; mobile hamburger toggle (open + closed on mobile sizes)
- **Hero**: headline wrapping, CTA button stacking, background crop, no text clipped under fixed nav
- **Section headings**: line breaks and readability of long descriptions (e.g. "Voice of the Owner" paragraph)
- **Service cards**: column count transitions (3 → 2 → 1)
- **Process timeline**: 5-col → 3-col → 1-col, connector lines
- **Advantages grid**: icon + text alignment
- **Footer**: column collapse and spacing
- **Universal checks**: horizontal scroll, overlapping elements, awkward whitespace, tap target sizes (≥44px) on mobile, illegible text

## Process

1. Open browser at sandbox preview
2. For each page → resize to each of the 6 viewports → screenshot → review
3. On mobile sizes, also open the hamburger menu and screenshot it
4. Compile findings into a single report grouped by **Severity** (Critical / Minor / Polish) and **Page/Viewport**

## Deliverable

A written report listing every issue found with:
- Page + viewport where it occurs
- What's wrong (with screenshot reference)
- Suggested fix

After you review the report, you can tell me which issues to fix and I'll switch to build mode to apply the changes.

## Notes

- The browser tool snaps to its nearest supported size, so actual captures may be ±a few pixels from the targets above (e.g. 390×844 is exact; iPad Air 820×1180 is supported exactly).
- I won't interact with forms (Contact page) destructively — only visual inspection plus opening the page.
- This is purely a visual audit; no code changes happen during the plan execution.
