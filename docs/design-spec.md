# Portfolio Homepage Design Specification

## Overview

This document outlines a modern, professional visual design system for Mohammed Babelly's portfolio homepage. The design emphasizes clean aesthetics, subtle animations, and a cohesive color palette suitable for a software engineer specializing in backend, cloud, and DevOps.

---

## 1. Color Palette

### Primary Colors

| Name | Hex Code | Usage |
|------|----------|-------|
| **Primary** | `#0F172A` | Main text, headings, dark backgrounds |
| **Primary Light** | `#1E293B` | Secondary dark elements, cards |
| **Primary Lighter** | `#334155` | Tertiary elements, borders |

### Accent Colors

| Name | Hex Code | Usage |
|------|----------|-------|
| **Accent** | `#3B82F6` | Links, buttons, highlights |
| **Accent Hover** | `#2563EB` | Hover states for accent elements |
| **Accent Light** | `#DBEAFE` | Light accent backgrounds, badges |
| **Accent Glow** | `rgba(59, 130, 246, 0.15)` | Subtle glow effects |

### Secondary Accent - Gradient Support

| Name | Hex Code | Usage |
|------|----------|-------|
| **Gradient Start** | `#3B82F6` | Gradient beginning - blue |
| **Gradient End** | `#8B5CF6` | Gradient ending - purple |

### Neutral Colors

| Name | Hex Code | Usage |
|------|----------|-------|
| **Background** | `#FFFFFF` | Main page background |
| **Background Alt** | `#F8FAFC` | Alternate section backgrounds |
| **Background Card** | `#FFFFFF` | Card backgrounds |
| **Surface** | `#F1F5F9` | Input backgrounds, subtle surfaces |
| **Border** | `#E2E8F0` | Borders, dividers |
| **Border Light** | `#F1F5F9` | Subtle borders |

### Text Colors

| Name | Hex Code | Usage |
|------|----------|-------|
| **Text Primary** | `#0F172A` | Headings, important text |
| **Text Secondary** | `#475569` | Body text, paragraphs |
| **Text Muted** | `#64748B` | Captions, metadata |
| **Text Light** | `#94A3B8` | Placeholder text, disabled |

### Semantic Colors

| Name | Hex Code | Usage |
|------|----------|-------|
| **Success** | `#10B981` | Success states, positive indicators |
| **Warning** | `#F59E0B` | Warning states |
| **Error** | `#EF4444` | Error states |

### CSS Variables Definition

```css
:root {
  /* Primary */
  --color-primary: #0F172A;
  --color-primary-light: #1E293B;
  --color-primary-lighter: #334155;
  
  /* Accent */
  --color-accent: #3B82F6;
  --color-accent-hover: #2563EB;
  --color-accent-light: #DBEAFE;
  --color-accent-glow: rgba(59, 130, 246, 0.15);
  
  /* Gradient */
  --gradient-primary: linear-gradient(135deg, #3B82F6 0%, #8B5CF6 100%);
  --gradient-text: linear-gradient(135deg, #3B82F6 0%, #8B5CF6 100%);
  
  /* Background */
  --color-bg: #FFFFFF;
  --color-bg-alt: #F8FAFC;
  --color-bg-card: #FFFFFF;
  --color-surface: #F1F5F9;
  
  /* Border */
  --color-border: #E2E8F0;
  --color-border-light: #F1F5F9;
  
  /* Text */
  --color-text-primary: #0F172A;
  --color-text-secondary: #475569;
  --color-text-muted: #64748B;
  --color-text-light: #94A3B8;
  
  /* Semantic */
  --color-success: #10B981;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  
  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  --shadow-glow: 0 0 20px var(--color-accent-glow);
}
```

---

## 2. Typography

### Font Family

Keep the existing **Atkinson Hyperlegible** font - it's excellent for accessibility and readability. Consider adding a monospace font for code-related elements.

```css
:root {
  --font-sans: 'Atkinson', system-ui, -apple-system, sans-serif;
  --font-mono: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;
}
```

### Type Scale

Using a modular scale with ratio 1.25 - Major Third

