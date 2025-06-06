<!-- README.md -->
# README - Generic GitHub Template

## Table of Contents

- [Overview](#overview)
  - [Key goals](#key-goals)
  - [Target audience](#target-audience)
- [Installation](#installation)
  - [On GitHub](#on-github)
  - [Clone your new repository](#clone-your-new-repository)
  - [Update/Customize Files](#updatecustomize-files)
  - [Set up platform-specific requirements](#set-up-platform-specific-requirements)
- [Features](#features)
  - [Pre-configured Standard Repository Files](#pre-configured-standard-repository-files)
    - [Root Level Files](#root-level-files)
    - [Standard Repository Folders](#standard-repository-folders)
      - [The `/src` Folder](#the-src-folder)
      - [The `/docs`](#the-docs)
      - [The `/assets`](#the-assets)
      - [The `/scripts`](#the-scripts)
      - [The `/__tests__`](#the-__tests__)
      - [The `.github/`](#the-github)
        - [`.github/workflows/`](#githubworkflows)
        - [`.github/ISSUE_TEMPLATE/`](#githubissuetemplate)
        - [`.github/copilot/`](#githubcopilot)
  - [Folder Metadata with `.fs-info` Files](#folder-metadata-with-fs-info-files)
- [Contributing](#contributing)
- [License](#license)
- [Roadmap](#roadmap)

## Overview

This template provides a generic GitHub repository ready to hold a wide variety of projects, regardless of language or platform. It offers a standardized structure, essential configuration files, and best-practices documentation to help you start new projects quickly and maintain them efficiently. The template is designed to be flexible, supporting applications, libraries, tools, and more, while promoting code reuse and maintainability across different environments.

### Key goals

This template is designed to help you quickly launch projects with a focus on

- Providing a standardized, language-agnostic project structure that is easy to understand and extend.
- Accelerating project setup by including essential configuration, documentation, and best-practices files out of the box.
- Supporting multi-platform and multi-language development with minimal friction.
- Promoting code reuse, maintainability, and clarity across different environments and teams.
- Reducing onboarding time for new contributors by documenting folder purposes and workflows.
- Enabling rapid prototyping, validation, and deployment for a wide range of project types.

### Target audience

This template is intended for:

- Developers and teams starting new projects who want a standardized, best-practices repository structure.
- Open source maintainers seeking to provide clear onboarding and contribution guidelines.
- Organizations aiming to unify project scaffolding across multiple languages and platforms.
- Contributors looking for well-documented, easy-to-navigate repositories.

## Installation

To create a new project using this template, follow the step-by-step procedure below.

### 1. On GitHub

1. Click the **"Use this template"** button at the top of the repository page.
2. Choose **"Create a new repository"**.
3. Fill in your new repository details (name, description, visibility, etc.).
4. Click **"Create repository from template"**.

### 2. Clone your new repository

Clone your newly created repository to your local machine:

```sh
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Update/Customize Files

The following files REQUIRE modifications to reflect your project:

- [README](README.md): modify the current file's content to describe your own project.

- [LICENSE](LICENSE.md): by default, this template provides a copy of the [MIT License](https://opensource.org/licenses/MIT), which needs to be updated with the copyright's year and name. For a different Open Source License, refer to the [OpenSource.org's website](https://opensource.org/).

- [SECURITY](SECURITY.md): this file contains a link to your repository, which `<username>` and `<repository>` placeholders require to be replaced by your project's specific data.

- [CHANGELOG](CHANGELOG.md): this file contains a link to your repository, which `<username>` and `<repository>` placeholders require to be replaced by your project's specific data.



```sh
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```


### 4. Set up platform-specific requirements

- Create configuration files (e.g., `package.json`, `pyproject.toml`, etc.).
- Update `.env.required` and `.env` and fill in required environment variables.
- Follow any additional setup steps according to your project's type

## Features

This template comes packed with essential features to streamline development and accelerate your workflow.

- Unified codebase for multi-platform projects
- Scalable, language-agnostic project structure
- Easy-to-extend and customize
- Pre-configured repository files for best practices

In addition to the above, this template provides a set of pre-configured repository files and folder metadata to help you maintain best practices and ensure clarity throughout your project structure. Details about these are provided in the subsections below.

### Pre-configured Standard Repository Files

This template includes a set of standard repository files to help you maintain best practices and project hygiene from the start.

**You should review and update the following files to match your specific project:**

#### Root Level Files

- [**`README.md`**](README.md): Project overview, installation, usage, and contribution guidelines.
  _Update to reflect your project's purpose, setup, and usage instructions._
- [**`LICENSE.md`**](LICENSE): Default is MIT.
  _Replace or update if your project uses a different license._
- [**`CODE_OF_CONDUCT.md`**](CODE_OF_CONDUCT.md): Community standards and expected behavior.
  _Update contact information or enforcement details as needed._
- [**`CONTRIBUTING.md`**](CONTRIBUTING.md): Guidelines for contributing to the project.
  _Customize to match your workflow and requirements._
- [**`SECURITY.md`**](SECURITY.md): Security policy and vulnerability reporting process.
  _Update reporting instructions and supported versions._
- [**`CHANGELOG.md`**](CHANGELOG.md): Track changes, releases, and updates.
  _Continue to update as your project evolves._
- [**`.env.required`**](.env.required): Template for required environment variables.
  _Update to list all environment variables your project needs. THIS FILE GETS COMMITTED._
- [**`.env`**](.env): Actual environment variable values for local development.
  _Should not be committed to version control; add to `.gitignore`. THIS FILE IS EXCLUDED FROM BEING COMMITTED (see [`.gitignore`](.gitignore))_
- [**`.env.example`**](.env.example): A template for required environment variables.
  _Should not be committed to version control; add to `.gitignore`._

- [**`.gitattributes`**](.gitattributes): Defines file handling attributes for Git, such as line endings normalization, diff settings, and linguist overrides. Helps maintain cross-platform consistency and proper file treatment in the repository.
- [**`.gitconfig`**](.gitconfig): Repository-specific Git configuration, such as preferred merge/diff tools and commit templates. Allows customizing Git behavior for this project.
- [**`.gitignore`**](.gitignore): Specifies intentionally untracked files to ignore, such as dependencies, build outputs, environment files, and OS/IDE artifacts. Keeps the repository clean and focused on source files.
- [**`.fs-info`**](.fs-info): Describes the purpose and typical contents of the project root folder. Each major folder in the template includes a `.fs-info` file to document its intended role and usage.

  _Update checklist and sections as needed._

#### Standard Repository Folders

The template includes a set of standard top-level folders, each serving a specific purpose in the project structure:

- **`/src`**
  Contains all source code for your application, library, or tool, including shared logic, components, platform-specific entry points, and utilities.

- **`/docs`**
  Documentation for the project, such as setup guides, architecture decisions, and platform-specific instructions.

- **`/assets`**
  Static assets like images, fonts, icons, and other resources used by the project.

- **`/scripts`**
  Utility scripts for development, build, or deployment automation.

- **`/__tests__`**
  Test suites and related configuration for unit, integration, or end-to-end testing.

- **`.github/`**
  GitHub-specific files, including workflows, issue templates, and pull request templates.

Each folder contains a `.fs-info` file that describes its intended role and typical contents. Detailed information about each folder is provided in the next subsections.

##### The `/src` Folder

The `/src` folder contains all source code for your project. This includes:

- Shared logic and business rules
- Components or modules (cross-platform and platform-specific)
- Platform entry points (e.g., `main.py`, `index.js`, `main.rs`, etc.)
- Utilities, helpers, and context providers
- Any subfolders for feature modules or domains

Maintain a clear structure within `/src` to separate concerns and maximize code reuse.

##### The `/docs`

The `/docs` folder holds documentation relevant to the project, such as:

- Setup and installation guides
- Architecture decision records (ADRs)
- Platform-specific instructions
- Contribution and onboarding guides
- API documentation

Keep documentation up to date to help contributors and users understand and use the project effectively.

##### The `/assets`

The `/assets` folder is for static resources, including:

- Images, icons, and logos
- Fonts and media files
- Any other static files required by the project

Organize assets by type or feature as needed for clarity.

##### The `/scripts`

The `/scripts` folder contains utility scripts for development, build, or deployment automation, such as:

- Build and packaging scripts
- Linting, formatting, or code generation tools
- Deployment and CI/CD helpers

Scripts should be well-documented and cross-platform where possible.

##### The `/__tests__`

This folder contains only end-to-end tests.
Unit tests should be stored near the code they test.

The `/__tests__/` folder is for all end-to-end test-related code and configuration, including:

- End-to-end test suites
- Test utilities and mocks
- Test configuration files

Organize tests to mirror the structure of `/src` for easier navigation.

##### The `.github/`

The `.github/` folder contains GitHub-specific files, including:

- Workflow definitions (`workflows/`)
- Issue templates (`ISSUE_TEMPLATE/`)
- Pull request template (`pull_request_template.md`)
- Copilot configuration files (`copilot/`)
- Other configuration files as needed

###### `.github/workflows/`

Contains GitHub Actions workflow YAML files that automate CI/CD tasks such as testing, building, and deploying the project. The template includes the following workflows:

- **[greetings.yml](.github/workflows/greetings.yml)**
  Welcomes users when they open their first issue or pull request. This workflow uses the `actions/first-interaction` action to automatically post a friendly greeting message, helping new contributors feel welcome.

- **[label.yml](.github/workflows/label.yml)**
  Automatically applies labels to pull requests based on repository configuration. This workflow uses the `actions/labeler` action to triage and organize pull requests, making it easier to manage contributions.

###### `.github/ISSUE_TEMPLATE/`

Holds Markdown templates for different types of GitHub issues (e.g., bug reports, feature requests) to standardize and streamline issue submissions. The template includes the following files:

- [**`bug_report.md`**](.github/ISSUE_TEMPLATE/bug_report.md): For reporting bugs and unexpected behavior.
- [**`feature_request.md`**](.github/ISSUE_TEMPLATE/feature_request.md): For suggesting new features or enhancements.
- [**`general_comment.md`**](.github/ISSUE_TEMPLATE/general_comment.md): For general feedback, questions, or comments.
- [**`misconduct_report.md`**](.github/ISSUE_TEMPLATE/misconduct_report.md): For reporting code of conduct violations or inappropriate behavior.
- [**`vulnerability_reportd.md`**](.github/ISSUE_TEMPLATE/vulnerability_reportd.md): For confidentially reporting security vulnerabilities.

###### `.github/copilot/`

Includes configuration and instruction files for GitHub Copilot, such as custom Copilot instructions to guide AI code suggestions. These files help ensure that Copilot-generated code aligns with your project's conventions and requirements.

### Folder Metadata with `.fs-info` Files

Every conceptual folder in the template contains a `.fs-info` file at its root.
These files describe the typical role and content of the folder, providing:

- An overview of the folder's purpose (agnostic to any specific project or language)
- A summary of typical files and subfolders
- Guidance for maintainers and contributors on how to use or extend the folder

This approach ensures clarity, consistency, and easier onboarding for new contributors.

## Contributing

Contributions are welcome! Please open issues or submit pull requests to help improve this template. More information is available at [`CONTRIBUTING](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](./LICENSE).


## Roadmap

- Add support for Jekyll documentation.
- Improve the template's documentation, including the present `README` file.
