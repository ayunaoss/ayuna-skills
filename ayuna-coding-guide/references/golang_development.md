# Go Development

Follow Go version and validation commands defined by repository first.
Otherwise, verify `go` with `command -v go` and `go version`; require Go 1.27.0 or later.

Ask before installing tools. Use project-pinned tool versions when available.
For an unconfigured project, use tools below.

Run repository validation commands. Without project commands, run `go test ./...`,
`go vet ./...`, `staticcheck ./...`, and `revive ./...` as applicable.
Run `goimports -w path/to/file.go` only on changed Go files.

For monorepos with `go.work`, run `go work sync` only when workspace dependencies change.

## Go Ecosystem Tools

* **revive**: Code linting. Install when approved:

    ```bash
    go install github.com/mgechev/revive@latest
    ```

* **goimports**: Fixes imports and runs `gofmt`. Install when approved:

    ```bash
    go install golang.org/x/tools/cmd/goimports@latest
    ```

* **staticcheck**: Supplements `go vet`; detects bugs, performance issues, and deadlocks. Install when approved:

    ```bash
    go install honnef.co/go/tools/cmd/staticcheck@latest
    ```
