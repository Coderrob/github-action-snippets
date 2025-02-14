# GitHub Actions VS Code Snippets

This repository provides a collection of **Visual Studio Code snippets** for **GitHub Actions** and **GitHub Actions Workflows**. These snippets simplify the process of writing, editing, and managing **GitHub Actions YAML files**, ensuring correctness and completeness with predefined property selections.

## 🚀 Features

- **Predefined GitHub Action Templates** for Composite, Docker, and Node.js Actions.
- **Workflow Boilerplate** to quickly set up CI/CD pipelines.
- **Environment Variables** to insert commonly used GitHub Actions context values.
- **Comprehensive Properties** for branding, inputs, outputs, and steps.
- **Auto-completion and Selection Options** for colors, icons, and OS environments.
- **Error-Free YAML Formatting** for valid and structured configurations.

## 📌 Installation

1. Create a .vscode folder in your project root (if it doesn’t exist).
1. Inside .vscode, create or move your github-actions.code-snippets file.
1. Restart VS Code (Ctrl + Shift + P → Reload Window).
1. Open a .yml or .yaml file and type the snippet prefix (e.g., gha-workflow).
1. Manually invoke the snippet picker using:

   Windows/Linux: `Ctrl + Space`  
   Mac: `Cmd + Space`

   The snippets should now appear! 🎉

## 🔥 Available Snippets

### 1️. GitHub Actions - Branding

- **Prefix:** `gha-action-branding`
- **Description:** Inserts branding details for a custom GitHub Action.
- **Properties:** `color`, `icon` (predefined values for easy selection).

### 2️. GitHub Actions - Common Environment Variables

- **Prefix:** `gha-action-step-env`
- **Description:** Inserts commonly used GitHub Actions step environment variables.
- **Includes:** `GITHUB_ACTOR`, `GITHUB_REPOSITORY`, `GITHUB_REF`, `GITHUB_SHA`, `GITHUB_WORKSPACE`, `RUNNER_OS`, `RUNNER_ARCH`.

### 3️. GitHub Actions - Composite Action

- **Prefix:** `gha-composite-action`
- **Description:** Creates a Composite GitHub Action with configurable inputs, outputs, and steps.

### 4️. GitHub Actions - Composite Action 'run' Step

- **Prefix:** `gha-composite-action-step-run`
- **Description:** Inserts a 'run' step for Composite Actions with optional **`if`, `env`, `shell`, and `working-directory`** properties.

### 5️. GitHub Actions - Composite Action 'uses' Step

- **Prefix:** `gha-composite-action-step-uses`
- **Description:** Inserts a 'uses' step for referencing other actions.

### 6️. GitHub Actions - Docker Action

- **Prefix:** `gha-docker-action`
- **Description:** Provides a template for creating a **Docker-based GitHub Action**.

### 7️. GitHub Actions - Node.js Action

- **Prefix:** `gha-node-action`
- **Description:** Provides a template for creating a **Node.js 20.x GitHub Action**.

### 8️. GitHub Actions - Workflow Boilerplate

- **Prefix:** `gha-workflow`
- **Description:** Inserts a **GitHub Actions Workflow** template with `push` and `pull_request` triggers.
- **Includes:** `checkout`, `setup-node`, `install dependencies`, and `run tests` steps.

### 9️. GitHub Actions - Workflow Job

- **Prefix:** `gha-workflow-job`
- **Description:** Inserts a job structure with `runs-on` options and a **job status reference**.

### 10. GitHub Actions - Workflow Job 'run' Step

- **Prefix:** `gha-workflow-job-step-run`
- **Description:** Inserts a 'run' step for Composite Actions with optional **`if`, `env`, `shell`, and `working-directory`** properties.

### 11. GitHub Actions - Workflow Job 'uses' Step

- **Prefix:** `gha-workflow-job-step-uses`
- **Description:** Inserts a 'uses' step for referencing other actions.

## 🛠 How to Use

1. Open a `.yml` file inside the `.github/workflows/` directory.
2. Type the **prefix** (e.g., `gha-`) and select the snippet from the suggestions.
3. Use the placeholders and tab through the fields to customize.
4. Save the file and push it to GitHub to trigger the workflow.

## 📖 Example Usage

**Using the `gha-workflow` snippet:**

```yaml
name: GitHub Workflow

on:
  - push
  - pull_request

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        id: checkout-repository
        uses: actions/checkout@v4

      - name: Setup Node.js
        id: setup-node
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: Install Dependencies
        id: install-dependencies
        run: npm install

      - name: Run Tests
        id: run-tests
        run: npm test

```

## 🔍 Contributing

Feel free to contribute by submitting a **Pull Request (PR)** or opening an **Issue** to suggest improvements or report any bugs.

## 🎯 License

This project is licensed under the **Apache License V2.0 License**.

---

📢 **Follow GitHub Actions best practices to ensure optimal CI/CD performance!** 🚀
