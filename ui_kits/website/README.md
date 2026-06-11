# FSP Website · UI Kit

Recreation of the FSP marketing website — single-page deck of 4 screens (Nav · Hero · Projects · Technology · CTA · News · Footer). All HTML/CSS, no framework dependency — the brand goes for square, hairline, no-shadow geometry which is faster to edit as raw markup.

## What's in here

- **`index.html`** — full clickable screen. Open in browser to see all sections.
- **`../../colors_and_type.css`** — design tokens (use this in your own files).
- **`../../reference/FSP Website.html`** — original from the user (untouched, for diffing).

## How to use a screen / component from it

1. Find the section in `index.html` (use `data-screen-label` attrs: `01 Hero`, `02 Projects`, `03 Technology`).
2. Copy its block of markup + its CSS rules from the inline `<style>`.
3. Paste into your file, alongside `colors_and_type.css`.
4. Asset paths: change `../../assets/...` to whatever's correct for your file location.

## Component inventory (selectors → what it is)

| Selector | What |
| --- | --- |
| `.nav` / `.nav-brand` / `.nav-links` / `.nav-right` | Sticky top nav with paper+blur background, brand mark, phone, primary CTA |
| `.btn` / `.btn.ghost` / `.btn.light` / `.btn.sm` / `.btn.arrow` | Buttons. `.arrow` adds the linear arrow icon. |
| `.hero-grid` / `.hero-left` / `.hero-photo` | Hero: 2-col with photo + frame-overlay caption |
| `.hero-tag` | Pill kicker with dot |
| `.hero-meta` | Inline stat row (3×) |
| `.hero-strip` | 4-col value-prop strip with numbered eyebrows |
| `.sect-head` | Section header — kicker + h2 + actions |
| `.tab-row` / `.tab` / `.tab.on` | Segmented tab control |
| `.proj-grid` / `.proj` | Project card grid (4-col) — see card.body anatomy in HTML |
| `.proj-grid .more-tile` | Dark "see all" CTA tile |
| `.stats-band` | 4-up big-number band with `.st b` and `.st span` |
| `.tech-vis` | Dark 3-layer panel cutaway visualization |
| `.process` / `.steps` / `.step` | Numbered process list, current step highlighted |
| `.cta-band` | Dark CTA band with form (graphite + navy pattern overlay) |
| `.news-grid` / `.news` / `.news.feature` | News card list (feature + 2 standard) |
| `.foot-cta` / `.foot-main` / `.foot-pat` / `.foot-legal` | Footer in 4 stacked layers (dark CTA → main → strip-pattern → legal) |
| `.dots-side` | Floating right-edge scrollspy |
| `.mk` / `.mk.s/m/l/xl` / `.mk.light` | The III mark — primary brand element |

## Brand mark · usage in code

All over the site the III mark is `<span class="mk SIZE"><span class="b"></span><span class="b"></span><span class="b"></span></span>`. Sizes: `s` / `m` / `l` / `xl`. Light variant: add `.light`. The graduated colours (light → medium → dark navy) are applied via `:nth-child` selectors in the `__brand-bars` style block at the bottom of `<head>`. **Don't replace this block** when you reuse markup.

## What's _not_ in this kit

- **Inner page templates** (project detail, blog post, calculator). The brand uses the same tokens — just compose from the components above.
- **Mobile menu.** Nav links hide below 1100px (`@media (max-width: 1100px) { .nav-links { display: none; } }`); a real burger menu isn't designed in the source. Add when needed.
- **Form validation states** beyond the basic `border-color: var(--navy)` focus. The brand has no error styling rules in the source — invent against tokens (red border + 11px red help text) if you need them.
