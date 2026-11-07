# Singularity Scout (TEST COPY)

A separate copy of Team 51's scouting board for trying out changes. **Nothing here affects the real board.**

| | Test copy (this repo) | Real board |
|---|---|---|
| Link | <https://eatinghamlili.github.io/singularity-scout-dev/> | <https://eatinghamlili.github.io/singularity-scout/> |
| Code | `eatinghamlili/singularity-scout-dev` | `eatinghamlili/singularity-scout` |
| Database | Supabase project `singularity-scout-dev` | Supabase project `singularity-scout` |

- The test database started as a copy of the real board's data on Nov 7, 2026, so the same scout codes work.
- An orange **TEST COPY** bar at the top of every page links back to the real board.
- Notes, ratings and picks saved here stay here.

## Making changes

1. Edit `src/board.html`. This is the board's source for the test copy only.
2. Rebuild the page: `python tools/build-site.py`
3. Commit and push. The test link updates within about a minute.

## Moving a change to the real board

When a change works here, copy `src/board.html` over the real board's source (`alliance-pick-board.html`), rebuild the real site with its `tools/build-site.py`, and push the `singularity-scout` repo. If a change needs a database rule change (`supabase/schema.sql`), apply it to the real `singularity-scout` project too.

## Notes

- Free Supabase projects pause after about a week with no activity. If the test copy can't reach its data, restore `singularity-scout-dev` in the Supabase dashboard.
- To refresh the test data from the real board, ask for the live data to be copied over again. That replaces what's in the test database.
