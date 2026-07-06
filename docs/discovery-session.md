# Discovery Session — Responsive Landing Page

**Date**: July 6, 2026
**Project**: Responsive Landing Page (Internship Project 2)
**Intern**: Sheikh Mohammad — Full Stack Intern at Nexsoft Solutions
**Session Type**: Requirements Discovery & Research

---

## Session Summary

Comprehensive discovery session covering all requirements for the responsive landing page. Starting from broad project context and drilling down into specific design, content, and technical decisions.

---

## Key Clarifications

1. **Purpose**: This is a **real production landing page** — not an internship exercise or a page for Nexsoft Solutions itself.
2. **Company**: The landing page is for **Eonix** — a real-time website & API monitoring SaaS startup. (Originally "Pulse" was considered but rejected due to name conflicts on social media.)
3. **Quality Bar**: Production-grade — SEO, performance, responsiveness, and polish all matter.

---

## Full Requirements

### Tech Stack
| Aspect | Decision |
|---|---|
| **Language** | TypeScript |
| **Framework** | Next.js 14+ (App Router) |
| **Styling** | Tailwind CSS |
| **Icons** | Lucide Icons |
| **Font** | Inter (clean, modern, SaaS-standard) |
| **Animations** | Tailwind CSS transitions + vanilla Intersection Observer (lightweight, no heavy libraries) |
| **Deployment** | Vercel |

