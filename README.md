# oss-ci

Manual CI runners I use to build and test branches of my open-source contributions before opening a PR, when my own machine can't build the project.

- `fork-branch-verify.yml`: checks out a branch of one of my forks and runs a given command (Rust and/or Node).
- `mpc-branch-verify.yml`: fmt, clippy and tests for one crate of a `near/mpc` fork branch (installs `cargo-near` for contract tests).

Both are `workflow_dispatch` only, use no secrets, and have read-only permissions.
