# dlp-cc-regex OpenCode skill

A reusable OpenCode skill for the Cloudflare DLP Regex Builder.

## Install for a project

Copy `.opencode/skills/dlp-cc-regex/` into the project root, or clone this repository and add its path to `opencode.json`:

```json
{
  "skills": ["/path/to/dlp-cc-regex-skill/.opencode/skills"]
}
```

OpenCode also discovers `.opencode/skills/<name>/SKILL.md` when this repository is used as the project directory.

## Local use without Terraform

Terraform is not required for local development. The builder is stateless and the
Rust/WASM validator is committed in the application repository:

```bash
npm test
npm run dev
```

`npm run dev` starts the local-only builder at `http://localhost:8799`.
No Terraform or Cloudflare credentials are required. `npm run dev:remote` is
available only when a remote Wrangler session is intentionally needed.

Docker is only needed when rebuilding the WASM artifact. Terraform is optional and
only needed for Cloudflare infrastructure or production deployment.

## Contents

- `SKILL.md` — Rust/WASM-authoritative DLP regex, security, testing, UI, Terraform, and deployment guidance.

Repository: https://github.com/remocloudflare/dlp-cc-regex-skill
