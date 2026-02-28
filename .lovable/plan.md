

# UI Fixes: Hero Buttons, Footer & Contact Cleanup

## 1. Remove "Get in Touch" and "View Projects" buttons from Hero
**File**: `src/components/sections/Hero.tsx`
- Delete lines 64-74 (the `<div className="flex flex-wrap justify-center gap-3">` block with both buttons)
- Also remove the unused `Send` import from lucide-react and `Button` import since they won't be needed anymore

## 2. Footer updates (3 changes)
**File**: `src/components/layout/Footer.tsx`

**2a. Remove "Experience" from navigation**
- Delete line 7: `{ label: 'Experience', href: '#experience' },` from the `navLinks` array

**2b. Add location below "ARU" brand**
- Add a `<p>` with `MapPin` icon and city text (`config?.personal.city || 'Pune, India'`) below the ARU logo link (after line 23)
- Add `MapPin` and `Mail` to the lucide-react imports

**2c. Replace Twitter with Email in social section**
- Remove the Twitter `<a>` block (lines 56-59)
- Add a mailto link with `Mail` icon: `<a href="mailto:ankurujawane@gmail.com">` with the same styling as other social icons
- Remove `Twitter` from imports, add `Mail` to imports

## 3. Remove contact info block from Contact section
**File**: `src/components/sections/Contact.tsx`
- Delete the entire `<ScrollReveal delay={0.2}>` block (lines 81-104) containing MapPin, Mail, GitHub, and LinkedIn
- Clean up unused imports: remove `MapPin`, `Mail`, `Github`, `Linkedin` from lucide-react imports

---

## Summary of file changes

| File | What changes |
|------|-------------|
| `src/components/sections/Hero.tsx` | Remove buttons block (lines 64-74), clean imports |
| `src/components/layout/Footer.tsx` | Remove Experience nav link; add location below ARU; swap Twitter for Email icon |
| `src/components/sections/Contact.tsx` | Remove info/social links block (lines 81-104), clean imports |

