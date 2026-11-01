# stack-board

Hosts the **plan site** built by [basstler](https://github.com/AbdelrhmanBassiouny/basstler):
one hub page, one index per registered repository, and one dashboard per plan, served on
this repository's own GitHub Pages.

**Site:** https://abdelrhmanbassiouny.github.io/stack-board/

The [`plan-site` workflow](.github/workflows/plan-site.yml) calls basstler's reusable
`plan-site-build.yml`. It reads the hub file on `AbdelrhmanBassiouny/basstler`'s notes
branch, which lists every repository the site publishes, renders their plans with the live
state of the pull requests they name, and deploys only when a page changed.

Nothing runs on a schedule. Each registered repository's notes branch carries a dispatch
workflow that starts this one on every push to it; it can also be run by hand.

Both workflows are written by basstler's `/setup-personal-notes`
(`python -m basstler.plan_site.publication`); re-run it to update them.
