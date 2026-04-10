# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static landing page for **FOR BURAZ**, a neo-noir crime drama feature film set in the Bosnian immigrant community in Tampa Bay, Florida. The page targets two audiences: private equity investors and the Bosnian diaspora (for crowdfunding). It is not a software application — it is a single-page marketing site.

## Key Files

- `Business_Plan_For_Buraz.md` — Source of truth for all film content (cast, story, financials, team bios). Do not alter source text except for grammar corrections.
- `project.md` — Project plan and task tracking from research through GitHub Pages publish.
- `styleguide.md` — Design system: color palette, typography, components, layout specifications.
- `site/index.html` — The landing page (current draft exists, will be rebuilt).
- `design and assets/` — Source fonts (Morrison-Regular OTF, Avenir TTC) and Florida silhouette PNGs in 6 colors.
- `lookbook.pdf` — Visual reference for the film's look and feel. Requires `poppler` to render.

## Design Direction

The visual language blends **Chinatown/Godfather noir aesthetics** with **Islamic/Quran green** accents. See `styleguide.md` for the full color palette, typography rules, and component specs.

Key constraints:
- Morrison-Regular (OTF) for display/headlines — works in browsers via @font-face
- Avenir (TTC) does NOT work in browsers — use system font stack: `'Avenir', 'Avenir Next', 'Helvetica Neue', sans-serif`
- Florida silhouette PNGs are used as decorative background elements
- Sizzle reel embed: `https://vimeo.com/sabinavajraca/forburazsizzle`

## Content Rules

- **Never modify source text** from the business plan except for grammar fixes.
- Cast with signed attachment letters: Emile Hirsch, Julian Maroun, Alma Prica, Faketa Salihbegovic, Flora Diaz.
- Desired/aspirational cast (not yet attached): Willa Fitzgerald (Lea), Joe Keery (Armin), plus a big-name cameo for Duncan (Sean Penn, Ben Affleck, or Matt Damon).
- Cinematographer: Ula Pontikos.
- The film is NOT yet funded. The landing page's purpose is to attract investment. Do not state that funding is complete.

## Tech Stack

Static HTML/CSS site. No build tools, no JavaScript framework. Hosted via GitHub Pages.

## Visual QA with Playwright

**All design changes must be verified with screenshots using Playwright.**

After any HTML/CSS change, take a screenshot and review it before considering the work done. This catches layout issues, color mismatches, and responsive problems that aren't visible from code alone.

### Setup (one-time)
```bash
# Requires Node.js (v18+)
cd site && npm init -y && npm install playwright
npx playwright install chromium
```

### Taking Screenshots
```bash
# Full-page screenshot
npx playwright screenshot --full-page site/index.html site/screenshots/full-page.png

# Or use a script for multiple viewports:
node screenshot.js
```

### screenshot.js (in site/ directory)
```js
const { chromium } = require('playwright');
(async () => {
  const browser = await chromium.launch();
  const page = await browser.newPage();
  await page.goto('file://' + __dirname + '/index.html');

  // Desktop (1440px)
  await page.setViewportSize({ width: 1440, height: 900 });
  await page.screenshot({ path: 'screenshots/desktop.png', fullPage: true });

  // Tablet (768px)
  await page.setViewportSize({ width: 768, height: 1024 });
  await page.screenshot({ path: 'screenshots/tablet.png', fullPage: true });

  // Mobile (375px)
  await page.setViewportSize({ width: 375, height: 812 });
  await page.screenshot({ path: 'screenshots/mobile.png', fullPage: true });

  await browser.close();
})();
```

### Workflow
1. Make HTML/CSS changes
2. Run `node site/screenshot.js`
3. Review screenshots with the Read tool (they render as images)
4. Fix any issues found
5. Re-screenshot to confirm

Screenshots are saved to `site/screenshots/` and should be added to `.gitignore`.

## Deployment

- Repository will be published to GitHub and served via GitHub Pages.
- All assets must use relative paths from `site/` root.
- Font files and images go in `site/assets/`.
- `site/screenshots/` is for QA only — excluded from deployment via `.gitignore`.
