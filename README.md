# ⚙️ Python CI/CD Pipeline with GitHub Actions

> A hands-on CI/CD project demonstrating automated **linting and testing for a Python application using GitHub Actions and pytest**.

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI/CD-2088FF?style=flat&logo=github-actions&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-testing-0A9EDC?style=flat&logo=pytest&logoColor=white)
![Flake8](https://img.shields.io/badge/Flake8-linting-4B8BBE?style=flat)

## 📌 Overview

This project is a practical introduction to **Continuous Integration (CI)** using GitHub Actions. Every push to `main` and every pull request targeting `main` triggers an automated workflow that installs the Python dependencies, runs code-quality checks with Flake8, and executes the pytest test suite.

The project demonstrates the core CI workflow used in modern software development:

```text
Developer Push / Pull Request
            ↓
      GitHub Actions
            ↓
     Checkout Repository
            ↓
       Setup Python 3.12
            ↓
     Install Dependencies
            ↓
        Run Flake8
            ↓
        Run pytest
            ↓
       CI Pass / Fail
```

## ✨ What This Project Demonstrates

- ⚙️ Creating a GitHub Actions CI workflow
- 🐍 Configuring a Python 3.12 CI environment
- 🧪 Automating tests with pytest
- 🔍 Automating Python linting with Flake8
- 🔀 Running CI on both pushes and pull requests
- 📦 Installing project dependencies automatically in CI
- 🚦 Using CI results to catch issues before changes are merged

## 🛠️ Tech Stack

| Area | Technology |
|---|---|
| Language | Python 3.12 |
| CI/CD | GitHub Actions |
| Testing | pytest |
| Linting | Flake8 |
| Version Control | Git / GitHub |

## 📁 Project Structure

```text
ci-cd-day4/
├── .github/
│   └── workflows/
│       └── ci.yml          # GitHub Actions CI workflow
├── tests/
│   └── test_app.py         # Automated tests
├── app.py                  # Application functions
├── requirements.txt        # Python dependencies
└── README.md
```

## 🔄 CI Workflow

The workflow is configured to run on:

- Pushes to `main`
- Pull requests targeting `main`

The pipeline performs these steps:

1. **Checkout** — retrieves the repository code.
2. **Setup Python** — configures Python 3.12.
3. **Install dependencies** — installs the project's Python packages.
4. **Linting** — runs Flake8 against the application and test files.
5. **Testing** — runs the pytest test suite.

The workflow configuration is defined in `.github/workflows/ci.yml`. fileciteturn15file0L2-L6

## 🧪 Testing

The project contains pytest tests covering the application's arithmetic functions, including addition, subtraction, and multiplication. fileciteturn18file0L2-L6

Run the tests locally with:

```bash
pip install -r requirements.txt
python -m pytest -v
```

## 🔍 Code Quality

Flake8 is used to check the application and test files as part of the CI workflow. The project includes Flake8 and pytest in its dependency set. fileciteturn16file0L2-L6

Run linting locally with:

```bash
flake8 app.py tests
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/rohit78u/ci-cd-day4.git
cd ci-cd-day4
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
```

**Windows:**

```bash
venv\Scripts\activate
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run tests

```bash
python -m pytest -v
```

### 5. Run linting

```bash
flake8 app.py tests
```

## 🎯 Learning Outcomes

This project provides hands-on experience with:

- Continuous Integration concepts
- GitHub Actions workflow configuration
- Automated testing
- Automated code-quality checks
- Pull-request validation
- Python project dependency management
- Basic CI troubleshooting

## 📌 Project Status

**Completed:** Core Python CI pipeline with automated linting and testing through GitHub Actions.

## 🔮 Future Improvements

- Add test coverage reporting
- Add a build/package validation stage
- Add dependency caching
- Add CI status badge
- Extend the pipeline to multiple Python versions
- Add deployment automation as a separate CD stage

## 📄 License

MIT