| Element | Size | Weight | Line Height | Letter Spacing |
|---------|------|--------|-------------|----------------|
| **Display** | `4rem` / 64px | 700 | 1.1 | -0.02em |
| **H1** | `3rem` / 48px | 700 | 1.2 | -0.02em |
| **H2** | `2.25rem` / 36px | 700 | 1.25 | -0.01em |
| **H3** | `1.5rem` / 24px | 600 | 1.3 | 0 |
| **H4** | `1.25rem` / 20px | 600 | 1.4 | 0 |
| **Body Large** | `1.125rem` / 18px | 400 | 1.7 | 0 |
| **Body** | `1rem` / 16px | 400 | 1.7 | 0 |
| **Body Small** | `0.875rem` / 14px | 400 | 1.6 | 0 |
| **Caption** | `0.75rem` / 12px | 400 | 1.5 | 0.01em |

### CSS Variables for Typography

```css
:root {
  /* Font Sizes */
  --text-display: 4rem;
  --text-h1: 3rem;
  --text-h2: 2.25rem;
  --text-h3: 1.5rem;
  --text-h4: 1.25rem;
  --text-body-lg: 1.125rem;
  --text-body: 1rem;
  --text-body-sm: 0.875rem;
  --text-caption: 0.75rem;
  
  /* Font Weights */
  --font-normal: 400;
  --font-medium: 500;
  --font-semibold: 600;
  --font-bold: 700;
  
  /* Line Heights */
  --leading-tight: 1.1;
  --leading-snug: 1.25;
  --leading-normal: 1.5;
  --leading-relaxed: 1.7;
}
```

### Responsive Typography

```css
/* Mobile - base 16px */
@media (max-width: 640px) {
  :root {
    --text-display: 2.5rem;
    --text-h1: 2rem;
    --text-h2: 1.75rem;
    --text-h3: 1.25rem;
  }
}

/* Tablet */
@media (min-width: 641px) and (max-width: 1024px) {
  :root {
    --text-display: 3rem;
    --text-h1: 2.5rem;
    --text-h2: 2rem;
    --text-h3: 1.375rem;
  }
}
```

---

## 3. Spacing System

Using an 8px base unit for consistent spacing.

### Spacing Scale

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `0.25rem` / 4px | Tight spacing, icon gaps |
| `--space-2` | `0.5rem` / 8px | Small gaps, inline spacing |
| `--space-3` | `0.75rem` / 12px | Button padding, small margins |
| `--space-4` | `1rem` / 16px | Standard padding, list gaps |
| `--space-5` | `1.25rem` / 20px | Medium spacing |
| `--space-6` | `1.5rem` / 24px | Section padding |
| `--space-8` | `2rem` / 32px | Large gaps |
| `--space-10` | `2.5rem` / 40px | Section margins |
| `--space-12` | `3rem` / 48px | Large section spacing |
| `--space-16` | `4rem` / 64px | Hero padding |
| `--space-20` | `5rem` / 80px | Major section breaks |
| `--space-24` | `6rem` / 96px | Page-level spacing |

### CSS Variables

```css
:root {
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;
}
```

### Container Widths

```css
:root {
  --container-sm: 640px;
  --container-md: 768px;
  --container-lg: 1024px;
  --container-xl: 1280px;
  --container-content: 720px; /* For readable content */
}
```

---

## 4. Animation Specifications

### Timing Functions

```css
:root {
  /* Easing curves */
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);
  
  /* Durations */
  --duration-fast: 150ms;
  --duration-normal: 300ms;
  --duration-slow: 500ms;
  --duration-slower: 700ms;
}
```

### Hover Effects

#### Links
```css
a {
  color: var(--color-accent);
  text-decoration: none;
  transition: color var(--duration-fast) var(--ease-out);
}

a:hover {
  color: var(--color-accent-hover);
}

/* Underline animation */
.link-animated {
  position: relative;
}

.link-animated::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--gradient-primary);
  transition: width var(--duration-normal) var(--ease-out);
}

.link-animated:hover::after {
  width: 100%;
}
```

#### Buttons
```css
.btn {
  transition: all var(--duration-normal) var(--ease-out);
  transform: translateY(0);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.btn:active {
  transform: translateY(0);
}
```

#### Cards
```css
.card {
  transition: all var(--duration-normal) var(--ease-out);
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-xl);
}
```

### Scroll Animations

Using CSS animations triggered by scroll - can be implemented with Intersection Observer or CSS scroll-driven animations.

#### Fade In Up
```css
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fadeInUp var(--duration-slow) var(--ease-out) forwards;
}
```

