# <Project Name>

Modern C++ template using CMake with a library target, CLI app target, and test target.

## Status
- Stage: Draft | Active | Stable | Deprecated
- Owner: <Owner>
- License: <License Name>
- Visibility: Public | Private | Internal
- Reason: <Why this visibility level is correct>
- Promotion criteria to Public: <What must be true before public release>

## What This Project Is
- A clean starter for C++ projects that need predictable structure and CI.
- Not a full framework or opinionated application architecture.

## Quickstart

### Prerequisites
- CMake >= 3.20
- C++20 compiler

### Build, Test, Run
```bash
cmake -S . -B build -DENABLE_TESTS=ON -DBUILD_APPS=ON
cmake --build build
ctest --test-dir build --output-on-failure
./build/ProjectName_cli
```

### Formatting Enforcement
```bash
git config core.hooksPath .githooks
```

```bash
clang-format -i apps/project_name_cli.cpp include/project_name.hpp src/project_name.cpp tests/test_placeholder.cpp
```

## Repository Layout
- `include/` public headers
- `src/` library implementation
- `apps/` executable entrypoints
- `tests/` test targets
- `docs/` project documentation
- `examples/` optional sample programs
- `tools/` helper scripts

## Documentation
- [Overview](docs/overview.md)
- [Architecture](docs/architecture.md)
- [ADRs](docs/adr/)

## Contributing
See `CONTRIBUTING.md`.
