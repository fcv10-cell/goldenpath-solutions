# GoldenPath Solutions — Website

Cinematic, professional marketing site for **GoldenPath Solutions**, a warehouse
staffing & recruitment company. Built with **Astro + Tailwind CSS v4**, featuring
a **liquid-glass** design system, full-bleed looping background videos, and
blur-in entrance animations — a dark, premium, space-travel-inspired aesthetic
grounded in the official GoldenPath brand (gold accents, warehouse footage).

## Brand

| Token | Hex | Role |
|-------|-----|------|
| Midnight Navy | `#0f172a` | Base background |
| Royal Workforce Blue | `#0017a0` | Depth / glow |
| Champagne Gold | `#c8a96b` | Primary accent |
| Golden Path Amber | `#a87900` | Accent gradient |
| Pure White | `#ffffff` | Contrast |

Headings use **Instrument Serif** (always italic), body uses **Barlow**. Tone:
professional, human, aspirational. The base is black with white liquid-glass
chrome and Champagne Gold (`#c8a96b`) accents.

## Tech stack

- [Astro](https://astro.build) 6 (static output)
- [Tailwind CSS](https://tailwindcss.com) v4 (via `@tailwindcss/vite`)
- Vanilla JS for the cinematic effects (no heavy animation libraries): word-by-word
  blur-in headlines, blur-in scroll reveals, a custom `FadingVideo` loop crossfade
  (rAF-driven), scroll-progress bar, and animated stat counters

## Project structure

```
src/
  layouts/Layout.astro      # HTML shell, fonts, all client scripts
  components/
    Nav.astro               # Liquid-glass pill nav + mobile menu (in Hero)
    Hero.astro              # Full-bleed video hero, glass badge/CTAs/stat cards
    Services.astro          # Full-bleed video "Capabilities" + 3 glass cards
    Stats.astro             # Glass stat strip with animated counters
    Process.astro           # 4-step glass cards
    Contact.astro           # CTA + contact form
    Footer.astro
  pages/index.astro         # Page assembly
  styles/global.css         # Design tokens + utilities
```

## Commands

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview the production build locally |

## Replacing placeholders

The site ships with tasteful placeholders so it looks finished out of the box.
Swap these for real brand assets:

- **Logo** — edit `src/components/Logo.astro` (replace the inline SVG mark/wordmark
  with the official logo file).
- **Hero photo** — replace the "Warehouse photo" placeholder block in
  `src/components/Hero.astro` with `<img src="/img/warehouse.jpg" … />` (put images
  in `public/img/`).
- **Partner logos** — update the `partners` array in `src/components/Marquee.astro`.
- **Copy & contact details** — email/phone in `src/components/Contact.astro`.
- **Contact form** — currently a front-end demo; wire it to a form backend
  (Formspree, Resend, an API route, etc.) for real submissions.