#### Fade In
```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animate-fade-in {
  animation: fadeIn var(--duration-normal) var(--ease-out) forwards;
}
```

#### Scale In
```css
@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.animate-scale-in {
  animation: scaleIn var(--duration-normal) var(--ease-out) forwards;
}
```

#### Staggered Children Animation
```css
.stagger-children > * {
  opacity: 0;
  animation: fadeInUp var(--duration-slow) var(--ease-out) forwards;
}

.stagger-children > *:nth-child(1) { animation-delay: 0ms; }
.stagger-children > *:nth-child(2) { animation-delay: 100ms; }
.stagger-children > *:nth-child(3) { animation-delay: 200ms; }
.stagger-children > *:nth-child(4) { animation-delay: 300ms; }
.stagger-children > *:nth-child(5) { animation-delay: 400ms; }
```

### Hero Section Animations

```css
/* Gradient text animation */
.gradient-text {
  background: var(--gradient-text);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Subtle floating animation for decorative elements */
@keyframes float {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

/* Pulse glow effect */
@keyframes pulseGlow {
  0%, 100% {
    box-shadow: 0 0 20px var(--color-accent-glow);
  }
  50% {
    box-shadow: 0 0 40px var(--color-accent-glow);
  }
}
```

### Reduced Motion Support

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 5. Component Styling Guidelines

### Header

```css
.header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--color-border-light);
  padding: var(--space-4) var(--space-6);
  transition: all var(--duration-normal) var(--ease-out);
}

.header-scrolled {
  box-shadow: var(--shadow-sm);
}

.nav-link {
  position: relative;
  padding: var(--space-2) var(--space-3);
  color: var(--color-text-secondary);
  font-weight: var(--font-medium);
  transition: color var(--duration-fast) var(--ease-out);
}

.nav-link:hover,
.nav-link.active {
  color: var(--color-accent);
}

.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: var(--space-3);
  right: var(--space-3);
  height: 2px;
  background: var(--gradient-primary);
  border-radius: 1px;
}
```

### Hero Section

```css
.hero {
  text-align: center;
  padding: var(--space-24) var(--space-6) var(--space-16);
  position: relative;
  overflow: hidden;
}

/* Optional: Subtle gradient background */
.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  max-width: 800px;
  height: 400px;
  background: radial-gradient(
    ellipse at center,
    var(--color-accent-glow) 0%,
    transparent 70%
  );
  pointer-events: none;
  z-index: -1;
}

.hero-title {
  font-size: var(--text-display);
  font-weight: var(--font-bold);
  color: var(--color-text-primary);
  margin-bottom: var(--space-4);
  letter-spacing: -0.02em;
}

.hero-subtitle {
  font-size: var(--text-h3);
  font-weight: var(--font-semibold);
  color: var(--color-text-secondary);
  margin-bottom: var(--space-3);
}

.hero-tagline {
  font-size: var(--text-body-lg);
  color: var(--color-text-muted);
  max-width: 600px;
  margin: 0 auto;
}
```

### Section Styling

```css
.section {
  padding: var(--space-16) var(--space-6);
  max-width: var(--container-content);
  margin: 0 auto;
}

/* Alternate background for visual rhythm */
.section-alt {
  background: var(--color-bg-alt);
  padding: var(--space-16) var(--space-6);
  margin: 0 calc(-50vw + 50%);
  padding-left: calc(50vw - 50%);
  padding-right: calc(50vw - 50%);
}

.section-title {
  font-size: var(--text-h2);
  font-weight: var(--font-bold);
  color: var(--color-text-primary);
  margin-bottom: var(--space-8);
  position: relative;
}

/* Optional: Accent line under section titles */
.section-title::after {
  content: '';
  display: block;
  width: 60px;
  height: 4px;
  background: var(--gradient-primary);
  border-radius: 2px;
  margin-top: var(--space-4);
}

/* Centered title variant */
.section-title-center {
  text-align: center;
}

.section-title-center::after {
  margin-left: auto;
  margin-right: auto;
}
```

### Skills Section - Card Grid

