# Task Master documentation

Start with the [root README](../README.md) for repository scope, install overview, source attribution, license, and safety notes.

## User guides

- [Tutorial](tutorial.md): install Task Master, connect an MCP client or use the CLI, and initialize a project.
- [Configuration](configuration.md): project configuration, model selection, and API-key setup.
- [Command reference](command-reference.md): CLI command examples.
- [Task structure](task-structure.md): task and subtask data.
- [Examples](examples.md): sample interactions and workflows.
- [Migration guide](migration-guide.md): migration guidance.
- [Models](models.md): supported model configuration.

## Project references

- [CLI entry point](../bin/task-master.js)
- [Task operations and commands](../scripts/modules/)
- [MCP server](../mcp-server/server.js)
- [Package scripts and license metadata](../package.json)
- [License text](../LICENSE)

The package metadata identifies [eyaltoledano/claude-task-master](https://github.com/eyaltoledano/claude-task-master) as the upstream repository. The license includes a Commons Clause. Review [LICENSE](../LICENSE) before redistribution or commercial use.

Task generation and analysis send project context to the configured AI provider. Protect credentials and review provider data handling and usage costs.