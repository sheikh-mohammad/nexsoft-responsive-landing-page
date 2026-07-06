# Eonix Landing Page — Project Constitution

**Date**: July 6, 2026
**Methodology**: Specification-Driven Development (SDD)
**Project**: Eonix — Real-time Website & API Monitoring SaaS Landing Page
**Developer**: Sheikh Mohammad — Full Stack Intern, Nexsoft Solutions

---

## Preamble

This constitution establishes the rules, principles, and workflows governing the development of the Eonix landing page. We follow **Specification-Driven Development (SDD)**: every piece of code must be preceded by a written specification, and every implementation must be verified against that specification before being accepted.

---

## Article I — Core Principles

### 1.1 Specification First, Code Second
No code shall be written without a corresponding specification. A specification must be reviewed and approved before implementation begins.

### 1.2 Traceability
Every implementation artifact (component, style, behavior) must trace back to a specification entry. Every specification entry must trace back to a requirements decision.

### 1.3 Verification
Each specification includes explicit acceptance criteria. Implementation is only complete when all acceptance criteria pass.

### 1.4 Single Source of Truth
Specifications are the authoritative reference. If code and specification disagree, the specification prevails and the code must be updated.

### 1.5 Progressive Refinement
Specifications are written top-down: requirements → feature specs → component specs → implementation specs. Each level adds detail.

---

## Article II — Specification Hierarchy

### Level 1: Requirements (docs/discovery-session.md)
Captures stakeholder decisions, goals, and constraints. Produced during the discovery phase.

### Level 2: Feature Specifications (docs/specs/features/)
One spec per major section or feature. Defines:
- Feature purpose and user value
- Content and copy
- Layout structure (mobile → tablet → desktop)
- Interactive behaviors and states
- Animation requirements
- Acceptance criteria

### Level 3: Component Specifications (docs/specs/components/)
One spec per reusable UI component. Defines:
- Props / TypeScript interface
- Visual variants (if any)
- State handling (loading, empty, error, active)
- Responsive breakpoint behavior
- Accessibility requirements
- Test criteria

### Level 4: Implementation Specifications (docs/specs/implementation/)
Technical specifications covering:
- Project structure and file organization
- CSS/styling conventions
- Animation implementation patterns
- SEO and metadata strategy
- Performance budgets

---

## Article III — Development Workflow

Every feature follows this 4-phase cycle:

### Phase 1: Specify
Write the specification document for the feature/component using the defined templates.
- Output: `.md` file in `docs/specs/`
- Review: Self-review against requirements

### Phase 2: Implement
Write code that fulfills the specification.
- Must follow project coding standards (Article V)
- Must handle all states defined in the spec
- Must be responsive across all breakpoints

### Phase 3: Verify
Check the implementation against every acceptance criterion in the spec.
- Visual verification (browser testing)
- Responsive verification (mobile, tablet, desktop)
- Interaction verification (animations, hover, click)
- Accessibility verification

### Phase 4: Commit
Commit only when all acceptance criteria pass.
- Commit message must reference the specification
- Working tree should be clean after commit

---

## Article IV — Specification Templates

### Feature Specification Template

```markdown
## Feature: [Name]

### Purpose
Why this feature exists and what user need it serves.

### Content
- Headline: [exact text]
- Subtext: [exact text]
- Visual elements: [description]

### Layout
- Mobile (< 768px): [description]
- Tablet (768-1024px): [description]
- Desktop (> 1024px): [description]

### Behaviors
- On load: [description]
- On hover: [description]
- On click: [description]
- On scroll: [description]

### States
- Default state
- Hover state
- Active/focus state
- Mobile state
- Dark/light mode

### Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
```

### Component Specification Template

```markdown
## Component: [Name]

### Interface
```typescript
interface Props {
  // prop definitions
}
```

### Variants
- [Variant 1]: [description]
- [Variant 2]: [description]

### States
- Default, Hover, Active, Disabled, Loading (as applicable)

### Responsive Behavior
- Breakpoint-specific changes

### Accessibility
- ARIA roles and attributes
- Keyboard navigation
- Focus management

### Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
```

