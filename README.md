# MU

MU is a workspace for the MU pipeline system. It brings together the Python execution worker and the MasterFlow desktop/backend while keeping each component in its own Git repository.

## Repositories

| Directory | Responsibility | Documentation |
| --- | --- | --- |
| [mu-cli](https://github.com/khanhtranrk/mu-cli) | Python CLI, pipeline execution, GPU-aware scheduling, actions, conditions, and master-flow worker integration. The executable is named `mu`. | [CLI README](https://github.com/khanhtranrk/mu-cli/blob/master/README.md), [spec reference](https://github.com/khanhtranrk/mu-cli/blob/master/docs/spec-format/README.md) |
| [mu-masterflow](https://github.com/khanhtranrk/mu-masterflow) | Tauri/React desktop UI, Convex backend, specs, requests, units, notifications, and worker HTTP endpoints. | [MasterFlow README](https://github.com/khanhtranrk/mu-masterflow/blob/main/README.md), [agent guide](https://github.com/khanhtranrk/mu-masterflow/blob/main/AGENT.md) |

## Clone

```bash
git clone --recurse-submodules https://github.com/khanhtranrk/mu.git
cd mu
```

For an existing checkout:

```bash
git submodule update --init --recursive
```

## Update submodules

```bash
git submodule update --remote --merge
# Review changes, then commit updated submodule pointers in the parent repository.
git status
```

Normal `git pull` in the parent does not automatically advance submodules to the latest upstream commits. To check out exactly the commits recorded by this workspace, use `git submodule update --init --recursive`.

## Development

Read [AGENTS.md](AGENTS.md) before cross-repository changes and [docs/README.md](docs/README.md) for shared documentation conventions. Run development commands from the relevant submodule directory, not the workspace root.

The submodules are independent projects with independent commits, branches, and dependencies. For changes spanning both, commit and push changes in the affected submodules first, then update the parent workspace's submodule pointers.
