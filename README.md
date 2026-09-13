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
npx --yes wrangler@4.131.1 dev --local --port 8799
```

Docker is only needed when rebuilding the WASM artifact. Terraform is optional and
only needed for Cloudflare infrastructure or production deployment.

## Contents

- `SKILL.md` — Rust/WASM-authoritative DLP regex, security, testing, UI, Terraform, and deployment guidance.

Repository: https://github.com/remocloudflare/dlp-cc-regex-skill
