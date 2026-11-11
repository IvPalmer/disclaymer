# Disclaymer

Portfolio site for Disclaymer, two developers shipping web apps and unusual digital products: shipped projects plus a contact channel. Next.js 15 static export (`out/`), pnpm. Co-owned: the upstream repo is `claytonbrgsdev/disclaymer`; `IvPalmer/disclaymer` is the operator's fork and the deploy source.

Where: work / freelance / disclaymer, `~/Dev/work/freelance/disclaymer` (manifest row `disclaymer`, no lead).

Read docs/ROADMAP.md first: goal, open tasks and the decisions waiting on the operator (which deploy is canonical, whether the project list is current).

Verify: `pnpm install --frozen-lockfile && pnpm build` (writes `out/`). `pnpm dev` for a local preview of the static site.

## Deploy
- `disclaymer-test.grooveops.dev`: Dokploy builds the `Dockerfile` (static export served by nginx, only `out/`) from `IvPalmer/disclaymer` branch `vps-deploy`; a push there redeploys. `RUNTIME.md` has the VPS notes.
- `www.disclaymer.com`: GitHub Pages of `claytonbrgsdev/disclaymer`, branch `main`, served from the repo root, so anything merged there is public as a file. `.github/workflows/deploy.yml` (Pages through Actions on `main`) is the older route.
- The two remotes have diverged; work and PRs go to `IvPalmer/disclaymer` `vps-deploy` (remote `ivpalmer` in the Mac checkout) unless the operator says otherwise.
