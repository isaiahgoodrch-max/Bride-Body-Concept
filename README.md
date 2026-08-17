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

## Copy
Bree's own wording throughout. Only changes: trimmed her bio to short paragraphs,
fixed "Unecessary" to "Unnecessary", and added the intro statement plus the FAQ,
which don't exist on the live site.

## Before this goes live
1. **The form is a demo.** `#bookForm` prevents default and shows a confirmation.
   Wire it to Formspree / her CRM, or swap the card for a Calendly / Acuity embed.
2. Footer legal links point to `#`.
3. Numbers are hard-coded (50+, 5/5, 15+). Confirm with Bree.
4. Swap `assets/` for higher-res originals if she has them. Everything here was
   pulled from the live site and recompressed.

## Deploy
```bash
npx vercel deploy --prod
```
