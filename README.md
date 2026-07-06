# stack-board

Hosts the **stacked-PR board** for
[`AbdelrhmanBassiouny/cognitive_robot_abstract_machine`](https://github.com/AbdelrhmanBassiouny/cognitive_robot_abstract_machine)
on this repo's own GitHub Pages site — kept separate because that repo's Pages is already used by its
documentation.

The [`board` workflow](.github/workflows/board.yml) polls the fork every ~10 minutes (and on
`workflow_dispatch` / `repository_dispatch`), reads its open PRs, renders the board with the fork's
`dev/stack.py`, and deploys it to Pages. It only reads the public fork and never modifies it.

**Board:** `https://abdelrhmanbassiouny.github.io/stack-board/`

The board's tooling and doctrine live in the fork under `dev/` (see `dev/README.md` there).
