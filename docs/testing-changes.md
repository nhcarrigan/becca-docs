# Testing Your Changes

Before submitting your code changes in a pull request, you should always run the tests locally. There are a few validation steps that are checked.

## Code Style and Formatting

We use ESLint and Prettier to enforce our code standards and styling. You can run the linter locally with:

```bash
pnpm run lint
```

Our linter uses our shared [configuration](https://github.com/naomi-lgbt/eslint-config/blob/main/index.js), with a few [overrides](https://github.com/BeccaLyria/discord-bot/blob/main/.eslintrc.json) specific to Becca.

## Unit Tests

We use Chai's `assert` API to run our unit tests. You can verify the tests are passing with:

```bash
pnpm run test
```

If you are adding new files or exported functions, you should include a test for them. If you are fixing a bug, you should include a regression test that confirms the bug is fixed.

## Test Coverage

We are in the process of adding checks to validate test coverage. You can see the current coverage by running:

```bash
pnpm run test:coverage
```

The coverage report will display in the terminal, and will also be generated as a website available in the `coverage` directory. Changes to code should improve or maintain the current coverage percentage.

## Dead Code and Unused Dependencies

We use `knip` to check for unused exports, files, and dependencies. You can run the check with:

```bash
pnpm run clean
```

This check should pass before making a pull request. It is possible that a failure is a false positive - however, any changes to the configuration should be discussed in our Discord server to confirm that it is actually a false positive.
