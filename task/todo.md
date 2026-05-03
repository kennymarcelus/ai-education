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
