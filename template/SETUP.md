# B2B Lead-Gen Template — Setup Guide

> Built from Cause72 / Omnia source. Two-page site: homepage + schedule call page.
> Layout standards encoded and verified. Est. time to customize a new client: **25–40 min**.

---

## Folder Structure

```
template/
  index.html             ← Homepage
  schedule-call.html     ← Schedule/booking page (v2: tall logo-only header)
  assets/
    logo/                ← Drop your logo here
  SETUP.md               ← This file
  TEMPLATE_STANDARDS.md  ← Layout rulebook (read if anything looks broken)
```

---

## Step 1 — Add the Logo

1. Place your logo file in `assets/logo/` (PNG with transparent background recommended)
2. Note the filename (e.g., `acme-logo.png`)

---

## Step 2 — Token Find & Replace

Open **both** `index.html` and `schedule-call.html` in your editor.  
Run **Find & Replace** (Ctrl+H / Cmd+H) for each token below.

> **Tip:** Search for `[` to jump between all remaining tokens after you finish.

### Brand Tokens (replace in BOTH files)

| Token | Replace With | Notes |
|---|---|---|
| `[BRAND_NAME]` | e.g. `AcmeLegal` | Company name |
| `[BRAND_TAGLINE]` | e.g. `Precision Leads for Trial Attorneys` | Short tagline — footer |
| `[LOGO_PATH]` | e.g. `acme-logo.png` | Filename only, must be in `assets/logo/` |
| `[YEAR]` | `2026` | Copyright year |
| `[NAV_CTA_LABEL]` | e.g. `Schedule Strategy Call` | Nav button + hero CTA + footer CTA |
| `[ACCENT_COLOR]` | e.g. `#0066ff` | Primary brand color |
| `[ACCENT_HOVER]` | e.g. `#0080ff` | Lighter variant for hovers |

> **Note on colors:** After replacing the token comments, also change the two hex values on the lines marked `/* [ACCENT_COLOR] */` and `/* [ACCENT_HOVER] */` in both files' `:root` block.

### Meta / SEO Tokens

| Token | Replace With |
|---|---|
| `[META_TITLE]` | e.g. `AcmeLegal \| High-Intent PI Leads` |
| `[META_DESC]` | Short page description (155 chars) |
| `[OG_TITLE]` | Same as META_TITLE usually |
| `[SCHEDULE_META_TITLE]` | e.g. `Schedule a Call — AcmeLegal` |
| `[SCHEDULE_META_DESC]` | Short schedule page description |

### Homepage Content Tokens (`index.html`)

| Token | Replace With |
|---|---|
| `[HERO_H1_WHITE]` | First (white) part of H1 |
| `[HERO_H1_ACCENT]` | Accent-colored last words of H1 |
| `[HERO_SUBTEXT]` | Hero paragraph below headline |
| `[HERO_SCARCITY_LINE]` | e.g. `Limited Partnerships Available` |
| `[VALUES_H2_WHITE]` | e.g. `Protecting Your Time.` |
| `[VALUES_H2_ACCENT]` | e.g. `Maximizing Case Value.` |
| `[VALUE_CARD_1_ICON]` | FA icon class e.g. `fa-brain` |
| `[VALUE_CARD_1_TITLE]` | Card 1 title |
| `[VALUE_CARD_1_BODY]` | Card 1 paragraph |
| `[VALUE_CARD_2_*]` | Same pattern for card 2 |
| `[VALUE_CARD_3_*]` | Same pattern for card 3 |
| `[PROCESS_H2_ACCENT]` | e.g. `Engineered` |
| `[PROCESS_H2_WHITE]` | e.g. `for Precision` |
| `[PROCESS_SUBTITLE]` | Process section subtitle line |
| `[STEP_1_ICON]` | FA icon e.g. `fa-cogs` |
| `[STEP_1_TITLE]` | Step 1 heading |
| `[STEP_1_BODY]` | Step 1 paragraph |
| `[STEP_2_*]` / `[STEP_3_*]` | Same pattern |
| `[PARTNERS_H2_WHITE]` | e.g. `Strategic Partnerships` |
| `[PARTNERS_H2_ACCENT]` | e.g. `Only` |
| `[PARTNERS_SUBTITLE]` | Partnerships section subtitle |
| `[PARTNER_CARD_1_ICON]` | FA icon e.g. `fa-chart-line` |
| `[PARTNER_CARD_1_TITLE]` | Partner card 1 title |
| `[PARTNER_CARD_1_BODY]` | Partner card 1 body |
| `[PARTNER_CARD_2_*]` / `[PARTNER_CARD_3_*]` | Same pattern |
| `[TRUST_QUOTE]` | Quote inside shield card |
| `[TRUST_H2_WHITE]` | Trust H2 first white phrase |
| `[TRUST_H2_ACCENT]` | Trust H2 first accent phrase |
| `[TRUST_H2_WHITE_2]` | Trust H2 second white phrase |
| `[TRUST_H2_ACCENT_2]` | Trust H2 second accent phrase |
| `[FINAL_CTA_H2_WHITE]` | e.g. `Ready to` |
| `[FINAL_CTA_H2_ACCENT]` | e.g. `Move Faster` |
| `[FINAL_CTA_SUBTITLE]` | CTA section subtext |
| `[CTA_BULLET_1]` / `[CTA_BULLET_2]` / `[CTA_BULLET_3]` | 3 short proof bullets |

