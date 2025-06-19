# System Patterns

## System Architecture

The application is currently a client-side web application, primarily driven by HTML, CSS (Tailwind CSS), and JavaScript. Data persistence is minimal, relying on local storage or potentially a simple JSON structure for now.

## Key Technical Decisions

- **Front-end Framework/Library:** None explicitly, using vanilla JavaScript for DOM manipulation.
- **Styling:** Tailwind CSS for utility-first styling.
- **Build Process:** PostCSS for Tailwind CSS processing.

## Design Patterns in Use

- **Module Pattern (Implicit):** JavaScript code might be organized into modules, though not formally enforced yet.
- **Event-driven:** User interactions will trigger events handled by JavaScript functions.

## Component Relationships

- `index.html`: Main entry point, contains the UI structure.
- `main.js`: Handles application logic, DOM manipulation, and data management.
- `input.css`/`tailwind.config.js`/`postcss.config.js`: Related to styling and build process.
- `horarios_pilates.md`: Contains raw schedule data that needs to be parsed and displayed.
