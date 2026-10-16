# stack-board

Hosts the **plan dashboards** for
[`AbdelrhmanBassiouny/cognitive_robot_abstract_machine`](https://github.com/AbdelrhmanBassiouny/cognitive_robot_abstract_machine)
on this repository's own GitHub Pages site, kept separate because that repository's Pages
already serves its documentation.

**Dashboards:** https://abdelrhmanbassiouny.github.io/stack-board/

The [`plan-dashboards` workflow](.github/workflows/plan-dashboards.yml) runs every ~10
minutes and on `workflow_dispatch`. It reads every plan under `.claude/personal/plans/` on
the fork's `claude/personal-notes` branch, fetches the live state of the pull requests
they name, renders the index and one page per plan with the fork's
`basstler.build_site`, and deploys them to Pages. It only reads the public fork.

The pages need no Claude account: anyone with the link sees the same, current site.
