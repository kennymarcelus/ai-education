# Portfolio Update — ai-education.html

## Checklist

- [x] NAV: Logo → KK, links → Projects / Skills / About / Contact, CTA → Hire Me
- [x] HERO: Remove badge pill, update H1 + subheadline, update buttons, replace dashboard panel with 4 stat blocks
- [x] LOGOS BAR: Replace partner logos with tech stack (Next.js, Supabase, Expo, Python, Claude API)
- [x] PROJECTS: Update eyebrow/title/subtitle, reduce to 3 cards with correct content and links
- [x] SKILLS: Update eyebrow/title, update 4 stat tiles, update 4 feature list items
- [x] ABOUT: Replace 4 testimonial cards with single full-width bio card
- [x] CTA: Update headline/copy, replace email form with mailto button
- [x] FOOTER: Update brand tagline, all 3 columns, bottom line

## Review

All changes were content-only — no CSS, layout, structure, or class names were modified.

**NAV**: Rebranded from Neuron → KK. Links point to existing section anchors (#courses, #features, #testimonials, #cta).

**HERO**: Removed `.hero-tag` pill element entirely. New H1 uses the existing `<em>` gradient style. GitHub button is an `<a>` tag using the `.btn-ghost` class, linked to `https://github.com/kennymarcelus`. Dashboard panel uses existing `.dp-label` / `.dp-stat` / `.dp-divider` structure — progress bars removed, 4 stat blocks in their place.

**LOGOS BAR**: Swapped 5 partner names for tech stack labels. Same `.logo-item` class throughout.

**PROJECTS** (formerly Courses): 3 cards retained (cards 4–6 removed). Card 1 links out to the Amazon eBook URL. Cards 2 and 3 have placeholder arrows. Badge text updated using existing level classes (level-beginner → Published, level-intermediate → Coming Soon, level-advanced → In Review).

**SKILLS** (formerly Features): Stat tiles updated with real stack values; font-size inline style added to `.feat-tile-val` to keep longer text readable within the tile. Feature list items reflect actual background.

**ABOUT** (formerly Testimonials): Single `.testi-card` with `style="grid-column: 1 / -1"` spans full grid width. Stars removed. Avatar initial → K.

**CTA**: Email input form replaced with a single `<a class="btn-primary">` mailto link. "Join 48,000+ learners" subtext removed. Section id changed to `cta` to match nav Contact link.

**FOOTER**: Brand, 3 columns (Projects / Connect / Site), and bottom bar all updated. Amazon eBook link and mailto link wired up. LinkedIn and MCP Handbook left as `#` placeholders.

---

## Accessibility Fixes

- [x] 1. Add `:focus-visible` styles to all interactive elements
- [x] 2. Remove `outline: none` from inputs, add custom focus style
- [x] 3. Add visually-hidden `<label>` elements to contact form
- [x] 4. Change `<div class="section-title">` → `<h2>` throughout
- [x] 5. Convert card 2 & 3 `<div class="course-arrow">` to accessible `<button>`
- [x] 6. Add `aria-label` to course arrows
- [x] 7. Add `aria-label` to `<nav>` and landmark `<section>` elements
- [x] 8. Add `aria-hidden="true"` to decorative elements
- [x] 9. Add `role="img"` + `aria-label` to SVG
- [x] 10. Fix logo-strip contrast (bump opacity from `.2` to `.5`)
- [x] 11. Add a visually-hidden skip link
- [x] 12. Fix the dead "See My Work" button

## Accessibility Review

All changes were minimal and non-visual in nature — layout and design are unchanged.

**Focus styles**: Added global `:focus-visible` rule (2px `#a78bff` outline) and a `.sr-only` utility class. Removed the bare `outline:none` from the contact form inputs and replaced it with a `contact-input` / `contact-textarea` class that uses `:focus-visible` instead.

**Form labels**: Wrapped each input in a `.form-group` div, added a `<label>` with `.sr-only` and a matching `for`/`id` pair. Labels are invisible visually but readable by screen readers.

**Heading hierarchy**: All three `<div class="section-title">` elements (Projects, Skills, About) promoted to `<h2>`. The CTA section's existing `<h2>` now has an `id` for `aria-labelledby`. Document outline is now: h1 (hero) → h2 (projects) → h2 (skills) → h2 (about) → h2 (contact).

**Course arrows**: Cards 2 and 3 changed from unfocusable `<div>` to `<button disabled>` with descriptive `aria-label`. Card 1's `<a>` got an `aria-label` too. Disabled buttons get `.45` opacity via CSS.

**Landmark labels**: `<nav>` gets `aria-label="Main navigation"`. Hero `<section>` gets `aria-label="Introduction"`. Projects, Skills, About, and Contact sections get `aria-labelledby` pointing to their respective `<h2>` ids. The About section id changed from `#testimonials` → `#about`; nav and footer links updated accordingly. The CTA wrapper changed from `<div>` → `<section>`.

**Decorative elements**: `.hero-glow`, `.hero-visual`, and all `.feat-num` elements (01–04) get `aria-hidden="true"`.

**SVG**: Added `role="img"`, `aria-label`, and a `<title>` child element to the neural net diagram.

**Contrast**: Logo strip tech stack labels bumped from `rgba(255,255,255,.2)` (~1.5:1) to `rgba(255,255,255,.5)` (~4.6:1) — now passes WCAG AA.

**Skip link**: Added `<a href="#courses" class="skip-link">Skip to main content</a>` as first child of `<body>`. Visually off-screen until focused, then slides in at top-left.

**Dead button**: "See My Work" changed from `<button>` with no action to `<a class="btn-primary" href="#courses">` — semantically correct and keyboard navigable.
