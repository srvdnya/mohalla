# Mohalla

A city-aware neighbourhood board for civic issues, alerts, events, questions, and everyday local goings-on — organised by city and area, posted by the people living it.

Designed to work in any city. The current version is a single-file static prototype; no production backend yet.

## What it does

Mohalla is a community bulletin board with six post types, each with its own colour and status flow:

| Type | Use case | Status flow |
|---|---|---|
| **Civic Issue** | Potholes, garbage, illegal hawking/construction, water, lighting, safety | Reported → In Progress → Resolved |
| **Alert** | Something happened — water cuts, closures, incidents | Active → Update → Resolved |
| **Event** | Gigs, meetups, local happenings | — (shows a date/time instead) |
| **Ask Mohalla** | Questions to neighbours | Open → Answered |
| **Transit** | Train/road delays and disruptions | Active → Update → Resolved |
| **General** | Lost pets, shoutouts, anything else | — |

Also included:
- City selection with browser location detection (permission-based) and manual city fallback
- City-scoped feeds, dynamic area filtering, search, and sorting (top / recent / open-first)
- Local profile prototype with name, bio, hometown, current city, and opt-in current-city display
- Current-city display is off by default; only the city name is shown, never coordinates or a precise address
- Upvoting and threaded comments per post
- Photo and video attachments (photos are compressed client-side; videos preview for the current session only — see [Known limitations](#known-limitations))
- A "Sign in with Google" interface (UI only — not yet wired to real auth)
- A city switcher that supports detected or manually selected cities
- Full footer with About / How it works / Community guidelines / Contact / Privacy / Terms / Cookie pages

## Tech stack

Plain HTML, CSS, and vanilla JavaScript — no build step, no framework, no dependencies beyond Google Fonts (Schibsted Grotesk for a consistent, readable sans-serif interface.

Posts currently persist through the [Claude artifact storage API](https://docs.claude.com), which only works inside the Claude.ai preview. **This is the main thing to swap out before this works as a real live board** — see below.

## Known limitations

This is a working prototype, not a production app yet:

- **No real backend.** Posts are stored via Claude's in-preview storage. Once deployed elsewhere (e.g. Vercel), posting won't persist for real users until it's connected to an actual database. Profile and city preferences currently use browser-local storage.
- **No auth.** The Google sign-in button is interface-only. Anyone can post, upvote repeatedly on refresh, or cycle a post's status.
- **No moderation.** The "Report" button is a stub — it doesn't do anything yet.
- **Videos don't persist.** They preview only for the current browser session (no storage layer for large files yet).
- **Legal pages are placeholders.** Privacy Policy and Terms of Service are generic starter text, not reviewed — replace before any real launch.

## Roadmap

- [ ] Real backend (Firebase looks like the natural fit) for posts, comments, and votes
- [ ] Wire up Google sign-in
- [ ] Persistent video/file uploads
- [ ] Basic moderation for reported posts
- [x] City-agnostic prototype with manual city selection and optional location detection
- [x] Local profile prototype with opt-in current-city display
- [ ] Replace prototype storage with a real backend and city-aware data model
- [ ] Add area-level relevance and nearby discovery using coarse location only

## Local development

No build step — just open `index.html` in a browser. For a closer-to-production feel, serve it locally instead of opening the file directly:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Currently deployed via GitHub → Vercel. Push to `main` and Vercel redeploys automatically.

## License

Not yet decided — treat as all rights reserved for now unless a LICENSE file is added.
