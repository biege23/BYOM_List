This PR adds a canonical `byom_version.json` (small version endpoint) and includes a workflow *patch* that maintainers can copy into `.github/workflows/generate-byom-version.yml`.

Why
- Enables clients to perform a tiny, frequent version check before downloading `BYOM_Models.yml`, preventing origin throttling and thundering-herd behavior.

What changed
- `byom_version.json` (added)
- `BYOM_WORKFLOW_PATCH.txt` (workflow YAML attached as a patch — see contents)

Notes for maintainers
- I could not create a workflow file directly under `.github/workflows/` via the API in this repo; the workflow YAML is attached as `BYOM_WORKFLOW_PATCH.txt` in this branch. Please copy it to `.github/workflows/generate-byom-version.yml` (or grant CI permissions to allow the file to be added via this branch).
- Once merged, the workflow will auto-update `byom_version.json` on pushes to `BYOM_Models.yml`.

Validation
- After merge, confirm the Pages URL for `byom_version.json` is reachable: `https://biege23.github.io/BYOM_List/byom_version.json`

Security
- Workflow only writes a generated JSON file and commits it back; it uses `actions/checkout@v4` with `fetch-depth: 0` (intended) and commits as `github-actions[bot]`.

If you prefer, I can open a follow-up PR that adds the workflow file directly once you enable repository write permissions for automation.