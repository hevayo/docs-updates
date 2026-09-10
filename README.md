# docs-updates

The WSO2 Updates documentation. Two sites live in this repo until the cutover:

- `master` builds the current site, https://updates.docs.wso2.com/en/latest/ (MkDocs, `en/`). Writers still change the docs there.
- `docs-v2/main` is the same docs as a Content repo of WSO2 Docs (docs.wso2.com), generated from `master` until the cutover. At the cutover it becomes the repo's main line.

## The WSO2 Docs layout (`docs-v2/main`)

| Directory | Doc space | Editions and branches |
|---|---|---|
| `updates/` | Updates | 2.0.0, built from `docs-v2/main` |

Each Doc space directory holds `docspace.yaml` (the Doc space manifest), `editions.yaml` (per-Edition variables), `redirects.yaml` (page moves), `docs/` (pages; folders are the menu) and `assets/` (images and downloads).

Every branch of this layout starts with `docs-v2/` until the cutover. Updates has one version, 2.0.0, built from the main line; there are no release branches. Docs releases are made by hand from `docs-v2/main` and tagged `2.0.0-docs.<n>`.

The repo root holds only shared files: this README, `CODEOWNERS`, `LICENSE`, the issue and pull request templates, the release workflow (`.github/workflows/docs-bundle-release.yml`, "Release a Docs bundle"), the branch ruleset (`.github/branch-ruleset.json`), the editor settings, and `AGENTS.md` and `CLAUDE.md` for agents (they point to `npx @wso2-enterprise/docs help`), the Platform-managed ones from `templates/content-repo/` in `wso2-enterprise/choreolabs-docs`.

The tools are on GitHub Packages. Once per machine, make a classic personal access token with `read:packages` (authorised for the `wso2-enterprise` organisation's SSO if it asks), then run `npm login --scope=@wso2-enterprise --auth-type=legacy --registry=https://npm.pkg.github.com` with your GitHub user name and the token as the password. This repo's `.npmrc` names the registry for `@wso2-enterprise`; it holds no token.

Get started, from setting up your computer to a Docs release going live: the WSO2 Docs Platform's README, https://github.com/wso2-enterprise/choreolabs-docs#readme.
