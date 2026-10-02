# Task Master scripts

The CLI entry point in `bin/task-master.js` delegates commands to files under this directory. The scripts initialize a project, parse PRDs, update task data, and coordinate model-backed operations.

## Source map

- [`init.js`](./init.js): initialize the `.taskmaster/` project structure.
- [`dev.js`](./dev.js): development CLI entry used by the package binary.
- [`modules/commands.js`](./modules/commands.js): register CLI commands.
- [`modules/task-manager.js`](./modules/task-manager.js): task and subtask operations.
- [`modules/dependency-manager.js`](./modules/dependency-manager.js): dependency operations.
- [`modules/config-manager.js`](./modules/config-manager.js): project model/configuration and credentials.
- [`modules/ai-services-unified.js`](./modules/ai-services-unified.js): provider requests.
- [`example_prd.txt`](./example_prd.txt): example input format.

## Side effects

Task commands can create or modify files under the project `.taskmaster/` directory. Generation, expansion, analysis, or research commands can send project context to the configured model provider and may incur provider charges. Review the project root and configuration before running a command.

See the [configuration guide](../docs/configuration.md) and the [root README](../README.md).