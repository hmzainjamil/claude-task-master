# Task Master test suites

This directory contains unit, integration, and end-to-end test files. The package scripts define the supported commands.

## Run checks

From the repository root:

```sh
npm test
npm run test:coverage
npm run test:e2e
```

- `npm test` runs Jest.
- `npm run test:coverage` runs the Jest coverage script.
- `npm run test:e2e` invokes `tests/e2e/run_e2e.sh`.

See [package.json](../package.json) for additional scripts and [test setup](./setup.js) for shared configuration.

This documentation update did not run any test command or verify a coverage percentage.