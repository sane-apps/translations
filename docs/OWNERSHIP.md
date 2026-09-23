# Ownership and coordination

Multiple agents share these repos. Rules to avoid collisions and lost work.

## Lane operators (as of 2026-09-23)

| Lane | Operator | Books |
|------|----------|-------|
| reformed | Cursor densify loop (daytime cadence) | 6 Reformed books (`docs/work-lanes.json`) |
| densify | Cursor densify loop | refresh-lane books |
| rank1 | paused; no operator | all other books by default |
| topics | site builder flow | `ante-nicene-topics` |
| latin | unassigned | none yet |
| overnight claims | scheduled `fathers-overnight` runner | whatever `docs/CLAIMS.md` has free |
| pipeline/infra | Muse | scripts, gates, catalog, night machinery |

Lane-to-book mapping is authoritative in `docs/work-lanes.json`, not here.

## Area ownership

- `publication-review.json` regeneration: whoever holds the manifest lock.
  `scripts/manifest_lock.py acquire --agent NAME --task ...` before starting,
  `release` after. Never regenerate while another agent holds it; locks
  expire after 30 min so crashes cannot wedge the lane.
- Site ships: routine punches by the densify loop; owner-requested ships by
  whoever is asked. Never `--skip-build` past a gate failure.
- Catalog/authority/catelog regen scripts: mechanical; any agent may re-run
  after book.yml changes.
- Logos builds: see `docs/LOGOS_BACKLOG.md` (automation in progress).

## Collision rules

1. Never edit another lane's book files (translations, reviews, justifications).
   Metadata-only lane notes go through the lane operator.
2. Never hand-merge `publication-review.json` conflicts: take one side and
   regenerate from the current tree (`scripts/regen_declared_packet.py` +
   genuine receipt review).
3. Commit only your own files. Never `git add -A` / `git commit -a` in a
   shared tree; name paths explicitly.
4. Coordinate book-scope changes through `SESSION_HANDOFF.md` (existing
   convention); claim slices through `scripts/claims.py`.
5. If a hook or lock blocks you, stop and report; do not retry around it.
