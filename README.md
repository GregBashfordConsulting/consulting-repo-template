# Consulting Project Template

A reusable structure for MATLAB + C scientific computing or DSP projects.  
Designed to keep research prototypes and production code synchronized and testable.

---

## Folder Overview
| Folder | Purpose |
|---------|----------|
| `matlab/` | MATLAB reference implementations, analysis scripts, plots |
| `src/` | C source files (portable signal-processing core) |
| `include/` | C headers |
| `tests/` | Unit tests for C code |
| `docs/` | Design notes, project documentation |
| `data/` | Example datasets (omit large files; use `.gitignore`) |

---

## Quick Start
### Build and test (C)
```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release
ctest --test-dir build --output-on-failure
