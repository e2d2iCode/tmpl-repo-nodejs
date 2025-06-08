<!-- README.md -->

# README - GitHub Template for NodeJS Projects

## Table of Contents

- [Overview](#overview)
  - [Key goals](#key-goals)
  - [Target audience](#target-audience)
- [Installation](#installation)
  - [1. On GitHub](#1-on-github)
  - [2. Clone your new repository](#2-clone-your-new-repository)
  - [3. Configure/Customize The Template](#3-configurecustomize-the-template)
  - [4. Install Dependencies & Prepare](#4-install-dependencies--prepare)
- [Features](#features)
  - [NodeJS-Specifc Features](#nodejs-specifc-features)
    - [Pre-configured `package.json`](#pre-configured-packagejson)
    - [NodeJS-friendly `.gitignore`](#nodejs-friendly-gitignore)
    - [ESLint Support](#eslint-support)
    - [Prettier Support](#prettier-support)
    - [Jest Support](#jest-support)
    - [Git Hooks Support](#git-hooks-support)
      - [The `pre-push` Hook](#the-pre-push-hook)
      - [The `commit-msg`](#the-commit-msg)
      - [The `pre-commit`](#the-pre-commit)
      - [The `post-merge`](#the-post-merge)
      - [The `post-checkout`](#the-post-checkout)
  - [Folder Metadata with `.fs-info` Files](#folder-metadata-with-fs-info-files)
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
        - [`.github/ISSUE_TEMPLATE/`](#githubissue_template)
        - [`.github/copilot/`](#githubcopilot)
- [Contributing](#contributing)
- [License](#license)
- [Roadmap](#roadmap)

## Overview

This template provides a generic GitHub repository ready to hold a wide variety
of projects, regardless of language or platform. It offers a standardized
structure, essential configuration files, and best-practices documentation to
help you start new projects quickly and maintain them efficiently. The template
is designed to be flexible, supporting applications, libraries, tools, and more,
while promoting code reuse and maintainability across different environments.

### Key goals

This template is designed to help you quickly launch NodeJS projects with a
focus on

- Providing a standardized, NodeJS-centric project structure that is easy to
  understand and extend.
- Accelerating NodeJS project setup by including essential configuration,
  documentation, and best-practices files out of the box.
- Supporting modern NodeJS development with minimal friction.
- Promoting code reuse, maintainability, and clarity across different NodeJS
  environments and teams.
- Reducing onboarding time for new contributors by documenting folder purposes
  and workflows.
- Enabling rapid prototyping, validation, and deployment for a wide range of
  NodeJS project types.

### Target audience

This template is intended for:

- Developers and teams starting new projects who want a standardized,
  best-practices repository structure.
- Open source maintainers seeking to provide clear onboarding and contribution
  guidelines.
- Organizations aiming to unify project scaffolding across multiple languages
  and platforms.
- Contributors looking for well-documented, easy-to-navigate repositories.

## Installation

To create a new project using this template, follow the step-by-step procedure
below.

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

**Note.** Your development environment must have [npm](https://www.npmjs.com/)
and/or [yarn](https://yarnpkg.com/), and [NodeJS](https://nodejs.org/)

### 3. Configure/Customize The Template

The exact procedure to configure/customize the template depends on the project's
specifics. The following modifications, however, are required regardless of the
project:

- Replace the root-level [README](README.md) file by one describing your
  project.

- Update/Chage the [LICENSE](LICENSE.md): by default, this template provides a
  copy of the _MIT_, which requires the `<<year>>` and `<<name>>` placeholders
  to be replaced by the copyright's year and name, respectively. For a different
  Open Source License or more information on the _MIT_, visit the
  [OpenSource.org's website](https://opensource.org/).

- Replace the `<<user>>` and `<<repo>>` placeholders by your GitHub's _username_
  and the the name of _repository_ hosting it. The files this replacement should
  affect are:

  - The [SECURITY](SECURITY.md) policy at the project's root
  - The [CHANGELOG](CHANGELOG.md) template at the project's root

- In the [CHANGELOG](CHANGELOG.md) template at the project's root, further
  replace the `<<yyyy-mm-dd>>` placeholder to be found at the end of the
  `## [Seed] ...` headings by the current date in the specified format. Note
  that instructions on how to update that file are embedded in the file itself.

- In [package.json](package.json), replace the `e2__project-<key>__e2`
  placeholders by values matching your project's information; there are 3 of
  them:
  - `e2__project-name__2e` should be your project's name;
  - `e2__project-descr__2e` should be a description of your project;
  - `e2__project-author__2e` should be the name(s) of the project's author(s);
  - `e2__project-license__2e` should be 'MIT' or the name the license you chose;
  - `e2__project-keywords__2e` should be a list of keywords referencinge your
    project;

### 4. Install Dependencies & Prepare

Install the required dependencies using your preferred package manager:

**Using `npm`**

```sh
npm install
```

**Using `yarn`**

```sh
yarn install
```

## Features

This template comes packed with essential features to streamline development and
accelerate your workflow.

- Unified codebase for multi-platform projects
- Scalable, language-agnostic project structure
- Easy-to-extend and customize
- Pre-configured repository files for best practices

In addition to the above, this template provides a set of pre-configured
repository files and folder metadata to help you maintain best practices and
ensure clarity throughout your project structure. Details about these are
provided in the subsections below.

### NodeJS-Specifc Features

This template is tailored for NodeJS development and includes several
NodeJS-specific enhancements. The next sections describe these enhancements in
detail, outlining how they support efficient and modern NodeJS project
workflows.

#### Pre-configured `package.json`

The [``package.json`](package.json) comes with sensible defaults for scripts,
dependencies, and metadata fields. Placeholders are provided for project name,
description, author, license, and keywords, making it easy to customize for your
project.

It also provides the following scripts, which can be easily extended or
customized

- **`start`**: Runs the main application in production mode.
- **`dev`**: Starts the application in development mode with hot-reloading (if
  configured).
- **`test`**: Executes the project's test suite.
- **`lint`**: Checks the code for linting errors using ESLint.
- **`format`**: Formats the codebase using Prettier or the configured formatter.
- **`prepare`**: Runs tasks needed before publishing or installing dependencies
  (e.g., Husky hooks setup). That command is run automatically after
  `npm install` or `yarn install` is invoked.

#### NodeJS-friendly `.gitignore`\*\*

Pre-configured to ignore `node_modules`, log files, build outputs, and
environment files, reducing accidental commits of unwanted files.

#### ESLint Support

The template includes a pre-configured ESLint setup for consistent code quality
and style enforcement. It comes with recommended rules for NodeJS, including
support for modern JavaScript features and best practices. The configuration is
located in `.eslintrc` or `.eslintrc.json` and can be extended to include
plugins (such as `eslint-plugin-node`, `eslint-plugin-import`,
`eslint-config-prettier`, etc.) or custom rules as needed. ESLint is integrated
with most editors for real-time feedback and can be run manually via
`npm run lint` or automatically as a pre-commit hook (via Husky). The setup
supports linting for both JavaScript and TypeScript if needed, and can be
further customized for your project's coding standards.

#### Prettier Support

Prettier is integrated for automatic code formatting, ensuring a consistent code
style across the project. The configuration is provided in `.prettierrc`,
`.prettierrc.json`, or within `package.json` under the `prettier` key, and can
be customized to match your team's preferences (e.g., tab width, semicolons,
single/double quotes, trailing commas). Prettier works alongside ESLint (with
`eslint-config-prettier` to avoid conflicts) and can be run via `npm run format`
or as part of the pre-commit workflow to enforce formatting before code is
committed. Editor plugins are available for on-save formatting, and Prettier can
be extended with ignore files (`.prettierignore`) to exclude files or folders
from formatting.

#### Jest Support

Jest is set up as the default testing framework, providing a robust environment
for writing and running unit and integration tests. Example configuration and
scripts are included.

The `__tests__/` folder is dedicated to end-to-end (E2E) tests. All E2E test
suites, utilities, and configuration files should be placed here. Unit tests
should be located alongside the code they test within the `/src` directory. This
separation helps maintain clarity between unit and E2E testing, making it easier
to organize and maintain your test code.

#### Git Hooks Support

Git hooks are managed via Husky, enabling automated checks (such as linting and
testing) before commits and pushes. This helps maintain code quality and prevent
errors from reaching the remote repository.

Each hook is configured in the `.husky/` directory and can be customized to fit
your project's workflow.

##### The `pre-push` Hook

The [`pre-push`](.husky/pre-push) hook runs the project's entire test suite
before allowing a push to a remote repository. This ensures that only code
passing all tests can be pushed, helping prevent broken or failing code from
reaching shared branches.

##### The `commit-msg`

The [`commit-msg`](.husky/commit-msg) hook uses
[commitlint](https://commitlint.js.org/) to enforce commit message conventions.
If a commit message does not follow the required format (as configured in
[`commitlint.config.js`](commitlint.config.js)), the commit will be rejected.
This helps maintain a consistent and meaningful commit history.

##### The `pre-commit`

The [`pre-commit`](.husky/pre-commit) hook runs code formatting (e.g., Prettier)
and linting (e.g., ESLint) on staged files before a commit is finalized. If any
formatting or linting errors are found, the commit is aborted. This ensures that
only well-formatted and lint-free code is committed to the repository.

##### The `post-merge`

The [`post-merge`](.husky/post-merge) hook automatically runs dependency
installation (e.g., `npm install` or `yarn install`) after a successful merge.
This ensures that your local dependencies are always up to date with the latest
changes from merged branches, reducing the risk of missing or outdated packages.

##### The `post-checkout`

The [`post-checkout`](.husky/post-checkout) hook automatically runs dependency
installation after switching branches or checking out a commit. This keeps your
working directory's dependencies in sync with the checked-out code, preventing
runtime errors due to missing or mismatched packages.

### Folder Metadata with `.fs-info` Files

Every conceptual folder in the template contains a `.fs-info` file at its root.
These files describe the typical role and content of the folder, providing:

- An overview of the folder's purpose (agnostic to any specific project or
  language)
- A summary of typical files and subfolders
- Guidance for maintainers and contributors on how to use or extend the folder

This approach ensures clarity, consistency, and easier onboarding for new
contributors.

### Pre-configured Standard Repository Files

This template includes a set of standard repository files to help you maintain
best practices and project hygiene from the start.

**You should review and update the following files to match your specific
project:**

#### Root Level Files

- [**`README.md`**](README.md): Project overview, installation, usage, and
  contribution guidelines.
- [**`LICENSE.md`**](LICENSE): Default is MIT.
- [**`CODE_OF_CONDUCT.md`**](CODE_OF_CONDUCT.md): Community standards and
  expected behavior.
- [**`CONTRIBUTING.md`**](CONTRIBUTING.md): Guidelines for contributing to the
  project.
- [**`SECURITY.md`**](SECURITY.md): Security policy and vulnerability reporting
  process.
- [**`CHANGELOG.md`**](CHANGELOG.md): Track changes, releases, and updates.
- [**`.env.required`**](.env.required): Template for required environment
  variables.
- [**`.env`**](.env): Actual environment variable values for local development.
- [**`.env.example`**](.env.example): A template for required environment
  variables.
- [**`.gitattributes`**](.gitattributes): Defines file handling attributes for
  Git, such as line endings normalization, diff settings, and linguist
  overrides. Helps maintain cross-platform consistency and proper file treatment
  in the repository.
- [**`.gitconfig`**](.gitconfig): Repository-specific Git configuration, such as
  preferred merge/diff tools and commit templates. Allows customizing Git
  behavior for this project.
- [**`.gitignore`**](.gitignore): Specifies intentionally untracked files to
  ignore, such as dependencies, build outputs, environment files, and OS/IDE
  artifacts. Keeps the repository clean and focused on source files.
- [**`.fs-info`**](.fs-info): Describes the purpose and typical contents of the
  project root folder. Each major folder in the template includes a `.fs-info`
  file to document its intended role and usage.

#### Standard Repository Folders

The template includes a set of standard top-level folders, each serving a
specific purpose in the project structure:

- **`/src`** Contains all source code for your application, library, or tool,
  including shared logic, components, platform-specific entry points, and
  utilities.

- **`/docs`** Documentation for the project, such as setup guides, architecture
  decisions, and platform-specific instructions.

- **`/assets`** Static assets like images, fonts, icons, and other resources
  used by the project.

- **`/scripts`** Utility scripts for development, build, or deployment
  automation.

- **`/__tests__`** Test suites and related configuration for unit, integration,
  or end-to-end testing.

- **`.github/`** GitHub-specific files, including workflows, issue templates,
  and pull request templates.

Each folder contains a `.fs-info` file that describes its intended role and
typical contents. Detailed information about each folder is provided in the next
subsections.

##### The `/src` Folder

The `/src` folder contains all source code for your project. This includes:

- Shared logic and business rules
- Components or modules (cross-platform and platform-specific)
- Platform entry points (e.g., `main.py`, `index.js`, `main.rs`, etc.)
- Utilities, helpers, and context providers
- Any subfolders for feature modules or domains

Maintain a clear structure within `/src` to separate concerns and maximize code
reuse.

##### The `/docs`

The `/docs` folder holds documentation relevant to the project, such as:

- Setup and installation guides
- Architecture decision records (ADRs)
- Platform-specific instructions
- Contribution and onboarding guides
- API documentation

Keep documentation up to date to help contributors and users understand and use
the project effectively.

##### The `/assets`

The `/assets` folder is for static resources, including:

- Images, icons, and logos
- Fonts and media files
- Any other static files required by the project

Organize assets by type or feature as needed for clarity.

##### The `/scripts`

The `/scripts` folder contains utility scripts for development, build, or
deployment automation, such as:

- Build and packaging scripts
- Linting, formatting, or code generation tools
- Deployment and CI/CD helpers

Scripts should be well-documented and cross-platform where possible.

##### The `/__tests__`

This folder contains only end-to-end tests. Unit tests should be stored near the
code they test.

The `/__tests__/` folder is for all end-to-end test-related code and
configuration, including:

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

Contains GitHub Actions workflow YAML files that automate CI/CD tasks such as
testing, building, and deploying the project. The template includes the
following workflows:

- **[greetings.yml](.github/workflows/greetings.yml)** Welcomes users when they
  open their first issue or pull request. This workflow uses the
  `actions/first-interaction` action to automatically post a friendly greeting
  message, helping new contributors feel welcome.

- **[label.yml](.github/workflows/label.yml)** Automatically applies labels to
  pull requests based on repository configuration. This workflow uses the
  `actions/labeler` action to triage and organize pull requests, making it
  easier to manage contributions.

###### `.github/ISSUE_TEMPLATE/`

Holds Markdown templates for different types of GitHub issues (e.g., bug
reports, feature requests) to standardize and streamline issue submissions. The
template includes the following files:

- [**`bug_report.md`**](.github/ISSUE_TEMPLATE/bug_report.md): For reporting
  bugs and unexpected behavior.
- [**`feature_request.md`**](.github/ISSUE_TEMPLATE/feature_request.md): For
  suggesting new features or enhancements.
- [**`general_comment.md`**](.github/ISSUE_TEMPLATE/general_comment.md): For
  general feedback, questions, or comments.
- [**`misconduct_report.md`**](.github/ISSUE_TEMPLATE/misconduct_report.md): For
  reporting code of conduct violations or inappropriate behavior.
- [**`vulnerability_reportd.md`**](.github/ISSUE_TEMPLATE/vulnerability_reportd.md):
  For confidentially reporting security vulnerabilities.

###### `.github/copilot/`

Includes configuration and instruction files for GitHub Copilot, such as custom
Copilot instructions to guide AI code suggestions. These files help ensure that
Copilot-generated code aligns with your project's conventions and requirements.

## Contributing

Contributions are welcome! Please open issues or submit pull requests to help
improve this template. More information is available at
[`CONTRIBUTING](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](./LICENSE).

## Roadmap

- Add support for Jekyll documentation.
- Improve the template's documentation, including the present `README` file.
