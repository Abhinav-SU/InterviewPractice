# AGENTS.md

Guidance for AI agents working in this repository.

## Repository status

**InterviewPractice** is currently a placeholder repository. It contains only `README.md` (title: "InterviewPractice"). There is no application source, dependency manifests, Docker configuration, CI workflows, or service definitions yet.

Until application code is added, there are no lint, test, build, or dev-server commands defined in this repo.

## Cursor Cloud specific instructions

### Services

| Service | Required | Notes |
|---------|----------|-------|
| *(none)* | — | No runnable application or backend in the repo yet |

### VM update script

No dependency refresh is needed on startup. The configured update script is a no-op (`true`) because there are no `package.json`, `requirements.txt`, or similar manifests.

### When code is added

After the first stack is committed (e.g. Node, Python, Go), update:

1. The VM **update script** (via SetupVmEnvironment) to match the package manager (`npm install`, `pnpm install`, `uv sync`, etc.).
2. This section with concrete dev/lint/test commands from `README.md` or package scripts.
3. Any non-obvious startup steps (ports, env vars, databases) here—not in the update script.

### Tooling available on the Cloud VM

The VM image includes common runtimes (e.g. Node.js, Python 3, Go, Rust) for when this repo is expanded. Use whatever stack the project adopts; do not assume one is already chosen.

### Git

- Default branch: `main`
- Remote: `origin` → GitHub `Abhinav-SU/InterviewPractice`
