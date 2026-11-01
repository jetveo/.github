# Security Policy

## Reporting a vulnerability

Please **do not** open a public issue for security problems.

Report privately via one of:

- GitHub: **Security → Report a vulnerability** on the affected repository (private advisory)
- E-mail: **security@jetveo.io** <!-- TODO: create the mailbox before publishing -->

Include: affected repo and version (SDK version from `.jvproj`, `jv --version`), steps to reproduce, and impact as you understand it. A proof of concept helps; exploitation of production systems does not — please stop at demonstrating the issue.

## What to expect

| Step | Target |
|------|--------|
| Acknowledgement | within 3 business days |
| Initial assessment and severity | within 10 business days |
| Fix for Critical / High | released as a patch of every [supported SDK version](#supported-versions) |
| Public advisory | after the fix is available, credited to you unless you prefer otherwise |

We will keep you informed throughout. If you have not heard from us within the targets above, please follow up — e-mail does get lost.

## Supported versions

<!-- TODO: fill once the LTS policy exists; this is a placeholder structure -->

| SDK version | Supported |
|-------------|-----------|
| latest minor | yes |
| previous minor | security fixes only, for 6 months after the next minor |
| older | no — please upgrade |

Applications pin their SDK version in `.jvproj`; upgrading is an explicit step with a schema diff. See the docs for the upgrade guide.

## Scope

In scope: the runtime, SDK, language server, `jv` CLI, Claude Code plugin, and Jetveo Cloud (`*.jetveo.io`) <!-- TODO: confirm cloud domains -->.

Out of scope: applications built by third parties on Jetveo, social engineering, denial of service by volume, and findings from automated scanners without a demonstrated impact.

## Safe harbour

We will not pursue legal action against researchers who act in good faith, respect user privacy, do not exfiltrate data beyond what is needed to demonstrate the issue, and give us reasonable time to fix before disclosure.
