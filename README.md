<div align="center">

# NEXORA

### Where Campus Comes Alive.

**A premium, responsive event discovery and registration experience for a university festival.**

[Explore the features](#features) · [Get started](#getting-started) · [Project structure](#project-structure) · [Customization](#customization)

![HTML5](https://img.shields.io/badge/HTML5-semantic-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-responsive-1572B6?logo=css3&logoColor=white)
![Vanilla JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=222)
![No build step](https://img.shields.io/badge/build-none-8A9A5B)
![License](https://img.shields.io/badge/license-not--specified-lightgrey)

</div>

---

## Overview

NEXORA brings a campus festival into one thoughtfully designed web experience. Visitors can discover events, search by name or venue, save favorites, review schedules and venues, register through a guided form, and keep a digital event pass.

The project is built with **HTML5, CSS3, and plain JavaScript**. It has no framework, package installation, build process, or server requirement: open `index.html` in a modern browser and explore.

> **Demo behavior:** registrations, favorites, and theme preference are saved in the current browser with `localStorage`. This is a front-end demo; it does not submit data to a server or send confirmation email.

## Features

### Discover events

- Search event names, categories, descriptions, and venues as you type.
- Filter by event category and sort by featured, popularity, date, or seats remaining.
- Open detailed event views with dates, venue, availability, team size, prize pool, rules, organizer, and schedule.
- Save and revisit favorite events; favorites persist in the browser.
- See registration availability and full-event states.

### Register and keep your pass

- Follow a guided four-step flow for personal information, event and team details, preferences, and final review.
- Get inline field feedback for required details, email and phone formats, team limits, duplicate registrations, and event capacity.
- Review a confirmation summary and receive a unique demo registration ID.
- View a digital event pass or download a self-contained printable HTML ticket.
- Review registrations from the **My Events** area and cancel a registration with an in-app confirmation.

### Explore the festival

- Follow the featured-event countdown and day schedule.
- Browse a custom campus map and select a venue to see its event, capacity, and directions.
- Switch between dark and light themes; your choice is remembered.
- Open the front-end analytics preview at [`#admin`](#admin-preview).

### Designed for different screens and access needs

- Responsive layouts for desktop, tablet, and mobile.
- Semantic page sections, labeled fields, visible keyboard focus, keyboard-operable controls, and Escape-to-close dialogs.
- Reduced-motion preferences are respected.
- Smooth reveal effects and lightweight CSS motion without animation libraries.

## Getting started

### Run locally

1. Download or clone this project.
2. Open `index.html` in a current browser.
3. Browse the demo and register for an event. The browser stores the registration locally.

No Node.js, package manager, build command, or backend is needed. If you prefer a local web server, serve the `nexora/` folder with any static file server and open its `index.html` page.

### Reset the demo data

NEXORA uses browser `localStorage` keys prefixed with `nexora-`. To reset registrations, favorites, and theme, clear this site's local storage in the browser’s developer tools, or run this in the page console:

```js
Object.keys(localStorage)
  .filter((key) => key.startsWith("nexora-"))
  .forEach((key) => localStorage.removeItem(key));
location.reload();
```

## Project structure

```text
nexora/
├── index.html                 # Semantic page structure and app entry point
├── README.md                  # Project guide
├── css/
│   ├── style.css              # Design tokens, components, layout, and theme
│   └── responsive.css         # Tablet and mobile adaptations
├── js/
│   ├── events.js              # Event catalog and localStorage helpers
│   ├── animations.js          # Toasts, reveal observer, and shared helpers
│   ├── registration.js        # Registration flow and digital ticket
│   └── app.js                 # Discovery, navigation, map, schedule, dashboard
└── assets/
    ├── images/                # Optional image assets
    └── icons/                 # Optional icon assets
```

## Customization

### Update event details

Edit the event objects in [`js/events.js`](js/events.js). Each event includes an ID, title, category, date, venue, capacity, registration count, team size, prize, description, rules, organizer, contact, schedule, and visual colors.

Keep each `id` unique. Registrations refer to event IDs, so changing an ID will make existing browser demo registrations point to the older ID.

### Adjust the design

The core palette, surfaces, type colors, radii, shadows, and motion timing are CSS custom properties near the top of [`css/style.css`](css/style.css). Responsive breakpoints and mobile-specific layout changes live in [`css/responsive.css`](css/responsive.css).

### Change the festival countdown

The featured event target date is defined in `js/app.js` in the countdown section. Update the date and local time there when adapting this demo for another festival.

## Admin preview

Open the page with the `#admin` hash, for example `index.html#admin`, to see the demonstration dashboard. It summarizes the bundled event catalog and registrations stored in the current browser. It is a visual preview only; it has no authentication, server-side data, or administrative write operations.

## Technology

- **HTML5** for semantic structure and accessible form controls.
- **CSS3** for the visual system, responsive layouts, animation, and theme variants.
- **Vanilla JavaScript (ES6+)** for rendering, filtering, validation, persistence, dialogs, countdown, and interactions.
- **Web Storage API** for browser-local demo state.
- **Google Fonts** for Manrope and DM Sans when network access is available; system font fallbacks keep the page usable offline.

## Browser support

Designed for current desktop and mobile versions of Chrome, Edge, Firefox, and Safari. A browser with JavaScript and `localStorage` enabled is required for interactive features. If Google Fonts cannot load, the site uses local system sans-serif fonts.

## Privacy and production use

All supplied sample registration details stay in the browser that created them. Because there is no backend, data is not shared between people or devices, and the registration confirmation does not send an email. Do not use this demo to collect real attendee information. A production deployment would need a secure backend, appropriate data handling, server-side capacity and duplicate checks, and a real ticket-validation flow.

## License

This project is provided as a demonstration. Add or replace a license before redistributing it as an open-source project.

---

<div align="center">

**NEXORA · Discover. Compete. Create. Connect.**

`college-fest` · `event-registration` · `event-management` · `campus-events` · `html` · `css` · `javascript` · `vanilla-js` · `responsive-design` · `frontend` · `localstorage` · `no-framework`

</div>
