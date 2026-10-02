# Task Master

Task Master AI is a CLI and MCP server for planning software work from a product requirements document. It stores project configuration, tasks, subtasks, dependency data, and reports in the project's `.taskmaster/` directory.

This checkout contains the Task Master project associated with [eyaltoledano/claude-task-master](https://github.com/eyaltoledano/claude-task-master). The source credits Eyal Toledano and Ralph Khreish. Preserve those notices. The license includes the Commons Clause; read [LICENSE](./LICENSE) before redistributing, selling, or offering the software as a service.

## At a glance

| Field | Details |
|---|---|
| npm package | `task-master-ai`, version `0.16.1` in package metadata |
| CLI | `task-master` |
| MCP server binaries | `task-master-mcp`, `task-master-ai` |
| Project store | `.taskmaster/` |
| Main implementation | `scripts/modules/` and `mcp-server/` |
| License | MIT with Commons Clause; see [LICENSE](./LICENSE) |

## What it does

- Initializes Task Master files in a project.
- Parses a PRD into tasks and subtasks.
- Tracks task status, dependencies, and next actionable work.
- Provides CLI commands and an MCP server interface.
- Supports multiple AI providers selected through project configuration.

Task generation and analysis send prompt and project content to the configured model provider. Configure only providers you intend to use and check their data policies and costs.

## Quick start

Install the published package and initialize the project where you intend to use Task Master:

```sh
npm install --global task-master-ai
task-master init
task-master models --setup
```

Place a PRD in `.taskmaster/docs/`, configure credentials for the selected provider, then run:

```sh
task-master parse-prd .taskmaster/docs/prd.txt
task-master list
task-master next
```

See the [tutorial](./docs/tutorial.md), [command reference](./docs/command-reference.md), and [configuration guide](./docs/configuration.md) for setup details. The CLI writes task data and configuration under the project it finds. This repository already contains a sample `.taskmaster/` tree; avoid running initialization or task mutations here unless you intend to change those sample files.

## MCP server

The package exposes `task-master-mcp` and `task-master-ai` binaries for MCP clients. See the [tutorial](./docs/tutorial.md) and [MCP server implementation](./mcp-server/server.js) for configuration. Pass API keys through your MCP client's protected environment settings; do not commit real keys.

## Repository map

| Path | Purpose |
|---|---|
| `bin/task-master.js` | CLI entry point |
| `scripts/init.js` | Project initialization |
| `scripts/modules/` | Task operations, dependency handling, model/configuration, and CLI commands |
| `mcp-server/` | MCP server and tool implementations |
| `.taskmaster/` | Example project configuration, PRD, tasks, and reports |
| `docs/` | User guides and command reference |
| `tests/` | Automated test suites |

## Development checks

The package defines `npm test`, `npm run test:coverage`, `npm run test:e2e`, and `npm run format-check`. See [package.json](./package.json) for the full script list. No install, build, test, provider call, or MCP session was run for this README update.

## Documentation

- [Documentation index](./docs/README.md)
- [Tutorial](./docs/tutorial.md)
- [Command reference](./docs/command-reference.md)
- [Configuration](./docs/configuration.md)
- [Contributing](./CONTRIBUTING.md)
- [Changesets](./.changeset/README.md)
