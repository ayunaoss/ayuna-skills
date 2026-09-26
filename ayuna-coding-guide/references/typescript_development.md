# TypeScript Development

Follow runtime, package manager, test, lint, and type-check commands defined by repository first.
Detect them from `package.json`, lockfiles, runtime files, and CI.

For an unconfigured project, use active Node.js LTS version 24 or later and `pnpm`.
Verify with `node --version` and `pnpm --version`.

Ask before installing Node.js or pnpm, or changing dependencies or lockfiles.
Install pnpm only when approved:

    ```bash
    curl -fsSL https://get.pnpm.io/install.sh | sh -
    ```

For new projects, set `packageManager` to pnpm in `package.json`.
Run `pnpm install` from project root when dependency installation is required.

For new projects, use Jest for unit tests and oxlint for linting. Install them only when approved:

    ```bash
    # For installing jest in the project
    pnpm add --save-dev jest

    # For installing oxlint in the project
    pnpm add --save-dev oxlint
    ```

Run repository checks. Without project scripts, run `pnpm test` only when a `test` script exists.
Run `pnpm exec oxlint` only when oxlint is installed.
Run `pnpm exec tsc --noEmit` only when TypeScript is installed and `tsconfig.json` exists.

Fix lint and type-checking errors. Fix warnings where possible.
Suppress a warning only with a specific, documented reason.
