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

## Use locally

Install this skill in OpenCode. It provides the project guidance automatically;
users do not need to install npm, Terraform, Docker, or Cloudflare credentials just
to load the skill.

For the runnable DLP Builder, use the public demo or the application repository's
own local-development instructions. This skill repository contains guidance only,
not the Worker runtime or its dependencies.

## Contents

- `SKILL.md` — Rust/WASM-authoritative DLP regex, security, testing, UI, Terraform, and deployment guidance.

Repository: https://github.com/remocloudflare/dlp-cc-regex-skill
