Quick maintainer instructions

This branch contains a small helper `byom_version.json` and a workflow *patch* (see `BYOM_WORKFLOW_PATCH.txt`) that should be placed at `.github/workflows/generate-byom-version.yml`.

Why merge
- Provides a canonical, CDN-friendly `byom_version.json` so downstream apps (e.g. BioComp) can perform tiny version checks before downloading `BYOM_Models.yml`.

Steps to merge (one-liner)
1. Copy `BYOM_WORKFLOW_PATCH.txt` → `.github/workflows/generate-byom-version.yml` (or paste its contents) and commit on this branch.
2. Confirm the workflow file is valid (lint or run `act` locally) and push.
3. Merge this PR to `main`.
4. Verify `https://biege23.github.io/BYOM_List/byom_version.json` is reachable after Pages builds.

If you prefer, I can open a follow-up PR that adds the workflow file directly (requires repo write). Thank you!