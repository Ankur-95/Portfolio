

# Update Project Card Buttons

## Changes

### 1. `src/components/sections/Projects.tsx`
- Rename "Add GitHub" to "GitHub Link" on the disabled GitHub button (keep the icon)
- Remove the "Coming Soon" button entirely (the `else` branch for `demoUrl`)
- Keep the "Demo" button when `demoUrl` exists

### 2. `src/pages/ProjectsPage.tsx`
- Same changes: rename disabled GitHub button text to "GitHub Link", remove "Coming Soon" button
- Keep the "View Demo" button when `demoUrl` exists