### Design System
| Aspect | Decision |
|---|---|
| **Theme** | Dark & Sleek with warm dark background (#1a1a1a) |
| **Theme Toggle** | Yes — Dark + Light mode toggle in navbar |
| **Accent Color** | Neon / Lime Green (Claude picks optimal shade) |
| **Border Radius** | Mixed — sharp/clean cards with rounded buttons for contrast |
| **Typography** | Inter — Clean modern sans-serif |
| **Tone** | Professional & polished |
| **Visuals** | Mix of abstract shapes + dashboard mockup |
| **Page Width** | User to decide (1280px / 1440px / full-width) — TBD |

### Navigation
- **Type**: Sticky navbar (fixed on scroll)
- **Mobile**: Slide-in drawer menu
- **Navbar CTA**: User to decide (Start Free Trial / Get Started / none) — TBD
- **Items**: Links to all sections on the page

### Hero
- **Layout**: Centered text with animated background
- **CTA Buttons**: "Start Free Trial" (primary) + "See Pricing" (secondary)
- **Typed Text**: Mix of monitoring phrases + value propositions
- **Background**: Gradient or particle animation

### Sections
1. **Hero** — Centered headline, subtext, 2 CTAs, animated background, typed text effect
2. **About** — Company mission, 6 animated stat counters (company trust + technical mix, 3x2 grid)
3. **Services / Features** — Grid of feature cards: Uptime Monitoring, API Checks, Smart Alerts + integrations showcase (Slack, PagerDuty, Discord, Telegram, Webex, Email, SMS, Webhooks)
4. **Testimonials** — Featured quote on top + 5-card grid below (6 total)
5. **Portfolio / Capabilities** — 8+ use-case category cards (industries)
6. **Pricing** — 3-tier table: Free / Pro (highlighted as popular) / Enterprise with 10+ features per tier
7. **FAQ** — 10+ questions, accordion style (mix of general product + technical)
8. **Contact** — Email (TBD format), phone number, fictional office address
9. **Footer** — 5-column: Product + Resources + Company + Legal + Social. Social links: GitHub, Twitter/X, LinkedIn, YouTube, Discord (placeholder URLs). Newsletter signup in footer.

### Animations & Interactivity
- Scroll-triggered fade-in/slide-up reveals (Intersection Observer)
- Staggered card animations on Services, Pricing, Testimonials
- Typed text effect in hero
- Animated counters in stats section
- Gradient background animation in hero
- Smooth hover effects on all interactive elements
- Back-to-top button
- Smooth scroll navigation
- **Page load**: Branded splash loader (Eonix logo animation)

### Extras
- **Cookie consent**: Yes — GDPR-style banner
- **Newsletter**: Yes — email signup in footer
- **Link behavior**: Same tab (all links)

### Content
- All content AI-generated (realistic SaaS copy for Eonix)
- FAQ: 10+ questions, mix of general product and technical
- Pricing: 3 tiers with 10+ features each, Pro highlighted
- Stats: 6 stats — mix of company credibility + technical metrics
- Testimonials: 6 total (1 featured + 5 grid)
- Use-case categories: 8+ industries

### Technical Requirements
- Fully responsive (mobile, tablet, desktop)
- SEO-friendly (meta tags, semantic HTML)
- Performance optimized (lazy loads, optimized images, minimal JS)
- Clean, well-organized codebase with reusable components

### Timeline
- Complete within the week (week of July 6, 2026)

---

## Complete Decisions Log

| # | Question | Decision |
|---|---|---|
| 1 | Purpose of landing page? | Both — internship evaluation & real production page |
| 2 | What does Nexsoft do? (context) | Software Development |
| 3 | Tech stack freedom? | MERN & Next.js expected |
| 4 | Design vibe? | Dark & Sleek |
| 5 | Color scheme? | Dark with accent color |
| 6 | Sections beyond core 3? | All possible sections |
| 7 | Accent color? | Green / Lime |
| 8 | Animation level? | Heavy / Premium |
| 9 | Content source? | Generate everything (AI) |
| 10 | Next.js router? | App Router (default modern choice) |
| 11 | Icon library? | Lucide Icons |
| 12 | Contact form? | No form — just display info |
| 13 | Deployment? | Vercel |
| 14 | Company identity? | Startup / new brand (created for project) |
| 15 | Brand assets? | Claude decides company name and brand |
| 16 | Selected startup? | Pulse → **Eonix** (Pulse had name conflicts) |
| 17 | Footer links? | All working, multi-section footer |
| 18 | Timeline? | This week |
| 19 | Hero message angle? | Full-platform focus |
| 20 | Pricing tiers? | 3 tiers: Free / Pro / Enterprise |
| 21 | Core features? | Uptime + API + Alerts |
| 22 | About stats? | Mix of company + technical stats |
| 23 | Navigation style? | Sticky navbar |
| 24 | Visuals / imagery? | Mix of shapes + dashboard mockup |
| 25 | Theme toggle? | Yes — Dark + Light toggle |
| 26 | Social links? | All major platforms (GitHub, Twitter/X, LinkedIn, YouTube, Discord) |
| 27 | Contact details? | Full: email, phone, address |
| 28 | FAQ topics? | Mix: general product + technical |
| 29 | Portfolio style? | Use-case categories |
| 30 | Font? | Inter |
| 31 | Language? | TypeScript |
| 32 | Border radius style? | Mixed (sharp cards + rounded buttons) |
| 33 | Hero layout? | Centered text + animated BG |
| 34 | Pricing highlight? | Yes — Pro tier highlighted as popular |
| 35 | Animation library? | Tailwind CSS + vanilla Intersection Observer (lightweight) |
| 36 | Mobile menu? | Slide-in drawer |
| 37 | Pricing detail depth? | 10+ features per tier |
| 38 | Testimonials layout? | Featured + grid (6 total) |
| 39 | FAQ count? | 10+ questions |
| 40 | Portfolio categories? | 8+ industries |
| 41 | Copy tone? | Professional & polished |
| 42 | Typed text content? | Mix: monitoring phrases + value props |
| 43 | Cookie consent? | Yes — GDPR-style banner |
| 44 | Newsletter? | Yes — email signup in footer |
| 45 | Page load animation? | Branded splash loader |
| 46 | Link behavior? | Same tab |
| 47 | CTA buttons (hero)? | "Start Free Trial" + "See Pricing" |
| 48 | Testimonial count? | 6 (1 featured + 5 grid) |
| 49 | About stats count? | 6 stats (3x2 grid) |
| 50 | Integrations to showcase? | Full: Slack, PagerDuty, Discord, Telegram, Webex, Email, SMS, Webhooks |
| 51 | Dark background shade? | Warm dark: #1a1a1a |
| 52 | Footer structure? | 5-column: Product + Resources + Company + Legal + Social |
| 53 | Social URL format? | Placeholder (github.com/eonix, etc.) |
| 54 | Brand name final? | **Eonix** (replaced "Pulse") |
