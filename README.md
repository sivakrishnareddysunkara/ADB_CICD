# ADB_CICD

## CI / Continuous Integration

This project uses **GitHub Actions** for CI. Azure Pipelines has been disabled.

| Workflow | Status |
|---|---|
| Python Application CI | [![CI](../../actions/workflows/cicd.yml/badge.svg)](../../actions/workflows/cicd.yml) |

### How it works

- On every push or pull request to `main`, the [GitHub Actions workflow](.github/workflows/cicd.yml) runs automatically.
- The workflow checks out the code, sets up Python 3.10, installs dependencies (if `requirements.txt` exists), and validates Python syntax.
- Azure Pipelines (`azure-pipelines.yml`) has `trigger: none` and `pr: none` set to prevent it from running and causing "no hosted parallelism" errors.

To view CI run history, go to the **Actions** tab of this repository.
