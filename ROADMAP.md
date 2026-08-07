# BLK RAVN — Roadmap

Work intentionally deferred until we're more established — mostly things that need
partner approval, paid/partner APIs, or a research effort. Anything under "Shipped"
is already live in the app.

## Rideshare (Uber / Lyft)
- **Shipped:** "Book Uber" / "Book Lyft" deep-link buttons on drive legs — free, no API keys; the rider books and pays in their own app.
- **Later (once established):**
  - Enroll in the Uber / Lyft **affiliate / referral programs** — earn referral credit on rides we send them.
  - **In-app booking** — request a ride without leaving BLK RAVN (requires Uber/Lyft partner API approval).
  - **Live fare estimates & ETAs** (requires API access).
  - **Account linking / one-tap booking** (deeper OAuth per rider).

## Reservations
- **Shipped:** "Reserve on OpenTable" (name + city search) for dining venues; "Call to book" (opens the venue's map listing) for bars. Coffee shops and breweries stay walk-in.
- **Later (once established):**
  - **Real phone numbers** — web-search each venue's number and store it in the venue `phone` field so "Call to book" dials directly. The `phone` field and `tel:` logic are already wired; it just needs the data.
  - **OpenTable partner / affiliate integration** — real-time availability and in-app booking instead of a search handoff.

## Data / coverage
- **Finish coastal venue coordinate verification** — pending real lat/lon (still approximate): The Pennant, Lazy Eye Coffee, Green Fork, Rosemary's, Lahaina Beach House, Mavericks, JRDN, Price Street Pizza, Drift Cafe, Vanman's, Paradisaea, Pepino, El Pueblo, Mini's Panini. Also confirm neighborhood for Lahaina Beach House and Paradisaea (marked Pacific Beach, awaiting coords). Verify ambiguous venues (Molly's, Vanman's, Zoya, Lazy Eye Coffee).
- Add **real phone numbers** to the venue `phone` field (also enables direct-dial "Call to book").
- Expand venues **beyond San Diego** — the location engine currently maps everyone to San Diego neighborhoods.
- Add more **café / brunch venues** to keep enriching morning itineraries.

## Dev / infra
- Merge the **Vite dev setup** (on the `chore/dev-setup` branch) so both machines share a proper local dev server + build.
