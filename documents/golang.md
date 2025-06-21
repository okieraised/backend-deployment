## 🧩 Useful Go (Golang) Commands

### 🔹 Setup and Environment

| Command | Description |
|--------|-------------|
| `go version` | Print Go version |
| `go env` | Show Go environment variables |
| `go env -w <VAR>=<value>` | Set a Go environment variable (e.g., `GO111MODULE=on`) |
| `which go` | Find path to Go binary |

---

### 🔹 Project Initialization & Modules

| Command | Description |
|--------|-------------|
| `go mod init <module-name>` | Initialize a new Go module |
| `go mod tidy` | Add/remove dependencies to match imports |
| `go mod download` | Download all dependencies |
| `go mod vendor` | Create `vendor/` directory with dependencies |
| `go list -m all` | List all modules in the build list |
| `go get <module>@version` | Add/update a module dependency |

---

### 🔹 Building and Running

| Command | Description |
|--------|-------------|
| `go run <file>.go` | Run a Go file |
| `go run .` | Run main package in current directory |
| `go build` | Compile the Go package in current directory |
| `go build -o appname` | Build with a custom output binary name |
| `go install` | Compile and install to `$GOPATH/bin` |

---

### 🔹 Testing

| Command | Description |
|--------|-------------|
| `go test` | Run tests in current package |
| `go test ./...` | Run all tests recursively |
| `go test -v` | Verbose test output |
| `go test -run <TestName>` | Run a specific test |
| `go test -cover` | Show test coverage |
| `go test -bench .` | Run benchmarks |

---

### 🔹 Formatting and Linting

| Command | Description |
|--------|-------------|
| `go fmt ./...` | Format all `.go` files recursively |
| `go vet ./...` | Report suspicious code |
| `golint ./...` | Run linter (if installed via `go install golang.org/x/lint/golint@latest`) |

---

### 🔹 Code Navigation & Docs

| Command | Description |
|--------|-------------|
| `go doc <package>` | Show documentation for a package |
| `go doc <package>.<function>` | Show doc for specific function |
| `go list ./...` | List all packages in module |

---

### 🔹 Compilation for Other Platforms

| Command | Description |
|--------|-------------|
| `GOOS=linux GOARCH=amd64 go build -o appname` | Build for Linux AMD64 |
| `GOOS=windows GOARCH=amd64 go build -o appname.exe` | Build for Windows |
| `GOOS=darwin GOARCH=arm64 go build` | Build for macOS M1/M2 |

---

### 🔹 Common Tools (Install with `go install`)

| Tool | Description |
|------|-------------|
| `golangci-lint` | All-in-one linting tool |
| `godoc` | Local documentation server |
| `staticcheck` | Advanced linter |
| `mockgen` | Interface mocking tool for tests |

---

### 🔹 Example: `Makefile`

```makefile
APP_NAME := myapp

build:
	go build -o $(APP_NAME) .

run:
	go run .

test:
	go test ./... -v

fmt:
	go fmt ./...

clean:
	rm -f $(APP_NAME)


