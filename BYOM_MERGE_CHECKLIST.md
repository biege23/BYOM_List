Merge checklist for PR #1

- [ ] Copy `BYOM_WORKFLOW_PATCH.txt` → `.github/workflows/generate-byom-version.yml` and commit on this branch (or grant workflow write permission so the file can be added automatically).
- [ ] Verify workflow yaml syntax (run `act` or GitHub Actions lint).
- [ ] Merge PR to `main`.
- [ ] Confirm Pages publishes: `https://biege23.github.io/BYOM_List/byom_version.json` is reachable.
- [ ] (Optional) Tag release / update downstream consumers (BioComp PR #38).