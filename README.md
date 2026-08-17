# Bride Body Fitness — concept site

Static one-pager. No build step. Deploys as-is.

## Structure
Follows her live site's order, with an intro beat added after the hero.

Hero → "Your wedding day is coming" → stats → How It Works (4 steps) → Meet Bree →
pull quote → transformations carousel → testimonial marquee → what's included →
FAQ → booking form → Instagram → footer

## What moves
- Hero photo: slow Ken Burns drift (26s)
- Transformations: swipeable snap carousel, arrows on desktop
- Testimonials: auto-scrolling marquee, pauses on hover
- Stat counters: count up on scroll into view
- Scroll reveals with staggered delays

All of it respects `prefers-reduced-motion`. The reveals have a 4.5s timeout that
force-shows anything still hidden, and the stat counters have their final value in
the HTML already, so a JS failure leaves the correct numbers on screen rather than
zeroes.

## Transformations
The six carousel slides use the real case studies from her `/transformations` page:
name, age, program length, and outcome, each mapped to that bride's actual photo.
Two extra homepage photos with no case study attached were dropped.

## Copy
Bree's own wording throughout. Only changes: trimmed her bio to short paragraphs,
fixed "Unecessary" to "Unnecessary", and added the intro statement plus the FAQ,
which don't exist on the live site.

## Before this goes live
1. **The form is a demo.** `#bookForm` prevents default and shows a confirmation.
   Wire it to Formspree / her CRM, or swap the card for a Calendly / Acuity embed.
2. Footer legal links point to `#`.
3. **Client count is 50+**, which is the only figure published anywhere on her site
   (homepage stats and the transformations page both say it). If Bree confirms a
   higher real number, it lives in exactly three places in `index.html`:
   the hero trust line, the stats block (`data-to` plus the visible text), and the
   testimonials lede. Round down, not up.
4. "15+ years" conflicts with "over a decade" in her live bio. Confirm which is right.
5. Swap `assets/` for higher-res originals if she has them. Everything here was
   pulled from the live site and recompressed.

## Deploy
```bash
npx vercel deploy --prod
```
