@AGENTS.md

## This repo

- Updates (`updates/`) has one Edition, the Self-hosted version 2.0.0, built from the main line `docs-v2/main` (`branch: main` on the Edition in `docspace.yaml`). There is no release branch: 2.0.0 is released by hand from `docs-v2/main` as `2.0.0-docs.<n>`.
- Until the cutover the pages here are generated from `master` (MkDocs, `en/`) by the onboarding workspace's `tools/onboard-mkdocs/convert-updates.mjs`: fix the source on `master` or the script's rules, not the pages here.
- Every page keeps its old name in its address with front-matter `slug:` (`/updates/2.0.0/<page>/`), whatever folder the sidebar puts it in. Keep the slug when you move a page.