---

## Article V — Coding Standards

### 5.1 Project Structure
```
nexsoft-responsive-landing-page/
├── docs/
│   ├── discovery-session.md
│   ├── AGENTS.md
│   └── specs/
│       ├── features/
│       ├── components/
│       └── implementation/
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── layout/        # Navbar, Footer, BackToTop
│   │   ├── sections/      # Hero, About, Services, etc.
│   │   └── ui/            # Button, Card, Accordion, etc.
│   ├── hooks/             # Custom React hooks
│   ├── lib/               # Utility functions
│   └── types/             # Shared TypeScript types
├── public/
│   └── images/
└── (config files)
```

### 5.2 Naming Conventions
- **Files**: PascalCase for components (`HeroSection.tsx`), camelCase for utilities (`useScrollReveal.ts`)
- **Components**: PascalCase
- **Functions**: camelCase
- **CSS classes**: Tailwind utility classes (preferred); custom classes only for complex animations
- **TypeScript interfaces**: PascalCase with `Props` suffix for component props (`HeroSectionProps`)

### 5.3 Component Standards
- Each section gets its own directory under `src/components/sections/`
- Shared UI components go under `src/components/ui/`
- Components are server components by default; client components are marked with `"use client"`
- Stateful logic extracted to custom hooks in `src/hooks/`

### 5.4 Styling Standards
- Tailwind CSS for all styling
- CSS variables for theming (dark/light mode) defined in `globals.css`
- No inline styles
- Consistent spacing using Tailwind's spacing scale
- Animations use Tailwind's transition/animation utilities + CSS keyframes for complex sequences

### 5.5 TypeScript Standards
- Strict mode enabled
- Explicit prop interfaces for all components
- No `any` types — use proper generics or `unknown`
- Export types from `src/types/` when shared across components

---

## Article VI — Theming System

### 6.1 Theme Variables
All colors are defined as CSS custom properties on `:root` and `.dark`:
- `--color-bg-primary`: Background
- `--color-bg-secondary`: Card/section backgrounds
- `--color-text-primary`: Primary text
- `--color-text-secondary`: Muted text
- `--color-accent`: Green accent
- `--color-accent-hover`: Accent hover state
- `--color-border`: Borders and dividers

### 6.2 Dark Mode (Default)
- Background: #1a1a1a (warm dark)
- Cards: Slightly lighter dark
- Text: White/light gray
- Accent: Green

### 6.3 Light Mode
- Background: White/off-white
- Cards: White with subtle shadow
- Text: Dark gray/near-black
- Accent: Same green (adjusted for contrast)

---

## Article VII — Quality Assurance

### 7.1 Responsive Breakpoints
| Breakpoint | Width | Target |
|---|---|---|
| Mobile | < 768px | Phones |
| Tablet | 768px - 1024px | Tablets, small laptops |
| Desktop | > 1024px | Large screens |

All sections must be verified at all three breakpoints.

### 7.2 Performance Budget
- Lighthouse Performance: ≥ 90
- Lighthouse Accessibility: ≥ 90
- Lighthouse SEO: ≥ 90
- Total page size (excluding images): < 300KB
- Time to Interactive: < 3s

### 7.3 Browser Support
- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)

---

## Article VIII — Commit Convention

### Format
```
<type>: <brief description>

<details if needed>

Spec: docs/specs/<path-to-spec>
```

### Types
- `spec` — New or updated specification
- `feat` — New feature implementation
- `fix` — Bug fix
- `style` — Styling changes only
- `refactor` — Code restructuring
- `docs` — Documentation changes

---

## Article IX — Enforcement

1. All PRs and commits must reference the relevant specification
2. Implementation without a prior specification shall be rejected
3. Code that fails to meet acceptance criteria shall be returned for revision
4. This constitution may be amended by consensus between developer and project lead

---

## Signatories

**Developer**: Sheikh Mohammad — Full Stack Intern, Nexsoft Solutions
**Date**: July 6, 2026