```css
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: var(--space-6);
}

.skill-card {
  background: var(--color-bg-card);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  padding: var(--space-6);
  transition: all var(--duration-normal) var(--ease-out);
}

.skill-card:hover {
  border-color: var(--color-accent);
  box-shadow: var(--shadow-lg), 0 0 0 1px var(--color-accent-glow);
  transform: translateY(-2px);
}

.skill-card-title {
  font-size: var(--text-h4);
  font-weight: var(--font-semibold);
  color: var(--color-text-primary);
  margin-bottom: var(--space-3);
  display: flex;
  align-items: center;
  gap: var(--space-3);
}

.skill-card-title::before {
  content: '';
  width: 8px;
  height: 8px;
  background: var(--gradient-primary);
  border-radius: 50%;
}

.skill-card-content {
  color: var(--color-text-secondary);
  font-size: var(--text-body);
}
```

### Talks Section - Timeline Style

```css
.talks-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.talk-item {
  position: relative;
  padding-left: var(--space-8);
  padding-bottom: var(--space-6);
  border-left: 2px solid var(--color-border);
}

.talk-item:last-child {
  padding-bottom: 0;
}

.talk-item::before {
  content: '';
  position: absolute;
  left: -6px;
  top: 6px;
  width: 10px;
  height: 10px;
  background: var(--color-bg);
  border: 2px solid var(--color-accent);
  border-radius: 50%;
  transition: all var(--duration-fast) var(--ease-out);
}

.talk-item:hover::before {
  background: var(--color-accent);
  box-shadow: 0 0 0 4px var(--color-accent-glow);
}

.talk-title {
  font-weight: var(--font-semibold);
  color: var(--color-text-primary);
  margin-bottom: var(--space-2);
}

.talk-description {
  color: var(--color-text-secondary);
  font-size: var(--text-body-sm);
}
```

### Content Section - Cards

```css
.content-card {
  background: var(--color-bg-card);
  border: 1px solid var(--color-border);
  border-radius: 16px;
  padding: var(--space-8);
  margin-bottom: var(--space-6);
  transition: all var(--duration-normal) var(--ease-out);
}

.content-card:hover {
  box-shadow: var(--shadow-lg);
}

.content-card-header {
  display: flex;
  align-items: center;
  gap: var(--space-4);
  margin-bottom: var(--space-4);
}

.content-card-icon {
  width: 48px;
  height: 48px;
  background: var(--color-accent-light);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--color-accent);
}

.content-card-title {
  font-size: var(--text-h3);
  font-weight: var(--font-semibold);
  color: var(--color-text-primary);
}
```

### Connect Section

```css
.connect-section {
  text-align: center;
  padding: var(--space-20) var(--space-6);
  background: var(--color-bg-alt);
}

.social-links {
  display: flex;
  justify-content: center;
  gap: var(--space-4);
  margin-top: var(--space-8);
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 48px;
  height: 48px;
  background: var(--color-bg-card);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  color: var(--color-text-secondary);
  transition: all var(--duration-normal) var(--ease-out);
}

.social-link:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  color: white;
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

/* Alternative: Pill-style links with text */
.social-link-pill {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-3) var(--space-5);
  background: var(--color-bg-card);
  border: 1px solid var(--color-border);
  border-radius: 9999px;
  color: var(--color-text-secondary);
  font-weight: var(--font-medium);
  transition: all var(--duration-normal) var(--ease-out);
}

.social-link-pill:hover {
  background: var(--color-accent);
  border-color: var(--color-accent);
  color: white;
}
```

### Footer

```css
.footer {
  padding: var(--space-12) var(--space-6);
  background: var(--color-primary);
  color: var(--color-text-light);
  text-align: center;
}

.footer a {
  color: var(--color-text-light);
  transition: color var(--duration-fast) var(--ease-out);
}

.footer a:hover {
  color: white;
}

.footer-social {
  display: flex;
  justify-content: center;
  gap: var(--space-4);
  margin-top: var(--space-6);
}

.footer-social a {
  opacity: 0.7;
  transition: opacity var(--duration-fast) var(--ease-out);
}

.footer-social a:hover {
  opacity: 1;
}
```

---

## 6. Layout Improvements

### Current Issues
1. Hero section lacks visual impact
2. All sections look the same - no visual rhythm
3. Skills section uses utility classes inconsistently
4. No clear visual hierarchy between sections
5. Content feels cramped on larger screens

### Proposed Layout Structure

