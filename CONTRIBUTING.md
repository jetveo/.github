# Contributing to Jetveo

Thanks for your interest. A few things to know before you start.

## Support expectations

Jetveo is maintained by a small team. Issues and discussions are answered **best effort** — usually within a week, sometimes longer. There is no SLA on the open-source channels. If you need guaranteed response times, see [commercial support](https://jetveo.io) <!-- TODO: link to support page -->.

## Where to go

- **Question / "how do I…"** → [GitHub Discussions](https://github.com/orgs/jetveo/discussions)
- **Bug** → issue in the relevant repo, using the bug template
- **Feature idea** → Discussions first; open an issue once there is a concrete proposal
- **Security** → [SECURITY.md](SECURITY.md), never a public issue

## Before opening a pull request

- For anything beyond a small fix, **open a Discussion or issue first**. We may already be working on it, or have a reason it is not in the roadmap. A PR that implements an unagreed design is likely to be closed, which wastes your time.
- Keep PRs focused: one change, one PR.
- Follow the existing code style; the repo's `.editorconfig` is authoritative. Run `dotnet format` <!-- TODO: confirm tooling --> before pushing.
- Add or update tests for behaviour changes.
- Breaking changes to the YAML metadata format or the public SDK API need an explicit discussion — apps pin SDK versions, and every break is a migration for every user.

## Developer Certificate of Origin

All contributions must be signed off under the [Developer Certificate of Origin 1.1](https://developercertificate.org/). Add `-s` to your commits:

```bash
git commit -s -m "Fix migration diff for renamed references"
```

This certifies that you wrote the change or have the right to submit it under the repository's license. <!-- TODO: if you want to retain relicensing rights under BSL, replace DCO with a CLA (e.g. via cla-assistant) -->

## Licensing

By contributing you agree that your contribution is licensed under the license of the repository you contribute to (BSL 1.1 for runtime/SDK, MIT for CLI, plugin, schemas and examples). See each repo's `LICENSE`.

## Local development

See the `README.md` of each repository for build instructions. The runtime and SDK require .NET <!-- TODO: version -->; the CLI requires Node <!-- TODO: version -->.
