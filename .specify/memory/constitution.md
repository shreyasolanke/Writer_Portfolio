<!--
Sync Impact Report:
Version: 0.1.0 → 1.0.0 (Initial creation)
- Created new constitution for Static HTML Writer's Portfolio project
- Added 8 core principles covering static HTML, Google Drive compatibility, accessibility, interactivity, content structure, responsive design, professional presentation, and maintainability
- Templates: ⚠ pending (no templates exist yet - to be created if needed)
-->

# Project Constitution: Static HTML Writer's Portfolio

**Project Name:** Shreya Solanke Writer's Portfolio  
**Constitution Version:** 1.0.0  
**Ratification Date:** 2025-01-27  
**Last Amended Date:** 2025-01-27  

---

## Purpose

This constitution governs the development and maintenance of a static, self-contained HTML portfolio page for writer Shreya Solanke. The portfolio serves as a professional showcase of creative works (screenplays, poetry, songs, novels), credentials, and contact information. The page MUST be uploadable to Google Drive as a single HTML file and accessible via Google Drive's web viewer, while maintaining full interactivity, accessibility, and professional presentation.

---

## Core Principles

### Principle 1: Static Self-Containment

**Rule:** The portfolio MUST be a single, self-contained HTML file with all CSS and JavaScript embedded inline. No external dependencies, external stylesheets, external scripts, or server-side processing are permitted.

**Rationale:** Google Drive file hosting requires a single-file solution. External resources may fail to load or violate security policies when accessed through Google Drive's viewer. Self-containment ensures portability and reliability across hosting platforms.

**Implementation Requirements:**
- All CSS MUST be within `<style>` tags in the `<head>` section
- All JavaScript MUST be inline within `<script>` tags or as inline event handlers
- Images MAY use external URLs (CDN) but MUST have fallback handling
- Fonts MUST use web-safe fonts or embedded base64 data URIs
- No `<link>` tags for stylesheets or scripts
- No `<script src="">` tags

---

### Principle 2: Google Drive Compatibility

**Rule:** The HTML file MUST function correctly when uploaded to Google Drive and accessed via Google Drive's web viewer. All interactive elements MUST work without requiring local file system access or server-side execution.

**Rationale:** The primary deployment target is Google Drive file sharing. Compatibility ensures the portfolio is accessible to viewers without requiring web hosting or technical setup.

**Implementation Requirements:**
- Use relative anchor links (`#section-id`) for internal navigation
- Use `onclick` handlers or inline JavaScript for interactivity (avoid external event listeners that may not bind)
- Test all links and interactive elements in Google Drive preview mode
- Ensure smooth scrolling works without external libraries
- Contact links (mailto:, tel:) MUST be functional
- External links MUST open in new tabs (`target="_blank"`)

---

### Principle 3: Accessibility Compliance

**Rule:** The portfolio MUST meet WCAG 2.1 Level AA accessibility standards. All content MUST be perceivable, operable, understandable, and robust for users with disabilities.

**Rationale:** Professional portfolios must be accessible to all audiences, including those using screen readers, keyboard navigation, or assistive technologies. Accessibility also improves SEO and user experience.

**Implementation Requirements:**
- Semantic HTML5 elements (`<nav>`, `<section>`, `<header>`, `<footer>`, `<main>`)
- All images MUST have descriptive `alt` attributes
- Color contrast ratios MUST meet WCAG AA standards (4.5:1 for text, 3:1 for UI components)
- Interactive elements MUST be keyboard navigable
- Form inputs (if any) MUST have associated labels
- Skip navigation link for screen readers
- ARIA labels where semantic HTML is insufficient
- Focus indicators visible on all interactive elements

---

### Principle 4: Interactive Navigation & Clickability

**Rule:** The portfolio MUST provide smooth, intuitive navigation between sections. All clickable elements MUST provide clear visual feedback and function reliably across browsers.

**Rationale:** User engagement requires seamless navigation. Clickable elements enhance usability and demonstrate attention to user experience.

**Implementation Requirements:**
- Sticky navigation bar with anchor links to all major sections
- Smooth scroll behavior (`scroll-behavior: smooth` in CSS)
- Hover states on all interactive elements (buttons, links, cards)
- Active/focus states clearly visible
- Portfolio items MUST be clickable (even if linking to external samples)
- Call-to-action buttons prominently displayed
- Mobile-friendly touch targets (minimum 44x44px)

---

### Principle 5: Content Structure & Organization

**Rule:** Portfolio content MUST be organized into clear, hierarchical sections reflecting Shreya Solanke's professional identity: Writer, Screenwriter, Technologist, and Songwriter. Each work sample MUST include context, genre, and strategic value.

**Rationale:** Content organization directly impacts how viewers perceive professional credibility and range. Clear categorization helps producers, agents, and collaborators quickly find relevant work.

