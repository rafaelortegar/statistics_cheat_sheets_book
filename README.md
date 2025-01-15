# Python Cheat Sheets Book Repository

Welcome to the **Python Cheat Sheets Book** repository! This project is designed to help you build and serve Jupyter Books while working with Jupyter Notebooks, Docker, Poetry, Pyenv, Pre-Commit, and GitHub Actions. Follow this guide to set up and contribute to the project.

---

## **Table of Contents**

- [Python Cheat Sheets Book Repository](#python-cheat-sheets-book-repository)
  - [**Table of Contents**](#table-of-contents)
  - [**Features**](#features)
  - [**Folder Structure**](#folder-structure)
  - [**Initial Setup**](#initial-setup)
    - [**On Linux**](#on-linux)
    - [**On Windows**](#on-windows)
  - [**Using This Repo**](#using-this-repo)
    - [**Run with Docker**](#run-with-docker)
    - [**Run Locally with Poetry**](#run-locally-with-poetry)
    - [**Run Tests**](#run-tests)
  - [**Updating a Package**](#updating-a-package)
  - [**Contributing**](#contributing)
  - [**GitHub Actions**](#github-actions)

---

## **Features**

- **Docker**: Containerized environment for consistent development.
- **Poetry**: Dependency and environment management.
- **Jupyter Book**: Generate structured documentation from notebooks and markdown files.
- **Jupyter Notebooks**: Interactive notebooks for development and analysis.
- **Pre-Commit Hooks**: Ensure code quality and consistency.
- **Pyenv**: Manage Python versions.
- **GitHub Actions**: Automated workflows for linting, testing, and book building.
- **Tests**: Unit tests to validate the functionality of scripts.

---

## **Folder Structure**

```plaintext
.
├── LICENSE                  # License file for the project
├── README.md                # Main documentation for the repository
├── README_1.md              # Additional or alternate README
├── book                     # Jupyter Book content
│   ├── _build               # Built files for the Jupyter Book
│   │   ├── html             # HTML output
│   │   └── jupyter_execute  # Executed notebooks
│   ├── _config.yml          # Global configuration for the Jupyter Book
│   ├── _toc.yml             # Table of contents for the Jupyter Book
│   ├── intro.md             # Introduction chapter
│   ├── logo.png             # Logo for the book
│   ├── markdown-notebooks.md  # Example Markdown documentation
│   ├── markdown.md          # Example Markdown file
│   ├── notebooks.ipynb      # Example Jupyter Notebook
│   ├── references.bib       # References used in the book
│   └── requirements.txt     # Dependencies for the Jupyter Book
├── cheat_sheets_book        # Main source code for the cheat sheets book
├── dockerfiles              # Docker configurations
│   └── Dockerfile_jupyter_book_dev  # Dockerfile for the development environment
├── notebooks                # Additional Jupyter Notebooks
├── poetry.lock              # Poetry lock file for dependencies
├── pyproject.toml           # Poetry configuration file
├── pytest.ini               # Configuration for pytest
├── requirements.txt         # Dependencies for non-Poetry users
└── tests                    # Unit tests for the project
    └── test_example.py      # Example test case
```

---

## **Initial Setup**

### **On Linux**

1. **Install Pyenv**:
   ```bash
   curl https://pyenv.run | bash
   export PYENV_ROOT="$HOME/.pyenv"
   export PATH="$PYENV_ROOT/bin:$PATH"
   eval "$(pyenv init --path)"
   eval "$(pyenv virtualenv-init -)"
   exec $SHELL
   ```

2. **Install Python**:
   ```bash
   pyenv install 3.10.12
   pyenv virtualenv 3.10.12 python_cheat_sheets_book
   pyenv activate python_cheat_sheets_book
   ```

3. **Install Poetry**:
   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   export PATH="$HOME/.local/bin:$PATH"
   exec $SHELL
   ```

4. **Install Dependencies**:
   ```bash
   poetry install
   ```

### **On Windows**

1. **Install Pyenv-Win**:
   ```powershell
   pip install pyenv-win
   ```
   Add the following to your system PATH:
   - `%USERPROFILE%\.pyenv\pyenv-win\bin`
   - `%USERPROFILE%\.pyenv\pyenv-win\shims`

2. **Install Python**:
   ```powershell
   pyenv install 3.10.12
   pyenv virtualenv 3.10.12 python_cheat_sheets_book
   pyenv activate python_cheat_sheets_book
   ```

3. **Install Poetry**:
   ```powershell
   (Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -
   ```

4. **Install Dependencies**:
   ```powershell
   poetry install
   ```

---

## **Using This Repo**

### **Run with Docker**

1. **Build the Docker Image**:
   ```bash
   docker build -t jupyter-book-dev -f dockerfiles/Dockerfile_jupyter_book_dev .
   ```

2. **Run the Container**:
   ```bash
   docker run -it -p 8888:8888 -p 8000:8000 -v $(pwd):/notebooks jupyter-book-dev
   ```

3. **Access the Services**:
   - Jupyter Notebook: [http://localhost:8888](http://localhost:8888)
   - Jupyter Book: [http://localhost:8000](http://localhost:8000)

### **Run Locally with Poetry**

1. Activate the environment:
   ```bash
   poetry shell
   ```

2. Run Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Build the Jupyter Book:
   ```bash
   jupyter-book build book/
   ```

### **Run Tests**

1. Execute all tests:
   ```bash
   pytest
   ```

---

## **Updating a Package**

1. **Update the Dependency**:
   ```bash
   poetry add <package>@<version>
   ```

2. **Rebuild the Docker Image**:
   ```bash
   docker build -t jupyter-book-dev -f dockerfiles/Dockerfile_jupyter_book_dev .
   ```

3. **Run the Updated Container**:
   ```bash
   docker run -it -p 8888:8888 -p 8000:8000 -v $(pwd):/notebooks jupyter-book-dev
   ```

---

## **Contributing**

1. **Fork the Repo**: Clone your fork locally.
2. **Install Pre-Commit Hooks**:
   ```bash
   pre-commit install
   ```
3. **Create a Feature Branch**:
   ```bash
   git checkout -b feature/<feature-name>
   ```
4. **Make Changes**: Commit with meaningful messages.
5. **Run Tests**:
   ```bash
   pytest
   ```
6. **Push and Create a Pull Request**.

---

## **GitHub Actions**

This repository includes workflows for:
- **Linting**: Ensures code quality with tools like Black and Flake8.
- **Testing**: Runs unit tests automatically.
- **Book Building**: Builds and deploys the Jupyter Book to GitHub Pages.

---

If you encounter any issues or have questions, feel free to open an issue or contribute to the project!
