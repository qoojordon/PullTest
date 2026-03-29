# AGENTS.md

## Cursor Cloud specific instructions

This is a minimal single-file C++ project ("PullTest"). There are no package managers, databases, or external services.

### Build & Run

Build and run commands match the CI workflow in `.github/workflows/ci.yml`:

```
g++ -std=c++17 -Wall -Wextra -o app PullTest/main.cpp
./app
```

### Lint

There is no dedicated linter. Compiler warnings (`-Wall -Wextra`) serve as the lint check. The existing unused-parameter warnings on `argc`/`argv` are known and present in CI.

### Tests

There is no test framework. The CI "test" is simply compiling and running the binary, verifying it exits 0.
