# Sporv Marketplace

The Sporv youth-sports **marketplace** — the family-facing product exactly as
it was: the classic landing with company/coach cards and search, Explore,
map, saved, product pages, the Trust page, the full sign-up process, and
booking with Stripe Connect checkout. The coach portal supplies it.

Snapshot of `sporve-web` from the marketplace era (before the pivot to the
agent-first club-ops app). Runs against the shared Supabase backend
(anon key, RLS-enforced) and the deployed Stripe edge functions.

## Build & run

```bash
python3 src/build.py            # inlines src/mod-*.js into index.html
python3 -m http.server 4173     # then open http://localhost:4173
```

One static `index.html` — fonts and hero images inlined, talks straight to
Supabase and the Stripe edge functions. No server, no secrets in this repo.
`bash src/smoke.sh` is the pre-commit gate.
