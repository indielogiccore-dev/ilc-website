# Repository Guidelines

## Project Structure & Module Organization

This repository is a static single-page web prototype. The main implementation lives in `code.html`, with inline Tailwind configuration, CSS helpers, markup, and CDN-loaded assets. `DESIGN.md` documents the Tactile Core visual system, including color tokens, typography, spacing, shapes, and neumorphic elevation rules. `screen.png` is the current visual reference for the page.

Keep future source files grouped by purpose if the project grows: place reusable styles in `src/styles/`, scripts in `src/scripts/`, and local images in `assets/`. Avoid splitting the current page unless there is enough repeated logic or styling to justify it.

## Build, Test, and Development Commands

No package manager, build pipeline, or test runner is currently configured.

- Open `code.html` directly in a browser to preview the page.
- Run `python -m http.server 8000` from the repository root if browser security rules require a local server, then visit `http://localhost:8000/code.html`.

The page depends on external CDN resources for Tailwind, Google Fonts, Material Symbols, and remote images, so an internet connection is required for a faithful preview.

## Coding Style & Naming Conventions

Use 2-space indentation for HTML nesting and keep utility classes ordered by layout, spacing, typography, color, then state. Preserve the existing Sora typography, Tailwind token names, and neumorphic helper classes such as `.neumorphic-raised`, `.neumorphic-inset`, and `.neumorphic-button-active`.

Use descriptive section comments for large page regions. Name new assets with lowercase, hyphen-separated filenames, for example `hero-dashboard.png`.

## Testing Guidelines

There are no automated tests yet. Before submitting changes, manually verify `code.html` in current Chrome or Edge at desktop and mobile widths. Check that shadows, spacing, remote images, form controls, and sticky navigation render correctly. Compare meaningful visual changes against `screen.png` and update the screenshot only when the intended UI changes.

## Commit & Pull Request Guidelines

This directory has no available Git history, so no existing commit convention can be inferred. Use concise imperative commit messages such as `Refine neumorphic card spacing` or `Add responsive hero adjustments`.

Pull requests should describe the user-visible change, note any design-system deviations from `DESIGN.md`, include screenshots for visual changes, and list manual browser checks performed.

## Security & Configuration Tips

Do not commit secrets or API keys into `code.html`. Treat third-party CDN URLs as production dependencies; document any new external script, font, or image source in the pull request.
