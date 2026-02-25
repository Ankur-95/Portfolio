

# Ankur Rakesh Ujawane — Robotics Portfolio Website

## Overview
A premium, aerospace-themed dark portfolio website with Apple-style minimal aesthetics, interactive animations, and easy content editing via JSON config files.

---

## Phase 1: Foundation & Theming

### Dark/Light Theme System
- Dark graphite/navy base as default with metallic steel highlights and aerospace cyan accents
- Elegant light mode alternative
- CSS variables for seamless switching
- Glassmorphism + metallic card accents throughout

### Typography & Layout
- Refined sans-serif typography (Inter/Space Grotesk) with big spaced headlines
- Mobile-first responsive design with generous whitespace
- High visual hierarchy with surgical gradient usage

### Content Config System
- `/content/siteConfig.json` storing all editable text: name, title, about, skills, experience, achievements, social links, contact info
- `/content/projects/` folder structure with sample project JSON entries
- Site reads all content from these config files for easy GitHub-based editing

---

## Phase 2: Header & Preloader

### Sticky Header
- Initials logo "ARU", anchor nav links (About / Skills / Experience / Projects / Contact)
- Small resume download icon (PDF placeholder)
- Dark/Light mode toggle
- Collapses to hamburger on mobile

### Boot-Up Preloader
- Terminal-style "system initializing..." sequence (2-3 seconds)
- Shows lines like `> Loading modules... ROS | Gazebo | Python`
- Skip button to bypass
- Plays once per session only

---

## Phase 3: Hero Section

### Terminal → Hero Transition
- Typewriter effect briefly prints name and title in terminal style
- Smoothly transitions/fades into the full hero layout

### Hero Layout
- Left column: Name, one-line persona, two CTAs (Contact / Projects)
- Right column: 3D robot model area (Three.js with react-three-fiber, placeholder geometry until .glb model is added — code ready for glTF swap)
- Robot gently rotates, reacts to mouse position; tap-to-pause on mobile

### Particle Background
- Lightweight canvas-based particle system behind hero
- Reduced density on mobile for performance
- Subtle floating dots with connection lines in cyan accent

### Cursor Trail
- Subtle glowing cursor trail effect on desktop only
- Performance-friendly with requestAnimationFrame

---

## Phase 4: About Section

### Professional Statement
- Short paragraph about Ankur's passion for robotics and AI integration
- Clean, centered layout with fade-in animation

### Three Micro-Highlights
- Education: DY Patil College of Engineering, Pune
- Experience: Internship/research highlights
- Drive: "Ready to work hard enough to make the competition less"
- Displayed as glassmorphism cards with metallic hover effects

---

## Phase 5: Timeline Section

### Education & Journey
- Vertical timeline with year markers
- Each entry: year, role/degree, institution
- Scroll-triggered reveal animations
- Minimal connecting line with cyan accent dots

---

## Phase 6: Skills Section

### Category-Based Skill Display
- Programming: C++, Python
- Robotics: ROS, Gazebo, RViz, Simulation
- Embedded Systems
- AI in Robotics
- No progress bars — clean list with small icons per skill
- One-line competency note per category
- Terminal-style console widget cycling through: "ROS | Gazebo | RViz | C++ | Python"

---

## Phase 7: Experience Section

### Internship/Work Cards
- Glassmorphism cards with metallic sheen on hover (lift effect)
- Each card: role, company, 2-4 bullet accomplishments
- Scroll-triggered entrance animations
- Placeholder entries from siteConfig.json

---

## Phase 8: Projects Section

### Interactive Project Grid
- Cards with placeholder states: "Upload media / Add GitHub link"
- Each card supports: title, summary, tech tags, image/video area, GitHub link, type badge (simulation/physical), role, "View demo" or "Coming soon" button
- 3D viewer placeholder slot per project
- Content loaded from `/content/projects/` JSON files
- Dedicated `/projects` subpage with expanded view

---

## Phase 9: Achievements Section

### Badges & Awards
- Clean list/badge layout
- Small icons with achievement titles
- Loaded from siteConfig.json

---

## Phase 10: Contact & Footer

### Contact Section
- Form with name, email, message fields (configured for Formspree integration)
- mailto: fallback link
- Social links (GitHub, LinkedIn, etc.)
- City text: "Pune, India"

### Footer
- Copyright line
- Quick nav links
- Tiny resume download icon
- Social icons repeated

---

## Phase 11: Polish & Documentation

### Accessibility
- ARIA labels on 3D model with fallback image
- Keyboard navigation throughout
- Color contrast compliance
- Semantic HTML

### Performance
- Lazy-loaded images and 3D model
- Reduced animations on mobile
- Lower particle density on small screens
- Optimized re-renders

### README & Admin Docs
- README.md with non-technical editing instructions
- How to: add projects, update social links, replace hero model, update resume
- Step-by-step GitHub web UI editing guide

