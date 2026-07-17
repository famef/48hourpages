# Design System: Run It Agency — AI Ads Agency Landing Page

Reference: Perspective Funnels marketing site (white SaaS, centered marketing layout).
Deliberate deviations from the anti-slop defaults, justified: the reference is a
centered-hero conversion page, so variance is intentionally low (symmetric, centered);
supporting pastel surfaces exist alongside the single interactive accent because the
reference's hero collage and offer cards depend on them.

## 1. Visual Theme & Atmosphere
A bright, optimistic SaaS marketing page — "Daily App Balanced" density (5),
"Predictable Symmetric" variance (3), "Fluid CSS" motion (5). Feels like a
well-funded conversion-optimization product: white canvas, confident centered
headlines, one blue accent doing all the interactive work, and a playful
pastel card collage in the hero. Trust is built with facts and checkmarks,
not adjectives.

## 2. Color Palette & Roles
- **Canvas White** (#FFFFFF) — primary page background
- **Cloud Wash** (#F6F7F9) — alternating section background, input fills
- **Charcoal Ink** (#171A20) — headlines, primary text (never #000)
- **Muted Steel** (#5D6473) — body copy, secondary text
- **Whisper Border** (#E7E9EE) — 1px card borders, dividers
- **Runner Blue** (#2456E6) — the single interactive accent: CTAs, links, focus rings, active states
- **Deep Ink Card** (#14161C) — the one dark statement card ("why now" quote)
- Supporting pastel *surfaces* (backgrounds only, never interactive):
  **Butter** (#FFE9A8), **Coral Mist** (#FFD9CF), **Sky Mist** (#D9E6FF), **Mint Mist** (#DCF2E4)
- Final CTA gradient: soft wash `linear-gradient(140deg, #D9E6FF, #FFE9A8, #FFD9CF)` at low opacity under white — no neon, no purple.

## 3. Typography Rules
- **Display:** Outfit (700/800) — geometric, friendly, track-tight (-0.02em), scaled with clamp(); hierarchy via weight, not size screaming
- **Body:** Outfit (400/500) — relaxed 1.65 leading, 60ch max line length
- **Mono:** ui-monospace stack — stat figures, meta labels, form helper text
- **Banned:** Inter, generic serifs, gradient text on headlines

## 4. Component Stylings
- **Buttons:** Pill radius (999px), Runner Blue fill, white text, soft blue-tinted shadow; hover darkens + lifts 1px; active pushes down 1px. Ghost variant: white fill, whisper border. No outer glows.
- **Cards:** 20–24px radius, white fill, whisper border, diffused ink-tinted shadow. Pastel-surface cards for offers. UI-mock cards (chat answer, audit report, prompt map) styled as product screenshots.
- **Check lists:** Blue check glyph in a tinted circle, 15–16px text.
- **Inputs:** Cloud-wash fill, whisper border, pill-ish 12px radius, focus ring in Runner Blue. Label via placeholder + aria-label (single-field lead form).
- **Chips:** Small pill tags (category chips, "Sponsored" ad-label chip in mono).

## 5. Layout Principles
- Max-width 1120px centered container; sections `clamp(72px, 9vw, 120px)` vertical rhythm.
- Centered headline blocks (max 20ch) with 60ch subcopy — the reference's signature.
- Zig-zag two-column feature rows (text ↔ UI-mock card), alternating sides.
- Offer tiers: one wide lead card (free audit, butter surface) + two equal cards below — deliberately not a 3-equal-card row.
- Single-column collapse below 900px/560px; no horizontal scroll at 375px.

## 6. Motion & Interaction
- CSS-only: gentle float loop on the hero side cards, hover lift on cards/buttons, smooth scroll. All via transform/opacity. Everything gated behind `prefers-reduced-motion`.

## 7. Anti-Patterns (Banned)
- No emojis, no pure black, no neon/purple glows, no gradient headline text.
- No fabricated stats, logos, testimonials, or client names — factual numbers only ($3–5 CPC, $0 minimum, 48h audit). Testimonial section stays commented out until real.
- No OpenAI/ChatGPT logos or branding imitation; "Sponsored" chip motif only.
- No hype copy ("revolutionize / unlock / supercharge / elevate / seamless").
- No stock photos; UI mocks are pure HTML/CSS.
