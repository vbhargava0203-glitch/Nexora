# NEXORA

**Where Campus Comes Alive.** A premium, responsive university event discovery and registration experience built with semantic HTML, CSS, and vanilla JavaScript.

## Run it

Open `index.html` directly in a modern browser. No build step, server, package installation, or backend is needed. The Google Fonts connection is optional; the interface falls back to system sans-serif fonts when offline.

## Included

- Event catalog with live search, category filters, sorting, detail dialogs, availability, and favorites.
- Four-step registration with validation, duplicate checks, capacity checks, confirmation, and browser-local persistence.
- Digital event pass, downloadable as a self-contained printable HTML ticket.
- Registrations dashboard, cancellation confirmation, working countdown, schedule, interactive campus venue map, theme preference, and responsive mobile navigation.
- Demo analytics at `#admin`, with registration and capacity summaries based on the local browser data.
- Reduced-motion support, keyboard focus styles, semantic landmarks, labels, Escape-to-close dialogs, and accessible status announcements.

## Data and privacy

This is a frontend demonstration. Events are defined in `js/events.js`; favorites, theme, and registrations are stored in this browser's `localStorage`. There is no server-side registration, email delivery, or shared database. Each browser keeps its own demo registrations.

## Project structure

```text
nexora/
├── index.html
├── css/
│   ├── style.css
│   └── responsive.css
├── js/
│   ├── app.js
│   ├── events.js
│   ├── registration.js
│   └── animations.js
├── assets/
│   ├── images/
│   └── icons/
└── README.md
```