**Implementation Requirements:**
- Hero section with professional photo, tagline, and brief bio
- About section covering professional background and creative pursuits
- Expertise grid showcasing core competencies
- Portfolio organized by category:
  - Features (screenplays)
  - Short Films
  - Web Series
  - Micro Drama
  - Songs (Spotify integration)
  - Poetry Collections
  - Novels (WIP)
- Each portfolio item MUST include: title, genre/format, description, and link to sample (where available)
- Credentials section: Education, Professional Recognition, IEEE Standards, Publications
- Contact section with email, phone, LinkedIn, Spotify links

---

### Principle 6: Responsive Design

**Rule:** The portfolio MUST render correctly and maintain usability across all device sizes: desktop (1920px+), tablet (768px-1024px), and mobile (320px-767px).

**Rationale:** Viewers access portfolios from diverse devices. Responsive design ensures professional presentation regardless of screen size.

**Implementation Requirements:**
- Mobile-first CSS approach with progressive enhancement
- Flexible grid layouts using CSS Grid and Flexbox
- Media queries for breakpoints at 768px and 1024px
- Typography scales appropriately (no horizontal scrolling)
- Navigation adapts to mobile (hamburger menu or stacked layout)
- Images scale responsively (`max-width: 100%`, `height: auto`)
- Touch-friendly interactive elements on mobile

---

### Principle 7: Professional Visual Design

**Rule:** The portfolio MUST present a clean, modern, professional aesthetic that reflects Shreya Solanke's hybrid identity as technologist and creative writer. Visual design MUST not distract from content.

**Rationale:** First impressions matter. Professional design establishes credibility and demonstrates attention to detail. The aesthetic should bridge technical precision with creative warmth.

**Implementation Requirements:**
- Cohesive color palette (primary, secondary, accent colors defined in CSS variables)
- Consistent typography hierarchy (headings, body, captions)
- Adequate white space for readability
- Subtle shadows and borders for depth without clutter
- Professional photo prominently displayed in hero section
- Consistent spacing system (8px base unit)
- No animated distractions (subtle transitions acceptable)
- Print-friendly styles (optional, via media query)

---

### Principle 8: Sample Work Links & External Integration

**Rule:** Portfolio items MUST link to external samples where available (Google Drive documents, Spotify tracks, published works, etc.). Links MUST be clearly labeled, open in new tabs, and include fallback messaging if samples are unavailable.

**Rationale:** The portfolio serves as a gateway to actual work samples. Clear linking enables viewers to evaluate writing quality, style, and range directly.

**Implementation Requirements:**
- Each portfolio item that has a sample MUST include a "View Sample" or "Read More" link
- Links MUST open in `target="_blank"` with `rel="noopener noreferrer"`
- Spotify embeds or links for song samples
- Google Drive document links for script excerpts
- Clear indication when samples are "Available on request" vs. "View sample"
- Broken link handling (graceful degradation)
- Link text MUST be descriptive (not "click here")

---

## Governance

### Amendment Procedure

1. **Proposal:** Any team member or stakeholder may propose an amendment by documenting the change rationale and impact assessment.
2. **Review:** Proposed amendments MUST be reviewed for consistency with existing principles and project goals.
3. **Versioning:** Amendments MUST increment the version number according to semantic versioning:
   - **MAJOR** (X.0.0): Backward-incompatible changes, principle removals, or fundamental scope changes
   - **MINOR** (0.X.0): New principles added, existing principles materially expanded
   - **PATCH** (0.0.X): Clarifications, typo fixes, non-semantic refinements
4. **Ratification:** Amendments are ratified upon update to this document with updated `LAST_AMENDED_DATE`.
5. **Propagation:** Constitution changes MUST trigger review of dependent templates, specifications, and implementation code.

### Compliance Review

- **Pre-deployment:** All HTML files MUST be validated against this constitution before upload to Google Drive
- **Post-deployment:** Manual testing in Google Drive viewer MUST confirm all principles are met
- **Accessibility audit:** Use automated tools (WAVE, axe DevTools) and manual keyboard navigation testing
- **Cross-browser testing:** Verify functionality in Chrome, Firefox, Safari, Edge (minimum)

### Version History

- **1.0.0** (2025-01-27): Initial constitution creation for Static HTML Writer's Portfolio project

---

## Scope & Boundaries

**In Scope:**
- Single-page static HTML portfolio
- Embedded CSS and JavaScript
- Google Drive file hosting and sharing
- Links to external work samples (Google Drive docs, Spotify, etc.)
- Professional presentation of writer credentials and works

**Out of Scope:**
- Multi-page websites or web applications
- Server-side processing or databases
- User authentication or content management systems
- Blog functionality or dynamic content updates
- E-commerce or payment processing
- External hosting services beyond Google Drive

---

*This constitution is a living document. It reflects the current understanding of project requirements and may evolve as the portfolio grows or deployment needs change.*
