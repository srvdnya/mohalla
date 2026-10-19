# Changelog

All notable changes to this project will be documented here.

## [Unreleased] — Location-aware discovery and rich community posts
- Added optional, user-triggered browser location detection with city and neighbourhood reverse geocoding
- Added neighbourhood autocomplete/search, area-specific filtering, dedicated area detail pages and area selection
- Added image carousel and video file selection with in-browser previews and remove controls in the post composer
- Added media previews to feed cards during the current browser session
- Added event-specific date, start time, venue, cost and optional registration link fields
- Made event cards open a dedicated event detail view with key event information
- Added explicit preview limitations for temporary media URLs and local-only demo data

## [Unreleased] — Multi-page community prototype
- Added device-local demo comments, save-post controls, and report/flag interactions with explicit prototype limitations
- Added an open-first feed sort option
- Fixed multi-page city selection and interaction selectors; JavaScript syntax validated
- Reworked the single-page feed into a dedicated homepage and separate neighbourhood feed, explore, events, alerts, about, guidelines and privacy pages
- Added a shared responsive design system, mobile navigation, consistent header/footer and accessible focus states
- Added searchable/filterable sample feed, area discovery, sample events/alerts and a local-only demo post flow
- Made prototype-only and non-verified sample-data limitations explicit in the interface and documentation
- Deferred sign-in and account creation as requested

## Previous city-aware prototype
- Removed the Mumbai-only city switcher in favour of manual city selection and permission-based current-city detection
- Added city-scoped feeds and dynamic area filtering
- Added a local profile prototype with name, bio, hometown, current city, and opt-in current-city display
- Kept current-city sharing off by default and limited the profile location display to a city name
- Updated copy and privacy notes to reflect the city-agnostic direction
- Replaced the mono/typewriter styling with a single readable sans-serif font throughout
- Reduced heavy borders, uppercase labels, decorative pins, and hover motion for a calmer interface
- Improved spacing, form controls, cards, mobile layout, and keyboard focus visibility

## [0.1.0] — Initial prototype
- Six post types (Civic Issue, Alert, Event, Ask Mohalla, Transit, General) with type-specific status flows
- Ward-based filtering, search, and sorting
- Upvoting and threaded comments
- Photo and video attachments (client-side image compression; session-only video preview)
- "Sign in with Google" interface stub
- City switcher (Mumbai live, other cities marked "Soon")
- Full footer with About, How it works, Community guidelines, Contact, Privacy policy, Terms of service, Cookie policy
- Custom favicon and brand identity (Bricolage Grotesque / Schibsted Grotesk / JetBrains Mono, amber/indigo/teal/vermillion/plum palette)
- Entrance animations, hover states, and modal transitions throughout
