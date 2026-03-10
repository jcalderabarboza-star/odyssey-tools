# CLAUDE.md — odyssey-tools

This file provides guidance for AI assistants (Claude Code and others) working in this repository.

## Project Overview

**odyssey-tools** is a nascent repository. At the time of this writing it contains only a top-level `README.md` and no source code, configuration, or build infrastructure. This document will be updated as the project grows.

Repository remote: `http://local_proxy@127.0.0.1:37305/git/jcalderabarboza-star/odyssey-tools`

---

## Repository Structure

```
odyssey-tools/
├── CLAUDE.md        # AI assistant guidance (this file)
└── README.md        # Project description
```

As source code, tests, and tooling are added, update this tree accordingly.

---

## Git Workflow

### Branches

- `master` — default/stable branch
- `origin/main` — remote main branch
- Feature branches should follow the pattern: `<username>/<short-description>` or `claude/<task-slug>` for AI-generated branches

### Branch naming for Claude sessions

Claude Code task branches **must** match the pattern:

```
claude/<task-slug>-<session-id>
```

Pushing to any other branch without explicit user permission is prohibited.

### Commit messages

Use clear, imperative-style commit messages:

```
Add user authentication module
Fix null pointer in data parser
Update CLAUDE.md with project structure
```

### Push workflow

```bash
git push -u origin <branch-name>
```

If a push fails due to network errors, retry up to 4 times with exponential back-off (2 s, 4 s, 8 s, 16 s). Do **not** retry on 403 errors — a 403 indicates a branch-name mismatch.

---

## Development Conventions (to be established)

The following sections are placeholders. Fill them in once the project's language, framework, and tooling are decided.

### Language & Runtime

_Not yet determined._

### Dependency management

_Not yet determined._

### Code style & linting

_Not yet configured._

### Testing

_Not yet configured._

### Build & run

_Not yet configured._

---

## Working with this Repository as an AI Assistant

1. **Read before editing.** Always read a file before modifying it.
2. **Minimal changes.** Only make changes that are directly requested or clearly necessary. Do not refactor, add comments, or clean up surrounding code unless asked.
3. **No speculative features.** Do not add error handling, fallbacks, or abstractions for scenarios that don't exist yet.
4. **Security.** Never introduce command injection, SQL injection, XSS, or other OWASP Top 10 vulnerabilities. Fix any discovered vulnerabilities immediately.
5. **Confirm destructive actions.** Force-pushes, hard resets, branch deletions, and file deletions require explicit user confirmation.
6. **Keep this file up to date.** When significant structural or workflow changes are made to the repository, update this document.

---

## Updating This File

When the project gains real content, update the following sections:

- [ ] Repository structure tree
- [ ] Language & runtime
- [ ] Dependency management commands
- [ ] Linting / formatting commands and configuration files
- [ ] Test commands and framework
- [ ] Build & run instructions
- [ ] Environment variables / secrets handling
- [ ] CI/CD pipeline description