```
┌─────────────────────────────────────────────────────────────┐
│  HEADER - Sticky with blur backdrop                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  HERO SECTION                                               │
│  - Large name with gradient accent                          │
│  - Animated subtitle                                        │
│  - Subtle background glow                                   │
│  - Staggered fade-in animation                              │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ABOUT SECTION                                              │
│  - Clean typography                                         │
│  - Accent line under heading                                │
│  - Comfortable reading width                                │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ │
│  ░ SKILLS SECTION - Alternate background                  ░ │
│  ░ - Card grid layout                                     ░ │
│  ░ - Hover effects on cards                               ░ │
│  ░ - Icon indicators                                      ░ │
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  TALKS SECTION                                              │
│  - Timeline-style layout                                    │
│  - Interactive hover states                                 │
│  - Visual connection between items                          │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ │
│  ░ CONTENT SECTION - Alternate background                 ░ │
│  ░ - Card-based layout for YouTube and Almentor           ░ │
│  ░ - Clear CTAs                                           ░ │
│  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  CONNECT SECTION                                            │
│  - Centered layout                                          │
│  - Social icons with hover effects                          │
│  - Clear call-to-action                                     │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│  FOOTER - Dark background                                   │
│  - Social links                                             │
│  - Copyright                                                │
└─────────────────────────────────────────────────────────────┘
```

### Responsive Breakpoints

```css
/* Mobile First Approach */

/* Small devices - phones */
@media (min-width: 640px) {
  /* sm: Tablet portrait */
}

@media (min-width: 768px) {
  /* md: Tablet landscape */
}

@media (min-width: 1024px) {
  /* lg: Desktop */
}

@media (min-width: 1280px) {
  /* xl: Large desktop */
}
```

---

## 7. Implementation Notes

### Priority Order for Implementation

1. **CSS Variables** - Set up the design tokens first
2. **Typography** - Apply the type scale globally
3. **Header** - Sticky header with blur effect
4. **Hero Section** - High-impact first impression
5. **Section Styling** - Consistent section patterns
6. **Component Cards** - Skills and content cards
7. **Animations** - Add hover effects and scroll animations
8. **Footer** - Complete the page styling

### Files to Modify

1. [`src/styles/global.css`](src/styles/global.css) - Add CSS variables and base styles
2. [`src/pages/index.astro`](src/pages/index.astro) - Update HTML structure and classes
3. [`src/components/Header.astro`](src/components/Header.astro) - Sticky header with blur
4. [`src/components/Footer.astro`](src/components/Footer.astro) - Dark footer styling

### Optional Enhancements

- **Dark Mode Support**: The color palette can be inverted for dark mode
- **Scroll Progress Indicator**: A thin progress bar at the top of the page
- **Intersection Observer**: For triggering scroll animations
- **View Transitions API**: For smooth page transitions in Astro

---

## 8. Visual Reference - Color Palette Preview

```
Primary Colors:
┌──────────┬──────────┬──────────┐
│ #0F172A  │ #1E293B  │ #334155  │
│ Primary  │ P-Light  │ P-Lighter│
└──────────┴──────────┴──────────┘

Accent Colors:
┌──────────┬──────────┬──────────┐
│ #3B82F6  │ #2563EB  │ #DBEAFE  │
│ Accent   │ A-Hover  │ A-Light  │
└──────────┴──────────┴──────────┘

Gradient:
┌────────────────────────────────┐
│ #3B82F6 ────────────► #8B5CF6  │
│ Blue                   Purple  │
└────────────────────────────────┘

Neutrals:
┌──────────┬──────────┬──────────┬──────────┐
│ #FFFFFF  │ #F8FAFC  │ #F1F5F9  │ #E2E8F0  │
│ White    │ BG-Alt   │ Surface  │ Border   │
└──────────┴──────────┴──────────┴──────────┘

Text:
┌──────────┬──────────┬──────────┬──────────┐
│ #0F172A  │ #475569  │ #64748B  │ #94A3B8  │
│ Primary  │Secondary │ Muted    │ Light    │
└──────────┴──────────┴──────────┴──────────┘
```

---

## Summary

This design specification provides a complete visual system for modernizing the portfolio homepage while maintaining professionalism and readability. The design emphasizes:

- **Clean, modern aesthetics** with a blue-purple gradient accent
- **Strong typography hierarchy** using the existing Atkinson font
- **Consistent spacing** based on an 8px grid
- **Subtle animations** that enhance without distracting
- **Visual rhythm** through alternating section backgrounds
- **Accessibility** with proper contrast ratios and reduced motion support

The implementation should be straightforward for a developer to follow, with all CSS variables and component styles clearly defined.
