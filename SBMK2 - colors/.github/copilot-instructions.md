# Copilot Instructions for SBMK2 Codebase

## Overview
This is a static website project focused on recipes and food presentation. The codebase is organized for maintainability and visual clarity, using HTML, CSS, and JavaScript. There is no build system or backend; all logic is client-side.

## Architecture & Structure
- **HTML Files**: Each major page (e.g., `index.html`, `grid.html`, `layout.html`, `showcase.html`, `alternative.html`) represents a distinct section or layout style. Pages are not dynamically generated.
- **CSS Directory**: Contains style sheets for each layout and section. The main stylesheet is `css/style.css`, which sets global styles and media queries. Other CSS files (e.g., `grid.css`, `layout.css`, `showcase.css`) provide page-specific overrides.
- **JS Directory**: Contains `script.js` for interactive features. All scripts are loaded directly in HTML files.
- **Image Directories**: `images/`, `imaalternative/`, and `otherimgs/` store assets for different sections. Image filenames are referenced directly in HTML and CSS.

## Key Patterns & Conventions
- **Containers**: The `.container` and `.container_inner` classes are used to structure content. CSS uses `nth-of-type` selectors to style containers based on their order in the DOM, not by class or ID.
- **Responsive Design**: Media queries in `style.css` adjust layout for various screen sizes. Widths are set via IDs like `#w20`, `#w50`, `#w100` and overridden in media queries.
- **Font Management**: Multiple font families are declared in `body`, but only the last one applies due to CSS rules. Use the last `font-family` for consistency.
- **Navigation**: Navigation is handled via anchor tags in HTML. No SPA routing or dynamic navigation.
- **No Build/Deploy Steps**: Files are served as-is. No npm, webpack, or other build tools. To update the site, edit HTML/CSS/JS and upload to the host.

## Developer Workflow
- **Edit HTML/CSS/JS directly**. No compilation or preprocessing.
- **Preview changes locally** in a browser. No automated test or linting setup.
- **Add new pages** by duplicating an existing HTML file and updating references.
- **Add new styles** by creating a new CSS file or extending an existing one, then linking it in the relevant HTML file.
- **Add images** to the appropriate directory and reference them by relative path.

## Examples
- To style a new section, add a new `.container:nth-of-type(N)` rule in `style.css` and update the HTML structure accordingly.
- To make a page responsive, add or update media queries in `style.css`.
- To add interactivity, extend `js/script.js` and link it in the target HTML file.

## Integration Points
- No external dependencies or APIs are used.
- Fonts are loaded via CSS, but ensure the correct font is applied (see above).

## Key Files
- `css/style.css`: Main global and responsive styles.
- `js/script.js`: All client-side scripting.
- `index.html`, `grid.html`, `layout.html`, `showcase.html`, `alternative.html`: Main site pages.
- `images/`, `imaalternative/`, `otherimgs/`: Image assets.

---

**If any conventions or workflows are unclear, please provide feedback so this guide can be improved.**
