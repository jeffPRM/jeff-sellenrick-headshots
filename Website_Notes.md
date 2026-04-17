# JSH Website — Build Notes & Decision Log
*Compiled from original Claude.ai project chat, March 2026*

---

## Current Status
**April 2026 update:** Major revision complete. See changelog below.

Single-file HTML build (`index.html`) is complete. All portfolio images now local (no Squarespace CDN). Contact form live via 17hats embed. Full SEO build-out done. GitHub-ready.

---

## April 2026 Changelog
- **Logo:** Nav logo increased to 84px desktop / 48px mobile
- **Hero image:** Changed to `../Portfolio/David2.jpg` (local)
- **Stat bar:** Removed from hero entirely
- **Services section:** Redesigned from 4 equal-weight grid cards → 3 full-width editorial rows (numbered, with teal vertical accent on hover). Cards merged: Corporate Headshots + Team & Office Photography → "Corporate & Team Headshots"
- **"Photography" → "Headshots"** in all service card titles
- **48hr references:** All removed (hero stat bar, How It Works, Individual section, About credentials)
- **Portfolio images:** All 10 switched from Squarespace CDN URLs → local Portfolio folder paths. Matt.jpg (not in local folder) → Alison.jpg; Jonathan_1.jpg → Guiliani_Anthony
- **About section:** "Professional Photographer" subtitle removed from Jeff's caption
- **About image:** Changed to local `../../Powder River Media/Data Dump/My Headshot/Jeff.jpg` — NOTE: this file needs to be included in GitHub repo or moved to Portfolio folder
- **Conference copy:** Removed "minimal footprint" → replaced with high-volume throughput language
- **Contact form:** 17hats iframe embedded as new section before Final CTA (id="contact")
- **SEO:** Meta description, OG tags, canonical URL, JSON-LD LocalBusiness schema markup added
- **Keywords added:** employee headshots, executive headshots, staff headshots, company headshots, consistent team headshots, convention headshot booth, LinkedIn headshots, Annapolis, Washington DC — all woven naturally into copy
- **Mobile:** Comprehensive responsive improvements across all sections
- **Footer:** Updated service link labels, updated tagline with keywords, copyright to 2026
- **Nav:** Added Contact link

---

## Tech Approach
- Single self-contained HTML file — no external dependencies except Google Fonts
- Logos embedded as base64 in `<head>`
- Portfolio images reference local paths: `../Portfolio/[filename].jpg`
- Jeff's about photo: `../../Powder River Media/Data Dump/My Headshot/Jeff.jpg` (needs to be in GitHub repo)
- Scroll-reveal animations via IntersectionObserver (fires on live site)
- **Hosted on GitHub Pages** at jeffsellenrickheadshots.com

---

## Typography
- **Headings:** Cormorant Garamond (refined serif)
- **Body:** DM Sans (clean sans-serif)
- Same pairing as Powder River Media — deliberate consistency across Jeff's brands

---

## Color System

### Block Colors (major section backgrounds)
| Section | Color |
|---|---|
| Hero | Teal `#0A3D3C` |
| Trusted By | Off-white `#F5F3EF` |
| Services | Charcoal `#1A1A1A` |
| Portfolio | Off-white `#F5F3EF` |
| How It Works | Charcoal `#1A1A1A` |
| Individual Headshots | Off-white `#F5F3EF` |
| About | Charcoal `#1A1A1A` |
| Testimonials | Teal `#0A3D3C` |
| Final CTA | Black `#111` |
| Footer | Charcoal `#1A1A1A` |

- Teal bookends the content (hero + testimonials) — roughly 15% of total page area
- Dark/light alternation runs cleanly from Trusted By onward
- Hero has a bottom-up gradient (dark near-black teal rising from the floor) — **no left-to-right gradient**

### Accent Colors
- **Orange `#C8541A`** — CTAs and buttons ONLY (Book a Session, Book Now, Book Headshots, etc.)
- **Teal `#2A7E7C`** (lighter teal) — structural/editorial accents: eyebrows, service card hover bars, feature dashes, quote marks, footer links

---

## Logo Integration
- **Horizontal wordmark** — nav bar (84px tall desktop / 48px mobile) and footer (48px tall)
- **Square JSH mark** — favicon + ghosted background accent in Final CTA section (4% opacity)
- Both logos embedded as base64 in `<head>` — no external logo files needed
- **Do not alter logos** — sizes and placements are set

---

## Real Content Pulled From Squarespace
- 10 portfolio photos (Elizabeth, Danielle, Matt, Pam, Fabien, Jonathan, David, Alice, Justin, and more)
- Jeff's headshot in About section
- Real testimonials verbatim: Lauren, Justin, Fabien, Allison, Jonathan
- Contact info: `info@jeffsellenrickheadshots.com` / `(240) 654-2145`
- Service descriptions including actor headshots and conference booth option
- Location copy: Baltimore, Central Maryland, Washington D.C., Annapolis, Nationwide
- About section uses Jeff's original Squarespace copy verbatim ("I'm Here to Help")

---

## Section Structure (in scroll order)
1. **Hero** — Teal bg, headline, subheadline, dual CTAs. Image: David2.jpg
2. **Trusted By** — Industry names in italic serif communicating organizational credibility
3. **Services** — 3 editorial rows: Corporate & Team Headshots | Conference & Event Headshot Booth | Individual Headshots
4. **Portfolio** — Asymmetric editorial grid, hover overlays with subject labels, all local images
5. **How It Works** — 4-step process: Schedule → Professional Setup → Guided Posing → Delivery
6. **Individual Headshots** — Dedicated solo booking section with feature checklist and CTA
7. **About** — Jeff's copy, portrait (local), location pills, credentials bar
8. **Testimonials** — Client quotes on teal background
9. **Contact** — 17hats form embed (id="contact") — primary conversion section
10. **Final CTA** — Black bg, ghosted JSH mark, dual CTAs
11. **Footer** — Charcoal, horizontal wordmark, organized link columns

---

## What's Still To Do
- [ ] **Jeff.jpg path**: Copy Jeff's headshot into the Portfolio folder (or repo root) and update the About section `src` path accordingly before deploying to GitHub
- [ ] Build separate landing pages: Corporate & Team Headshots page + Conference Headshot Booth page (two separate buyer audiences)
- [ ] Add Services dropdown to nav (Corporate & Team | Conference Booth) once landing pages are built
- [ ] Create standalone `contact.html` page (same 17hats form, same nav/footer) for direct linking
- [ ] Submit to Google Search Console once live on GitHub Pages
- [ ] Set up Google Business Profile with consistent name/services/location language
- [ ] Pricing page (TBD)
