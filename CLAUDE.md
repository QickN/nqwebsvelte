# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal portfolio website built with SvelteKit. The site has three main pages:
- Home: A simple landing page with navigation
- Projects: A showcase of various projects with links
- Skills: Information about skills and educational background

## Development Commands

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Start dev server and open in browser
npm run dev -- --open

# Build production version
npm run build

# Preview production build
npm run preview

# Check for TypeScript errors
npm run check

# Check TypeScript errors in watch mode
npm run check:watch 

# Lint code with Prettier
npm run lint

# Format code with Prettier
npm run format
```

## Project Structure

- `src/routes/`: Contains page routes
  - `+page.svelte`: Page components
  - `+page.js`: Page configuration (prerendering, client-side rendering)
  - `+layout.svelte`: Layout component applied to all pages
  - `/projects/`: Projects page
  - `/skills/`: Skills page
- `src/lib/`: Library code and assets
  - `images/`: Image assets
- `static/`: Static files served at root
- `svelte.config.js`: SvelteKit configuration
- `vite.config.js`: Vite configuration
- `jsconfig.json`: JavaScript/TypeScript configuration

## Architecture Notes

- Pages use static prerendering (`export const prerender = true`)
- Client-side rendering is enabled only in development mode for hot module replacement
- The project uses a glass-effect design with animated background
- Navigation is handled via the Header component
- Styling uses a mix of global CSS and component-scoped styles