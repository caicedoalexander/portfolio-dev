# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Alexander Caicedo built with Astro 5 and Tailwind CSS 4. The site is a single-page application in Spanish showcasing professional experience, projects, and contact information.

## Development Commands

```bash
# Install dependencies
bun install

# Start dev server (localhost:4321)
bun dev

# Build for production
bun build

# Preview production build
bun preview

# Run Astro CLI commands
bun astro [command]
```

## Architecture

### Tech Stack
- **Framework**: Astro 5.16+ (SSG, ClientRouter for transitions)
- **Styling**: Tailwind CSS 4 (via Vite plugin, no config file needed)
- **Typography**:
  - Display: Syne Variable (@fontsource-variable/syne) - Bold, geometric
  - Body: Manrope Variable (@fontsource-variable/manrope) - Clean, readable
  - Mono: JetBrains Mono Variable (@fontsource-variable/jetbrains-mono)
- **Design System**: Swiss Modern Minimalism
- **Language**: Spanish (lang="es")

### Component Architecture

**Layout System:**
- `src/layouts/Layout.astro` - Base layout with Header, Footer, and global styles
  - Implements dark mode support (system preference)
  - Includes ViewTransitions for smooth page transitions
  - Defines radial gradient backgrounds (different for light/dark)
  - Sets global scroll behavior and font family

**Page Structure:**
- `src/pages/index.astro` - Single page with sections organized by SectionContainer
  - Hero section (no id)
  - Experience section (#experiencia)
  - Projects section (#proyectos)
  - About Me section (#sobre-mi)

**Key Components:**
- `Header.astro` - Fixed navigation with scroll-based animation
  - Contains navigation items array with smooth scroll anchors
  - Implements IntersectionObserver for active section highlighting
  - Custom blur/shadow animation on scroll (0-100px range)
- `Hero.astro` - Profile image, availability badge, intro text, social links
- `Experience.astro` - Renders EXPERIENCE array via ExperienceItem components
- `Projects.astro` - Renders PROJECTS array with images, tags, and links
- `SectionContainer.astro` - Wrapper for main content sections
- `TitleSection.astro` - Section headers with icons
- Icon components in `src/components/icons/` - SVG icons as Astro components

### Design System

**Color System (CSS Variables):**
- Primary: `--color-primary` (#3b82f6)
- Accent Energy: `--color-accent-energy` (#f59e0b) - Primary CTAs
- Accent Success: `--color-accent-success` (#10b981) - Skills/achievements
- Accent Creative: `--color-accent-creative` (#ec4899) - Projects
- Text: `--color-text`, `--color-text-secondary`
- Background: `--color-bg`, `--color-bg-elevated`
- Border: `--color-border`
- All colors adapt automatically to dark mode via `@media (prefers-color-scheme: dark)`

**Typography:**
- Headers use `var(--font-display)` (Syne) - Bold, geometric, tight tracking (-0.02em)
- Body uses `var(--font-body)` (Manrope) - Clean, readable
- Code uses `var(--font-mono)` (JetBrains Mono)

**Animations:**
- **Scroll Reveals**: `.reveal` class with stagger classes (`.stagger-1` through `.stagger-5`)
- **Micro-interactions**: Hover scale (1.05), active scale (0.95), color transitions
- **Header Animation**: Scroll-based blur/shadow (0-100px range)
- **Section Navigation**: IntersectionObserver highlights active nav items

**Layout:**
- Grid-based with Swiss precision
- Generous white space
- Color-coded sections (diagonal accent lines)
- Geometric backgrounds with subtle patterns

**Tailwind Usage:**
- No tailwind.config file - uses Tailwind 4's new @import system
- Global styles in `src/styles/global.css` imports Tailwind via `@import "tailwindcss"`
- CSS variables for theming
- Custom animations in Layout.astro global styles

### Data Management

Content is defined as arrays within components:
- `EXPERIENCE` array in `Experience.astro`
- `PROJECTS` array and `TAGS` object in `Projects.astro`
- `navItems` array in `Header.astro`

To update content, edit these arrays directly in the component files.

## Key Files

- `astro.config.mjs` - Astro config with Tailwind Vite plugin
- `src/layouts/Layout.astro` - Global layout and styles
- `src/pages/index.astro` - Main page structure
- `src/components/Header.astro` - Navigation with scroll effects
- `src/components/Hero.astro` - Hero section with profile
- `src/styles/global.css` - Tailwind import
- `public/` - Static assets (images, favicon)

## Important Notes

- Language is Spanish throughout the site
- No TypeScript strict mode (no tsconfig.json configuration)
- Uses Astro's ViewTransitions for SPA-like navigation
- Header uses scroll-based animations with animation-timeline
- Profile image: `/alexandercaicedo.jpeg`
- Contact email: a.caicedo.dev@gmail.com
