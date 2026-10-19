# Mohalla

A city-aware neighbourhood board for civic issues, alerts, events, questions, and everyday local goings-on — organised by city and area, posted by the people living it.

## Current prototype

The site is now a multi-page static front-end built with plain HTML, CSS and vanilla JavaScript. The homepage introduces Mohalla; the community board, neighbourhood explorer, events, alerts, about, community guidelines and privacy overview each have their own page.

### Pages
- `index.html` — homepage and product introduction
- `feed.html` — searchable/filterable neighbourhood board
- `explore.html` — area discovery and manual city selection
- `events.html` — sample local event listings
- `alerts.html` — sample community alerts
- `about.html` — product overview and roadmap
- `guidelines.html` — intended community standards
- `privacy.html` — prototype data-handling overview

Shared UI and demo behaviour live in `assets/site.css` and `assets/site.js`.

## Prototype behaviour

- City selection is manual in this multi-page preview.
- The sample feed includes illustrative civic issues, alerts, events, transit updates, questions and general posts.
- Users can search and filter the sample feed.
- Creating a post stores it in the current browser's local storage only. It is not shared with other visitors or devices.
- Sample posts, people, counts and event details are illustrative and must be removed or replaced with verified content before a public launch.
- Sign-in and account creation are intentionally deferred. The current sign-in button explains that authentication is not yet available.

## Production readiness status

**This is a more complete front-end prototype, not yet a production-ready community service.** Do not present demo alerts as live information or use this prototype for urgent safety notices.

Before launch, implement and test:
- Secure authentication and account recovery
- A shared backend/database with validation, access rules, backups and migrations
- Server-side authorization for creating posts, votes, comments and status changes
- Moderation/report review, spam prevention, rate limits and abuse handling
- Verified alert workflows and clear source attribution
- Privacy policy and terms reviewed for the actual product, data retention/deletion controls, and consent for any location features
- Accessible interaction testing, responsive/browser QA, monitoring and deployment checks
- Replace or remove all illustrative content and mark unverified information clearly

The prototype deliberately does not request precise GPS location. City selection is manual and stored locally.

## Tech stack

- HTML5
- CSS with responsive layouts and reduced-motion support
- Vanilla JavaScript
- Browser local storage for demo-only data
- Google Fonts: Schibsted Grotesk

No build step or framework is required.

## Local development

Serve the repository root rather than opening the files directly:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

The repository is connected to Vercel. The feature branch `feat/location-aware-community` creates preview deployments; changes become production only after merging into the configured production branch (`main`).


## Location, media and detail-page work in progress

- Optional browser geolocation can reverse-resolve a city and neighbourhood after the visitor explicitly taps the location control. Manual city and neighbourhood search remain available.
- Area suggestions are based on the demo neighbourhood list and sample post locations; these are not a live places database.
- Dedicated `area.html` and `detail.html` pages give neighbourhoods, events and community posts their own detail views.
- The post composer supports a local preview of up to six images and one video, with remove controls and an image/video gallery in the current browser session.
- Event posts can capture a date, start time, venue/meeting point, cost and optional registration URL.
- Browser geolocation and reverse geocoding need HTTPS and permission. The demo reverse-geocodes through OpenStreetMap Nominatim; before a production launch, review its usage policy and use a suitable geocoding provider/service.
- Media files are previewed with temporary browser object URLs. Only file metadata is saved in demo post records, not the actual file bytes. Uploaded media will not persist across reloads or be shared until a secure object-storage/backend integration is implemented.

## License

Not yet decided — treat as all rights reserved for now unless a LICENSE file is added.
