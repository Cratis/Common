# Common

Shared configuration for all repositories in the [Cratis](https://github.com/Cratis) organization.

This repository holds the baseline every Cratis repository starts from, so conventions are defined once and stay consistent across the organization.

## What is shared here

- **AI contract** — repositories commit the Cratis AI contract instead of a synchronized corpus: `.cratis/PROJECT.md` (project context), `.cratis/ai.json` (profile subscription), and the `AGENTS.md`/`CLAUDE.md`/`GEMINI.md` bootstraps. Shared skills arrive through the Cratis AI marketplace plugins; see the [harness guide](https://www.cratis.io/ai/harnesses/).
- **GitHub templates** — issue templates and the pull request template under [`.github/`](.github).
- **CodeQL configuration** — the shared [CodeQL config](.github/codeql/codeql-config.yml) used for code scanning.
- **Standard workflow wrappers** — thin caller workflows (package updates, PR artifact cleanup, deployment approval) that delegate to the reusable workflows in [Cratis/Workflows](https://github.com/Cratis/Workflows).

## Who consumes it

Every repository in the Cratis organization. The workflow wrappers themselves are bootstrapped into repositories from [Cratis/Workflows](https://github.com/Cratis/Workflows). AI behavior is no longer synchronized between repositories: each repository commits its own `.cratis/` AI contract, and shared skills arrive through the Cratis AI marketplace plugins.

Part of [Cratis](https://www.cratis.io) — free, MIT-licensed tools for building event-sourced and CQRS applications.

## License

[MIT](LICENSE)
