# PNXBird

PNXBird is a static, client-side clan command hub for the PNX clan on
the Total Battle game. It provides event briefings, calendar visibility, reset
timers, daily readiness tracking, and soon, expandable troop-reference content.

## Features

- **Moon dashboard:** `index.html` is the main entry point and dynamically
  loads the Moon, Sun, or Royal themed view.
- **Event briefings:** Shared guidance for Olympus, Ragnarök, Dark Omens, and
  Tinman.
- **Calendar:** FullCalendar displays events from `data/tb-events.ics`, which is
  parsed with ical.js.
- **Reset-aware clocks:** The interface tracks UTC time and the clan's 17:00 UTC
  game-day reset convention.
- **Daily readiness:** Checklist items are stored in browser local storage and
  reset for each game-day cycle.
- **(soon)Troop reference:** Expandable target families and G5–G7 example tiers are
  populated from JSON data.
- **(soon)Themed pages:** `moon.html`, `sun.html`, and `royal.html` provide alternate
  presentation themes using shared dashboard behavior.

## Repository layout

| Path | Purpose |
| --- | --- |
| `index.html` | Main dashboard shell, styling, and client-side application logic |
| `moon.html`, `sun.html`, `royal.html` | Theme-specific page content |
| `data/event-guides.json` | Event briefing data |
| `data/daily-checklist.json` | Daily readiness checklist data |
| `data/troop-examples.json` | Expandable troop-reference data |
| `data/tb-events.ics` | Supplied Total Battle event calendar |
| `brand/` | Logos, hero artwork, and other visual assets |

## Current implementation state

The static HTML dashboard is the active application surface.

The dashboard loads Google Fonts, FullCalendar, and ical.js from CDNs at
runtime. No package manifest or build configuration is currently present in the
repository, so the site can be served as static files from a web server.
