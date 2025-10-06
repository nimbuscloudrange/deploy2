# GitHub Copilot Instructions for deploy2

## Repository Overview
This repository contains web-based games and interactive tools focused on IT and AI education. The main projects are:
- **index.html**: Landing page for Nimbus Cloud Range with glassmorphism design
- **Tetris.html**: Full-featured Tetris game implementation using Phaser.js

## Technology Stack
- **Frontend**: Pure HTML, CSS, and JavaScript (no build tools required)
- **Game Engine**: Phaser 3.80.0 (CDN-loaded)
- **Deployment**: Static HTML files

## Design System & Aesthetic

### Color Palette
- Background: Dark gradients (`#0b0f14` to `#0f131a`)
- Primary accent: Neon blue (`#78d7ff`)
- Glass effects: `rgba(15, 19, 26, 0.7)` with blur
- Text: White (`#fff`) and light blue tints

### CSS Variables (index.html)
Use existing CSS custom properties defined in `:root`:
- `--neon-blue`, `--glass-bg`, `--glass-border`, `--glass-shadow`
- `--gradient-top`, `--gradient-bottom`
- `--font-main`: Apple system fonts stack

### Visual Style
- **Glassmorphism**: Frosted glass cards with backdrop blur and subtle borders
- **Neon Effects**: Glowing text shadows and box shadows using `--neon-blue`
- **Smooth Transitions**: 0.12-0.2s for hover states and interactions
- **Responsive**: Use `clamp()` for fluid typography
- **Accessibility**: Include ARIA labels and semantic HTML

## Code Style Guidelines

### HTML
- Use semantic HTML5 elements (`<section>`, `<nav>`, `<footer>`)
- Include proper `aria-` attributes for accessibility
- Maintain clean indentation (2 spaces)
- Use descriptive class names (e.g., `glass-card`, `cta-row`)

### CSS
- Inline `<style>` tags in HTML files (no external CSS)
- Use CSS custom properties for theming
- Mobile-first responsive design with flexbox
- Prefer modern CSS (backdrop-filter, clamp(), CSS Grid)
- Keep selectors simple and performant

### JavaScript
- Vanilla JavaScript (no frameworks/libraries except Phaser for games)
- Use modern ES6+ syntax (arrow functions, const/let, destructuring)
- Keep code inline in `<script>` tags
- For Tetris game specifically:
  - Compact, efficient code (minified style where appropriate)
  - Use IIFEs to avoid global scope pollution
  - Include runtime assertions with `console.assert()`

## Component Patterns

### Glass Cards
```html
<section class="glass-card" aria-labelledby="section-title">
  <h2 id="section-title">Title</h2>
  <p>Content...</p>
</section>
```

### Call-to-Action Buttons
```html
<div class="cta-row">
  <a href="#" class="btn primary">Primary Action</a>
  <a href="#" class="btn secondary">Secondary Action</a>
</div>
```

### Hover Effects
All interactive elements should have smooth transitions and hover states with neon glow effects.

## Performance Considerations
- Minimize external dependencies
- Use CDN links for libraries (e.g., Phaser)
- Keep files self-contained for easy deployment
- Optimize for fast load times

## Game Development (Tetris.html)
- Follow Tetris Guideline standards (SRS rotation, scoring)
- Include features: ghost piece, hold, next preview, levels
- Maintain 60 FPS gameplay
- Audio system with mute toggle
- Keyboard controls (arrow keys, space, C, P, Z, X)

## Copyright & Attribution
- Copyright: "© 2025 Nimbus Cloud Range. All rights reserved."
- Author attribution for games: "Ryan Animashan · Nimbus LLC"
- Mission: "Making IT and AI education accessible and affordable for everyone."

## When Making Changes
1. Preserve the existing visual aesthetic and design system
2. Maintain accessibility standards
3. Test responsiveness across viewport sizes
4. Ensure fast load times and smooth animations
5. Keep code clean and well-organized
6. Match the existing coding style and patterns
7. Use semantic, descriptive naming conventions
