---
name: fsp-design
description: Use this skill to generate well-branded interfaces and assets for ФСП (FinStroyPanel) — manufacturer of energy-efficient prefab reinforced-concrete houses (Finnish monolithic technology). Contains essential design guidelines, colors, type, fonts, assets, and a website UI kit for prototyping. Brand language is engineering-document, square geometry, no decoration.
user-invocable: true
---

# FSP Design System Skill

Read the `README.md` file within this skill first — it covers brand context, content fundamentals (tone of voice, casing, no emoji), visual foundations (palette, type, spacing, motion, geometry), and iconography rules.

Then explore other available files:

- `colors_and_type.css` — design tokens (Navy / Graphite / Paper / Red, Montserrat 300–900, 8px spacing scale, motion, borders). **Import this in any FSP artifact.**
- `assets/` — logos (`logo_main.png`, `new_logo_render.png`, `logo_2026_*.png`), real photos (`project_*.jpeg`, `oiva_*.jpeg`), real merch (`merch_*.png`). Copy what you need; never invent logos or fake photos.
- `reference/FSP Design System.html` — full 15-section brandbook. **Source of truth** for any rule.
- `reference/FSP Website.html` — original marketing site, fully working.
- `ui_kits/website/index.html` — recreation you can copy components from (Nav, Hero, Project Card, Tech cutaway, CTA band, News, Footer).
- `preview/` — small cards demonstrating individual tokens / components.

## Working rules

If creating **visual artifacts** (slides, mocks, throwaway prototypes), copy assets out of `assets/` and create static HTML files for the user to view.

If working on **production code**, copy `colors_and_type.css` and read the rules in `README.md` to become an expert in designing with this brand.

## When the user invokes without other guidance

Ask what they want to build or design — landing page, slide deck, social post, presentation, bid document, project catalog page. Then ask a couple of pointed questions:

- What's the audience — clients, partners, ÖFiCe?
- What's the call to action — order, download PDF, schedule meet?
- Is it digital or for print (different min font sizes, different paper backgrounds)?

Then act as an expert FSP designer who outputs HTML artifacts _or_ production code, depending on the need.

## Hard rules (do not break)

1. **No emoji.** Anywhere. The brand voice prohibits them explicitly.
2. **No rounded corners.** All UI elements are square (`border-radius: 0`).
3. **No drop-shadows** on logos, type, or static elements. Hover-only on cards.
4. **No gradients** except the spec'd paper→paper-2 on cover and the cover-stripes. Never bluish-purple gradients.
5. **One font: Montserrat.** No exceptions.
6. **The III mark has 3 bars of different widths AND colors.** Width ratio is **2 : 3 : 4** (left → right, narrow→medium→wide). Colors go light→mid→dark navy. If your three bars are all the same width or all the same color — **it's not the FSP logo.** This is the most-broken rule by AI assistants — fix it first.
7. **Red is signal-only.** Never a primary CTA. Spec'd uses: warnings, "срочно" badges, fieldwear accent, infographic call-outs.
8. **Tone is engineering, not marketing.** «120 мм утеплителя», not «самые тёплые». «47 дней», not «быстро».
9. **Numbers are tabular** (`font-feature-settings: "tnum"`).
10. **Eyebrow / labels are UPPERCASE** with tracking `0.08em` – `0.20em`.

Now read the README and start.
