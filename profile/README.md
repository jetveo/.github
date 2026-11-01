# Jetveo

**Runtime and SDK for long-lived business applications, built for AI-assisted development.**

Define your data model, workflows and views as YAML in git. Write business logic in plain C#.
Let Claude Code (or any agent) build the app — the runtime keeps it secure, migratable and upgradable for years.

```bash
npx @jetveo/cli init my-app      # scaffold a project
cd my-app
jv run                           # local instance on SQLite
jv validate                      # Roslyn-backed checks for YAML + C#
jv deploy                        # ship to Jetveo Cloud (or self-host)
```

<!-- TODO: replace with a 20–30 s GIF: Claude Code adds an entity + workflow, app reloads -->

## Why not just .NET?

- **Schema migrations are generated, not written.** Rename a field, keep the data. Every release ships a schema snapshot; deploy diffs it against the database.
- **Permissions live in the runtime, not in generated code.** Row-level access, audit log and workflow guards are enforced below the application layer — whatever the AI writes.
- **Upgrades are explicit.** Each app pins its SDK version in `.jvproj`. A platform release never breaks an app; you upgrade when you decide to.
- **AI-native tooling.** JSON Schemas for every metadata type, a language server exposed over MCP, and a Claude Code plugin with the platform docs built in.

## Repositories

| Repo | What it is |
|------|------------|
| [jetveo](https://github.com/jetveo/jetveo) | Runtime, SDK and language server |
| [cli](https://github.com/jetveo/cli) | `jv` — the Jetveo CLI (`@jetveo/cli` on npm) |
| [examples](https://github.com/jetveo/examples) | Sample applications |
| [docs](https://github.com/jetveo/docs) | Documentation source — [jetveo.io/docs](https://jetveo.io/docs) <!-- TODO: confirm URL --> |
| [claude-plugin](https://github.com/jetveo/claude-plugin) | Claude Code plugin: skills, schemas, platform reference |

## License

Self-hosting is free. Runtime and SDK are released under the **Business Source License 1.1**
and convert to **Apache 2.0** after <!-- TODO: 2/3/4 --> years. The only restriction: you may not offer Jetveo
itself as a hosted platform to third parties. Hosting apps you build for your own customers is explicitly allowed.
CLI, plugin, schemas and examples are **MIT**.

## Talk to us

- Questions and ideas → [GitHub Discussions](https://github.com/orgs/jetveo/discussions)
- Bugs → issues in the relevant repo
- Security → see [SECURITY.md](https://github.com/jetveo/.github/blob/main/SECURITY.md)
- Managed hosting, SLA and partner program → [jetveo.io](https://jetveo.io)

Built in the Czech Republic. Running production ERP, WMS and invoicing systems since <!-- TODO: year -->.
