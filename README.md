# Bride Body Fitness — alternative site (pitch mockup)

Static one-pager. No build step. Open `index.html` or drop the folder on Vercel.

```bash
npx vercel deploy --prod
```

## What's here
- `index.html` — the whole site (CSS + JS inline)
- `assets/` — images pulled from the live site and re-compressed (668K total, down from ~8MB of PNGs)

## Before this goes live
1. **The form is a demo.** `#bookForm` prevents default and shows a confirmation. Wire it to
   Formspree / her CRM, or replace the whole card with a Calendly / Acuity embed.
2. **Placeholder legal links** in the footer point to `#`.
3. **Numbers are hard-coded** (50+, 5.0, 15+). Confirm them with Bree.
4. Swap `assets/hero.jpg` and `assets/founder.jpg` for higher-res originals if she has them.

## Notes
- Mobile-first. Hero copy sits on cream with the photo below it so the CTA lands above the
  fold on an iPhone, and the photo stays crisp instead of sitting under a wash.
- All type uses `clamp()`, so no headline can overflow the way "The Bride Body Bootcamp"
  currently does on her live site.
- Scroll reveals have a 4s safety net that force-shows anything still hidden, so content
  can never get stuck invisible.
