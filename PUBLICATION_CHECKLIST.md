# Publication Checklist

Use this checklist before making this proof kit public or pushing it to GitHub.

## Repository Boundary

- [ ] Repository name is intended to be `consequence-warehouse-safety-proof-kit`.
- [ ] The private engine repository remains separate as `consequence-warehouse-safety`.
- [ ] No GitHub remote is attached until the final publication decision.
- [ ] No GitHub Actions workflows are enabled by default.
- [ ] The public repo is a proof kit, not an open-source release.

## File Safety

- [ ] No `src` directory.
- [ ] No `engine` directory.
- [ ] No `private` directory.
- [ ] No Python source files.
- [ ] No notebooks.
- [ ] No JavaScript, TypeScript, HTML, or CSS dashboard implementation files.
- [ ] No raw generated evidence runs.
- [ ] No customer data.
- [ ] No credentials, tokens, API keys, or private URLs.
- [ ] No private deployment or production tooling.

## Licence And Access Boundary

- [ ] `LICENSE.md` states public review only.
- [ ] `NOTICE.md` states the private implementation remains separate.
- [ ] `COMMERCIAL_USE.md` says commercial use requires written permission.
- [ ] `ACCESS_REQUEST.md` explains how to request private review.
- [ ] `NDA_ACCESS.md` explains that private access may require an NDA.
- [ ] `PROOF_SCOPE.md` lists included and excluded materials.
- [ ] No patent, trademark, hosted-service, AI-platform, model-training, or
      commercial rights are granted by accident.

## Claim Safety

- [ ] Claims are framed as seeded simulator evidence, not production safety
      certification.
- [ ] Results are tied to the locked `warehouse_v16_default` scenario.
- [ ] Limits are stated in the README and evidence card.
- [ ] The proof does not claim every warehouse or fleet will show the same
      deltas.
- [ ] The oracle/reference mode is not presented as product behaviour.

## Evidence Safety

- [ ] Public metrics are summarized, not raw private run folders.
- [ ] Hash references do not include private artifact contents.
- [ ] Screenshots do not expose secrets, local usernames, private paths, or
      unrelated projects.
- [ ] Screenshots show public-safe dashboard state only.
- [ ] The proof kit can be reviewed without access to the private engine.

## Final Local Checks

Run these before publication:

```powershell
git status -sb
git remote -v
git ls-files
rg -n --glob "!PUBLICATION_CHECKLIST.md" "API_KEY|SECRET|TOKEN|PASSWORD|BEGIN PRIVATE KEY|gho_|sk-[A-Za-z0-9]" .
git ls-files | Select-String -Pattern "(^|/)src/|(^|/)engine/|(^|/)private/|\\.py$|\\.ipynb$|\\.js$|\\.ts$|\\.html$|\\.css$|evidence/runs|evidence/raw"
```

Expected result: clean working tree, no remote unless deliberately added, no
secret hits, and no private source or raw evidence files tracked.
