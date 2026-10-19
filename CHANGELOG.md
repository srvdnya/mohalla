# Changelog

All notable changes to this project will be documented here.

## [Unreleased] — City-aware community prototype
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
