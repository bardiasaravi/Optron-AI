# Optron AI — Official Website Hosting and Repository Roles

**Effective:** 18 October 2026  
**Status:** Independent public-site migration completed and verified.

## Official websites

- **[optron.app](https://optron.app)** and **[www.optron.app](https://www.optron.app)** — official Optron AI public marketing, identity, product information and early-access website.
- **[optronlabs.com](https://optronlabs.com)** and **[www.optronlabs.com](https://www.optronlabs.com)** — separate, private operational application / approved-access environment.

The official public website and the operational application now have **separate Git repositories and independent Vercel projects**. Both public-site domain names were migrated and tested on 2026-10-18; both operational application domain names stayed on the original application project.

## GitHub repositories: do not confuse their purpose

| Repository | Visibility | Purpose |
|---|---|---|
| `bardiasaravi/Optron-AI` | PUBLIC | Public identity, Big Book and documentation (this repository). **Not the website's deployment source.** |
| `bardiasaravi/optron-public-site` | PRIVATE | Source of Truth for the official public website `optron.app`. |
| `bardiasaravi/optron` | PRIVATE | Source of Truth for the application/runtime, served through `optronlabs.com`. |

**Clarification:** Public website accessibility does not imply that its repository is public. Neither private repository was opened as part of this migration.

## Maintenance principles

- Build and release public website updates from the **independent private website repository**, not the application repository or this Big Book.
- Maintain Optron Labs application deployments independently; do not overwrite the public website with the Labs sign-in page or overwrite Labs with its marketing website.
- Public-site forms may call a separately owned, restricted Labs endpoint. Never transfer application credentials, sensitive environment configuration, or private runtime code to the website repository.
- The public Big Book is for public documentation and brand identity, not for private runtime source code.
- Keep deployment, DNS and domain migration changes governed, tested and reversible.

**Verification scope:** both public domains were reachable and served expected content after cutover; the restricted private Labs application remained attached to its existing Vercel project. Live form-submission and recovery-drill claims must be assessed independently; they are not implied by the migration's success.

**For authorized Optron engineering teams:** the private GitHub repository `bardiasaravi/optron-public-site` contains the detailed, audited cutover runbook and verified project identifiers.
