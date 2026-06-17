# Contributing to Tent of Trials

Thank you for your interest in contributing! This guide will help you get started.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Python 3.10+** — required for the build system (`build.py`)
- **Git** — for version control

Depending on which modules you plan to work on, you may also need:

| Module | Language | Tool |
|--------|----------|------|
| backend | Rust | `cargo` (via [rustup](https://rustup.rs)) |
| frontend | TypeScript | `node` + `npm` |
| market | Go | `go` 1.21+ |
| frailbox | C | `gcc`, `make` |
| engine | C++ | `g++`, `cmake`, `make` |
| compliance | Java | `javac` (JDK 17+) |
| v2 services | Ruby | `ruby` |
| nfc-scanner | Lua | `luac` |
| openapi | Haskell | `ghc` |

## Local Setup

```bash
# Fork the repository on GitHub, then clone your fork:
git clone https://github.com/YOUR_USERNAME/zeroeye.git
cd zeroeye

# Run the build to verify your environment:
python3 build.py
```

The build will generate diagnostic artifacts in the `diagnostic/` directory. These are required for PR submissions.

## Making Changes

1. **Create a branch** from `main`:
   ```bash
   git checkout -b your-feature-branch
   ```

2. **Make your changes** — keep them scoped and focused

3. **Run the build** to verify nothing is broken:
   ```bash
   python3 build.py
   ```

4. **Commit** with a clear message:
   ```bash
   git add .
   git commit -m "feat: describe your change"
   ```

5. **Push** to your fork:
   ```bash
   git push origin your-feature-branch
   ```

## Submitting a Pull Request

1. Open a PR from your fork to `lobster-trap/zeroeye`
2. Use the [pull request template](.github/pull_request_template.md) — fill in all sections
3. **Include the diagnostic artifacts** from `build.py`:
   - `diagnostic/build-XXX.logd` (encrypted build log)
   - `diagnostic/build-XXX.json` (build metadata)
4. Reference the issue number in your PR title (e.g., `fix: add type hints to tools (#23)`)

## Code Style

This project uses [EditorConfig](https://editorconfig.org) to maintain consistent formatting. Most editors support it natively or via a plugin. See [`.editorconfig`](.editorconfig) for the full ruleset.

General guidelines:
- Follow existing patterns in the codebase
- Keep changes minimal and scoped to the issue
- No unrelated cleanup or refactoring

## Need Help?

Open an issue on GitHub if you have questions about the contribution process.
