# Project Plan: FOR BURAZ Landing Page

## Objective

Create and publish a landing page that presents the FOR BURAZ film project to:
1. **Private equity investors** — hook them with the business case, team credibility, revenue projections, and de-risk strategy
2. **Bosnian diaspora** — rally community support for crowdfunding (For Buraz Guild model)

The tone is cinematic and confident — a "fake press release" framing where we speak as if the film's success is inevitable, while being transparent that funding is being assembled now.

---

## Phases

### Phase 1: Research & Planning (COMPLETE)
- [x] Extract content from business plan
- [x] Research grassroots marketing models (Sound of Freedom, Passion of the Christ)
- [x] Research comparable film revenues (Anora, Minari, The Farewell)
- [x] Research cast IMDB profiles and credits
- [x] Research color palette (Quran green + Chinatown/Godfather noir)
- [x] Inventory design assets (fonts, Florida PNGs)
- [x] Create CLAUDE.md, project.md, styleguide.md

### Phase 2: Design System & Layout (NEXT)
- [ ] Finalize styleguide.md with user approval
- [ ] Define page layout / section order
- [ ] Define responsive breakpoints
- [ ] Identify all external assets needed (cast headshots, poster-style imagery)

### Phase 3: Build the Page
- [ ] Set up clean site directory structure
- [ ] Implement HTML structure with semantic sections
- [ ] Implement CSS design system (colors, typography, components)
- [ ] Build hero section
- [ ] Build logline / opportunity hook
- [ ] Build story section
- [ ] Build cast section (with photos, IMDB links, credits)
- [ ] Embed Vimeo sizzle reel
- [ ] Build comparable films / revenue analysis section
- [ ] Build financing & investment section
- [ ] Build team section
- [ ] Build contact / CTA section
- [ ] Responsive testing and polish

### Phase 4: Publish to GitHub
- [ ] Initialize git repository
- [ ] Create .gitignore (exclude .DS_Store, __MACOSX, etc.)
- [ ] Commit all site files
- [ ] Create GitHub repository (via `gh` CLI)
- [ ] Push to remote
- [ ] Enable GitHub Pages (from main branch, /site folder or root)
- [ ] Verify live URL works
- [ ] Share URL with user

---

## Page Layout (Proposed Section Order)

1. **Hero** — Title, genre, tagline, director credit. Full-viewport cinematic opening.
2. **The Hook** — "4 million Bosnians. No major film has told their story." Diaspora stats.
3. **The Story** — Synopsis from the business plan. Brief, evocative.
4. **Director's Statement** — Sabina's personal connection. Emotional anchor.
5. **Sizzle Reel** — Vimeo embed (`vimeo.com/sabinavajraca/forburazsizzle`). Placed after concept/cast intro.
6. **Cast** — Photo cards with IMDB links, role, and notable credits. Emile Hirsch featured prominently. Aspirational cast (Willa Fitzgerald, Joe Keery) presented as "in talks" or similar.
7. **Cinematographer** — Ula Pontikos highlight.
8. **Comparable Films** — Anora, Minari, The Farewell revenue analysis. Visual chart or table.
9. **The Opportunity** — Built-in audience, diaspora market dynamics, grassroots model (Sound of Freedom / Guild parallels).
10. **Revenue Projections** — Three-scenario table from business plan.
11. **Financing Structure** — How the film is being funded (PE + crowdfunding + pre-sales + incentives).
12. **The Team** — Sabina, Diane, Paul, Tea with bios and credibility markers.
13. **Script Recognition** — Festival accolades as badges/pills.
14. **Call to Action** — Contact info, investment inquiry, crowdfunding link placeholder.
15. **Footer** — Confidential notice, year.

---

## Content Sources

| Section | Source |
|---|---|
| Story, Cast, Team, Financials | `Business_Plan_For_Buraz.md` (do not alter source text) |
| Comparable film data | Research: Anora ($6M budget / $105M gross), Minari ($2M / $15M), The Farewell ($3.5M / $22.2M) |
| Marketing model | Research: Sound of Freedom (Angel Guild, pay-it-forward), Passion of the Christ (community gatekeepers, bulk tickets) |
| Cast IMDB links | Research: Hirsch nm0386472, Prica nm0697340, Fitzgerald nm5765981, Keery nm5462364, Pontikos nm1866498 |
| Sizzle reel | `https://vimeo.com/sabinavajraca/forburazsizzle` |
| Visual design | `styleguide.md`, `lookbook.pdf`, Florida PNGs, Morrison font |

---

## Confirmed Decisions

- **Cast headshots:** Pull from IMDB where possible; noir-styled placeholders as fallback.
- **Aspirational cast (Willa Fitzgerald, Joe Keery, big-name cameo):** Not emphasized. Only referenced in the revenue projections / comparables context.
- **For Buraz Guild:** Placeholder for now. Crowdfunding platform not yet established.
- **GitHub repo name:** `for-buraz` (recognizable).
- **Budget figure:** $2M USD, union production.
- **Domain:** GitHub Pages URL for now.