### Schedule Page Tokens (`schedule-call.html`)

| Token | Replace With |
|---|---|
| `[SCHEDULE_H1_WHITE]` | e.g. `Schedule Your` |
| `[SCHEDULE_H1_ACCENT]` | e.g. `Qualification Call` |
| `[SCHEDULE_SUBTITLE]` | Paragraph connecting value to the call |
| `[BENEFIT_1_ICON]` | FA icon e.g. `fa-clock` |
| `[BENEFIT_1_TEXT]` | Bullet 1 text |
| `[BENEFIT_2_ICON]` → `[BENEFIT_5_*]` | Same pattern |
| `[SCARCITY_TITLE]` | e.g. `Limited Territories` |
| `[SCARCITY_BODY]` | e.g. `We partner with select firms in each market` |
| `[SCHEDULE_CALENDAR_BODY]` | Placeholder card body text |

---

## Step 3 — Embed the Calendar

In `schedule-call.html`, find the `<!-- CALENDAR EMBED -->` comment block and replace the `<div class="calendar-placeholder">` section with your embed code:

- **Calendly:** Use the `calendly-inline-widget` div + their script (code provided in comments)
- **Cal.com:** Use the `<cal-inline>` element + their embed script
- **HubSpot:** Use the `meetings-iframe-container` div + their script

---

## Step 4 — Verify (Pre-Launch Checklist)

- [ ] No `[TOKEN]` strings remain (search for `[` in both files)
- [ ] Logo displays correctly at 40px tall (header) and 60px tall (footer)  
- [ ] Accent color renders correctly in nav button, icons, and CTA buttons
- [ ] Calendar embed shows (not the placeholder card)
- [ ] Mobile layout wraps correctly at 900px and 768px
- [ ] `schedule-call` link in homepage nav resolves to the schedule page
- [ ] Footer copyright year is current

---

## Layout Rules (Quick Reference)

> Full details: see `TEMPLATE_STANDARDS.md`

| Rule | Do | Don't |
|---|---|---|
| Header height | Set via `padding` on `.header-inner` | Never `height` + `overflow:hidden` |
| Logo sizing (header) | `max-height: 40px` (homepage) or `72px` (schedule) | `width: XX%` |
| Logo sizing (footer) | `height: 60px` | `max-height` with wide logos |
| Main content padding | `6rem 5% 60px` (sticky header) | `104px` offset (only for fixed headers) |
| Section width | Wrap in `.section-inner` | Let content go edge-to-edge |

---

## Font Awesome Icon Reference

Need an icon? Browse at [fontawesome.com/icons](https://fontawesome.com/icons).  
Use the format `fa-icon-name` for the `[*_ICON]` tokens.

Common picks:
- `fa-brain` `fa-bullseye` `fa-network-wired` `fa-rocket` `fa-bolt`
- `fa-chart-line` `fa-gem` `fa-cogs` `fa-shield-alt` `fa-crosshairs`
- `fa-clock` `fa-users` `fa-clipboard-check` `fa-map-marker-alt`
