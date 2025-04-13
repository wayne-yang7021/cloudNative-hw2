# GitHub Actions Learning Project

This project is a simple Python application designed to help learn and experiment with **GitHub Actions** and **Continuous Integration (CI)** workflows. It includes a basic Python script, a GitHub Actions CI workflow, and issue templates for bug reports and feature requests.

## Project Goal

The primary goal of this project is to:
- Understand how to set up and configure **GitHub Actions** for CI.
- Practice creating workflows to automate tasks like syntax checking for Python code.
- Learn how to use GitHub issue templates to streamline bug reporting and feature requests.

## Project Structure

- `main.py`: A simple Python script that defines an `add` function and prints the result of adding two numbers.
- `.github/workflows/python-ci.yml`: A GitHub Actions workflow that runs a syntax check on `main.py` for pull requests.
- `.github/ISSUE_TEMPLATE/`: Contains three issue templates:
  - Bug Report (English)
  - Bug Report (Chinese)
  - Feature Request (English)

## Getting Started

### Prerequisites

- Python 3.12 or higher
- A GitHub account to fork/clone this repository

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

2. **Run the Python Script Locally**:
```
bash
python main.py
```

Expected output:
```text
2 + 3 = 5
```

## Explore the CI Workflow

The CI workflow is defined in `.github/workflows/python-ci.yml`.  
It triggers on pull requests and checks the syntax of `main.py` using Python 3.12.

## GitHub Actions Workflow

The project includes a **Python CI** workflow (`.github/workflows/python-ci.yml`) that:
- Runs on `ubuntu-latest`.
- Triggers on `pull_request` events.
- Performs the following steps:
  1. Checks out the repository code.
  2. Sets up Python 3.12.
  3. Installs dependencies (upgrades `pip`).
  4. Runs a syntax check on `main.py` using `py_compile`.

To see the workflow in action:
1. Create a pull request with changes to `main.py`.
2. Check the "Actions" tab in your GitHub repository to view the workflow logs.

## Issue Templates

This project includes three issue templates to streamline contributions:
- **Bug Report (English)**: For reporting bugs in the project with details like reproduction steps, expected behavior, and environment.
- **Bug Report (Chinese)**: A translated version of the bug report template with fields for occurrence time, platform environment, and more.
- **Feature Request (English)**: For suggesting new features or improvements, including problem description and proposed solutions.

To use them:
1. Go to the "Issues" tab in the repository.
2. Click "New Issue" and select the appropriate template.

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes.
4. Test locally and ensure the CI workflow passes.
5. Submit a pull request.

Please use the issue templates to report bugs or suggest features before submitting code.