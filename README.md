# Common

Shared configuration for all repositories in the [Cratis](https://github.com/Cratis) organization.

This repository holds the baseline every Cratis repository starts from, so conventions are defined once and stay consistent across the organization.

## What is shared here

- **AI-assistant configuration** — [`.ai/`](.ai/README.md) is the single source of truth for rules, agents, prompts, skills, and hooks used by AI coding assistants. `.claude/`, `.agents/`, `AGENTS.md`, and the `.github/` instruction/prompt/skill files are generated adapters that surface the same content to each tool.
- **GitHub templates** — issue templates and the pull request template under [`.github/`](.github).
- **CodeQL configuration** — the shared [CodeQL config](.github/codeql/codeql-config.yml) used for code scanning.
- **Standard workflow wrappers** — thin caller workflows (package updates, PR artifact cleanup, Copilot instruction sync and propagation, deployment approval) that delegate to the reusable workflows in [Cratis/Workflows](https://github.com/Cratis/Workflows).

## Who consumes it

Every repository in the Cratis organization. Changes to the shared instruction files on `main` are propagated to the other Cratis repositories by the [propagate workflow](.github/workflows/propagate-copilot-instructions.yml), and instruction changes made elsewhere can be synced back in through the [sync workflow](.github/workflows/sync-copilot-instructions.yml). The workflow wrappers themselves are bootstrapped into repositories from [Cratis/Workflows](https://github.com/Cratis/Workflows).

Part of [Cratis](https://www.cratis.io) — free, MIT-licensed tools for building event-sourced and CQRS applications.

## License

[MIT](LICENSE)
