# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Vue.js 2 portfolio website for Jean-Marc Juif, a fullstack web developer. The site showcases professional experience, projects, skills, certifications, and recommendations with a dark/light theme toggle.

## Development Commands

```bash
# Install dependencies
npm install

# Development server with hot-reload
npm run serve

# Production build (outputs to dist/)
npm run build

# Lint and fix files
npm run lint
```

## Architecture

### Tech Stack
- **Frontend**: Vue.js 2 with Vue Router
- **UI Framework**: BootstrapVue with Bootstrap 4
- **Styling**: SCSS with CSS custom properties for theming
- **State Management**: Vuex (currently empty, not actively used)
- **Build Tool**: Vue CLI with webpack

### Key Components Structure
- `MainNav.vue` - Navigation bar with smooth scroll to sections
- `ThemeButton.vue` - Dark/light theme toggle using localStorage and CSS variables
- `Projects.vue` - Project showcase, reads data from `src/projects.json`
- `Experience.vue` - Professional experience timeline component
- `Formations.vue` - Education and certifications display
- `Quotes.vue` - Recommendations/testimonials section
- `Hobbies.vue` - Personal interests section
- `Footer.vue` - Site footer

### Data Management
- Project data is stored in `src/projects.json` and imported by the Projects component
- Theme preference is stored in localStorage
- No API calls or external data sources

### Theming System
The app uses CSS custom properties for theming:
- Light theme: defined in `:root` in `src/app.scss`
- Dark theme: defined in `:root.dark-theme` in `src/app.scss`
- Theme switching handled by `ThemeButton.vue` which toggles the `dark-theme` class on `document.documentElement`

### Routing
- Single-page application with Vue Router
- Currently only has a Home page at `/`
- Navigation uses smooth scrolling to sections within the page

### Deployment Configuration
- Production builds are configured for `/portfolio/` path (see `vue.config.js`)
- Build outputs to `dist/` directory
- Static assets (images, certificates) are in `public/` directory

### Styling Approach
- BootstrapVue components for UI elements
- Custom SCSS in `src/app.scss` for global styles and theming
- Component-scoped styles for specific component styling
- Responsive design with mobile-first approach

### Important Files
- `src/app.scss` - Global styles, theme variables, Bootstrap imports
- `src/projects.json` - Project data source
- `vue.config.js` - Build and deployment configuration
- `public/` - Static assets (images, certificates, PDFs)

### Development Notes
- The app uses French language throughout
- Images and certificates are referenced from `public/img/` directory
- Some components use BootstrapVue icons (`b-icon-*`)
- Smooth scrolling is implemented with custom `scrollMeTo()` method in Home.vue