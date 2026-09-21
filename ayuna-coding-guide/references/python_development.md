# Python Development

Follow runtime, package manager, test, lint, and type-check commands defined by repository first.
Prefer project virtual environment over system Python.

For an unconfigured project, require Python 3.12 or later. Verify with `python --version`,
set `target-version = "py312"` in `pyproject.toml`, and use uv.
Verify uv with `uv self version`.

Ask before installing uv or changing dependencies or lockfiles. When dependency synchronization is required,
run repository command; otherwise run `uv sync --all-groups --all-packages` from project root.

For new projects, use ruff. Install it only when approved:

    ```bash
    uv add --dev ruff
    ```

Run repository checks. Without project scripts, run `uv run ruff check .` and
`uv run ruff format --check .` only when ruff is configured or installed.
Request approval before adding ruff. Run configured type checker and tests when present.

Fix lint and type-checking errors. Fix warnings where possible.
Suppress a warning only with a specific, documented reason.

## Install uv

* Add `${HOME}/.local/bin` to your PATH if it is not already included.
* Run command below only after approval:

    ```bash
    curl -LsSf https://astral.sh/uv/install.sh | env UV_INSTALL_DIR="${HOME}/.local" UV_NO_MODIFY_PATH=1 sh
    ```
