# B2B SaaS YouTube Strategy Research Repo

Research base for a YouTube content playbook aimed at B2B SaaS companies. **See `PLAYBOOK.md` for the actual playbook** — this README and the `research/` folder are the supporting evidence base it was synthesized from.

## Constraints

- **Primary goal:** sales enablement and trust-building — not vanity metrics (views, subs, virality).
- **Target audience:** technical practitioners / end users — not executives or buyers.
- **Production resources:** solo founder, minimal budget — favor formats and tactics that don't require a production team.

## Why these 10 experts

The list (Dave Gerhardt, Chris Walker, Guillaume Moubeche, Jason Lemkin, Armand Farrokh & Nick Cegelski, Chris Savage, Ian Faison, Kieran Flanagan & Kipp Bodnar, Ross Simmonds, Rob Walling) was chosen to cover a spread of positions relevant to the brief rather than one archetype:

- **Founder-led personal brands** (Guillaume Moubeche, Rob Walling, Ross Simmonds, Chris Walker) — closest to what a solo founder can actually replicate.
- **Company-brand shows backed by a team** (Marketing Against the Grain/HubSpot, SaaStr, Wistia's Talking Too Loud, Caspian Studios) — useful as upper-bound benchmarks for cadence and production quality, not templates to copy directly.
- **Practitioner-tactic shows** (30MPC, Ross Simmonds, Passetto) vs. **narrative/exec-story shows** (Guillaume Moubeche's interview series, Ian Faison's pop-culture-to-marketing format) — to see which format actually reaches the stated technical-practitioner audience vs. which reaches executives instead.
- **A cautionary case** (Chris Walker) — a founder-led channel that went stale when the founder's attention moved to a new venture, contrasted with the company-brand channel (Passetto) that kept running without him. Worth keeping in the playbook as a risk to plan around.

## What was collected

For each expert: channel/show links were verified directly (not just from search snippets — several initial links turned out to be stale/abandoned, e.g. old playlists last updated in 2022 or 2025 while the real active channel lived elsewhere), a most-recent-upload date was confirmed, and a relevance annotation was written against the three constraints above. See `research/sources.md` for the full per-expert writeup, including a few explicit flags where something didn't match the initial assumption (Chris Walker's pivot away from B2B; Marketing Against the Grain and SaaStr turning out more hands-on/tactical than expected).

- **YouTube transcripts:** 3-5 most recent relevant videos per expert, pulled via `youtube-transcript-api` (Supadata was the first choice per the brief, but no API key/credentials were available in this environment, so this was the fallback). All 10 experts are fully collected (42 transcripts total). Rob Walling's pull initially hit a YouTube IP-level rate limit after ~36 prior video pulls in one session; resolved by retrying from a different network.
- **LinkedIn posts:** no compliant automated scraping/login-based method exists in this environment (no LinkedIn API partnership/credentials, and unauthenticated scraping violates LinkedIn's ToS). As a best-effort alternative, each author's `research/linkedin-posts/<name>/collected-snippets.md` was built from public search-indexed snippets (`site:linkedin.com/posts` queries) — 10 posts per author with partial text, URLs, and comment counts, plus a short read on recurring themes. This is directional, not full post text (LinkedIn requires login for that), but it surfaced some genuinely useful patterns: Guillaume Moubeche reuses the same origin-story hook template across years, Jason Lemkin's "20 AI agents replaced our sales team" post is the direct LinkedIn counterpart to his YouTube "Agents" series, and 30MPC's hosts post the exact same tactics in text form as their videos. Chris Walker's snippets were deliberately pulled from his pre-2026 GTM era, since his current feed is off-topic post-pivot (see his `sources.md` entry).
- **Other materials:** `research/other/` is currently empty. Several candidates surfaced during research (SaaStr's blog archive, Wistia's State of Video report, Rob Walling's books) but weren't pulled in full — flagging them here rather than force-filling the folder with low-value scrapes. Revisit if the playbook needs deeper source material from any one expert.

## How this maps to the constraints

- **Sales enablement / trust-building over vanity metrics:** annotations in `sources.md` specifically call out which shows produce hands-on, implementable content (30MPC, Ross Simmonds, Passetto) vs. which lean on brand/narrative (Ian Faison, Guillaume Moubeche's interview show) — the former is the closer model for this goal.
- **Technical practitioners, not executives:** flagged per-expert where content skews tactical/hands-on (increasingly true even for "exec" shows like SaaStr and Marketing Against the Grain, which have leaned into AI-tool tutorials) vs. where it stays at the strategy/narrative level.
- **Solo-founder, minimal budget:** each entry notes production format (talking-head solo, two-host conversational, interview-with-guest, company-studio-produced) so the eventual playbook can separate "copy this format" from "this only works with a team/budget."

## Structure

- `research/sources.md` — full per-expert entries: channel/show links, most recent confirmed upload date, relevance annotation, and what's been collected.
- `research/linkedin-posts/<author-name>/` — flagged for manual collection per author (no compliant scraping method available); notes/caveats included per author.
- `research/youtube-transcripts/<author-name>/` — pulled transcripts (Markdown, one file per video, with title/date/URL header) for the 3-5 most recent relevant videos per expert.
- `research/other/` — reserved for additional materials (blog posts, decks, non-YouTube podcast transcripts); currently empty, candidates noted above.
