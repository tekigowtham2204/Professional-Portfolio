# Project Structure — Professional Portfolio

This file documents the complete component structure and file organization.

## Components Overview

### src/app/components/

1. **SmoothScrollProvider.tsx**
   - React Context provider for Lenis smooth scrolling
   - Exports `useLenis()` hook for scroll access in components
   - Wraps the entire app for global smooth scroll experience

2. **Header.tsx** (152 lines)
   - Navigation header with Figma logo
   - Sticky on scroll with visual indicator
   - Mobile-responsive with hamburger menu
   - Active section highlighting
   - Smooth scroll navigation to sections
   - Animated indicators using Framer Motion

3. **HeroSection.tsx** (280 lines)
   - Hero intro section with animated profile photo
   - Displays: Name, tagline, skill tags
   - Tags: ['GenAI PM', 'LLM Systems', 'User Research', 'Product Strategy', 'RAG Pipelines']
   - Image asset: `../../assets/f526295bdde79bfd018746c5da9d08c05fa3c1c9.png`
   - Tagline: "Aspiring GenAI Product Manager building LLM-powered products across Healthcare, EdTech, and FinTech."

4. **AboutSection.tsx** (~113 lines)
   - Personal bio and summary
   - Info cards: Location, Email, Education
   - Links: tekigowtham04@gmail.com, linkedin.com/in/gowthambhaskar
   - Education: B.Tech ECE — LPU (2023-2027)
   - Bio covers GenAI PM background and product thinking

5. **ProjectsSection.tsx** (~200 lines)
   - Three featured AI/ML product projects
   - Project data structure includes: name, period, category, description, highlights, links
   - Projects:
     a) CareNote AI (Jan–Apr 2025) — Clinical Documentation Copilot
     b) LearnPath AI (Aug–Dec 2024) — Adaptive Skill-Gap Engine
     c) FinSense AI (May–Aug 2024) — Conversational Financial Clarity Engine
   - Each project links to GitHub repo

6. **SkillsSection.tsx**
   - Skills organised by categories:
     * GenAI & LLMs (GPT-4, Gemini, Prompt Engineering, RAG, LangChain, etc.)
     * Product (PRDs, OKRs, RICE Scoring, Roadmapping, User Stories, A/B Testing)
     * Research (User Interviews, Persona Development, JTBD, Competitive Analysis)
     * Tools & Data (Figma, Miro, Notion, Jira, Python, SQL, Google Analytics)
   - Certifications section

7. **ContactSection.tsx**
   - Contact and social links
   - Email: tekigowtham04@gmail.com
   - Phone: +91 83417 25726
   - LinkedIn: linkedin.com/in/gowthambhaskar
   - GitHub: github.com/tekigowtham2204
   - Call-to-action buttons

8. **SectionHeading.tsx**
   - Reusable section heading component
   - Styling with underline animation
   - Used in: About, Projects, Skills, Contact

### UI Component Library

Directory: src/app/components/ui/

30+ Pre-built Radix UI-based components:
- button.tsx
- card.tsx
- accordion.tsx
- dialog.tsx
- dropdown-menu.tsx
- popover.tsx
- tabs.tsx
- scroll-area.tsx
- badge.tsx
- avatar.tsx
- separator.tsx
- input.tsx
- textarea.tsx
- checkbox.tsx
- radio-group.tsx
- select.tsx
- slider.tsx
- switch.tsx
- table.tsx
- chart.tsx
- carousel.tsx
- progress.tsx
- skeleton.tsx
- tooltip.tsx
- hover-card.tsx
- context-menu.tsx
- breadcrumb.tsx
- command.tsx
- drawer.tsx
- sheet.tsx
- sidebar.tsx
- calendar.tsx
- collapsible.tsx
- menubar.tsx
- pagination.tsx
- navigation-menu.tsx
- label.tsx
- toggle.tsx
- toggle-group.tsx
- alert.tsx
- alert-dialog.tsx
- aspect-ratio.tsx
- input-otp.tsx
- resizable.tsx
- use-mobile.ts (mobile detection hook)
- utils.ts (cn() classname utility)

### Styling

Directory: src/styles/

- **index.css** — Global styles and CSS variables
- **tailwind.css** — Tailwind directives
- **theme.css** — Color, spacing, and design tokens
- **fonts.css** — Font family declarations (Inter, system fonts)

### Assets

Directory: src/assets/

- Hero profile image: f526295bdde79bfd018746c5da9d08c05fa3c1c9.png
- (Other static assets)

## Data Flow

1. **main.tsx** → Renders App
2. **App.tsx** → Wraps with SmoothScrollProvider, renders layout
3. Components import UI primitives from ui/ directory
4. Styling via Tailwind CSS classes + theme.css variables
5. Animations via Framer Motion (motion/react)
6. Smooth scroll via Lenis through SmoothScrollProvider

## Development Notes

- All components use TypeScript
- Component styling uses Tailwind utility classes
- Dark mode support via next-themes (not currently active)
- Mobile-first responsive design
- Lazy-loaded components where appropriate
- Accessibility: Radix UI provides WCAG compliance

## Customisation Points

To update portfolio content:

1. **HeroSection.tsx**: tagline, tags, image
2. **AboutSection.tsx**: bio text, email, education
3. **ProjectsSection.tsx**: project names, descriptions, links
4. **SkillsSection.tsx**: skill categories, skills list
5. **ContactSection.tsx**: contact info, social links
6. **Header.tsx**: navigation items (if adding sections)

## Build & Deploy

- Build: `npm run build` → optimised dist/
- Dev: `npm run dev` → localhost:5173
- Ready for deployment to Vercel, Netlify, GitHub Pages, etc.
