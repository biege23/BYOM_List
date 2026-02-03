Adds `byom_version.json` (canonical version endpoint) to enable lightweight client checks before downloading BYOM_Models.yml.

Includes `BYOM_WORKFLOW_PATCH.txt` (workflow YAML attached) — maintainers: please copy this file to `.github/workflows/generate-byom-version.yml` after review if the API blocks direct workflow creation.

Validation:
- Pages URL: `/byom_version.json` will be reachable after merge.
- Consumer app: BioComp will check this endpoint before fetching `BYOM_Models.yml`.
