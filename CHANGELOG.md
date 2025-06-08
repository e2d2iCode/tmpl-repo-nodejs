<!-- CHANGELOG.md -->
<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD033 -->

# Changelog

All notable changes to this project will be documented in this file.

!!!Hint Conventions This document's format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and
[Semantic Versionning](https://semver.org/spec/v2.0.0.htmlspec/v2.0.0.html).

## [Unreleased](https://github.com/<<user>>/<<repo>>/compare/...HEAD)

### Added

- ...

### Changed

- ...

### Deprecated

- ...

### Removed

- ...

### Fixed

- ...

### Security

- ...

## [Seed](https://github.com/<<user>>/<<repo>>/releases/tag/v0.0.1) &nbsp;-&nbsp; <<yyyy-mm-dd>>

Seeded from [tmpl-repo-nodejs](https://github.com/e2d2iCode/tmpl-repo-nodejs),
which provides:

### Added

- Standard Repo Files:

  - Env: `.env`, `.env.required`
  - Meta: `.fs-info` to describe dirs' roles and typical content
  - Seed: `README.md`, `LICENSE.md`, `CHANGELOG.md`, `.gitignore`
  - Policy: `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`
  - Configs: `.watchmanconfig`, `.gitattributes`, `.gitconfig`, `.editorconfig`

- Standard Repo Folders:

  - Dot-folders: `.configs/`, `.github/`, `.vscode/`, `.husky`
  - Std-folders: `/assets/`, `/docs/`, `/scripts/`, `/src/`, `/__tests__/`

- Features and Utilities:
  - Git hooks with `husky`
  - Testing support with `Jest`
  - Code quality with `ESLint` and `Prettier`
  - Generic `package.json` file and standard scripts
  - GitHub Features: actions, templates, workflows, Copilot instructions

<!-- markdownlint-disable -->
<!-- TENPLATES

___________________________________________________________________________

SECTIONS' TEMPLATES
´´´´´´´´´´´´´´´´´´´

## [Unreleased](https://github.com/<<user>>/<<repo>>/compare/...HEAD)

## [<vers>](https://github.com/<<user>>/<<repo>>/releases/tag/<the-tag>) &nbsp;-&nbsp; <yyy-mm-dd>

## [<vers>](https://github.com/<<user>>/<<repo>>/compare/<to-that>...<this>) &nbsp;-&nbsp; <yyy-mm-dd>

### Added

- ...

### Changed

- ...

### Deprecated

- ...

### Removed

- ...

### Fixed

- ...

### Security

- ...

___________________________________________________________________________

MILESTONES' TEMPLLATE
´´´´´´´´´´´´´´´´´´´´´

**[d<X.Y>-<label>-<Z>](https://github.com/<<user>>/<<repo>>/compare/d<X.Y>-<label>-<N>...<base-tag>**

___________________________________________________________________________

NEW VERSION CHECKLIST (!!! Release Branch !!!)
´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´

The first 3 steps below should be taken when on the `develop` branch, right before the `release` branch is created. If done on the `release` branch, then the changes should be merged back to the `develop` branch asap (before its changelog is updated with new entries, otherwise conflicts will occur when the `release` branch is merged back to the `develop` branch).

    [   ]  REPLACE [Unreleased] by the last release's next version

    [   ]  ADD today's date in the format YYYY-MM-DD, 2025-12-31

    [   ]  REPLACE [Unreleased] by the last release's next version

The step below finalizes the release's changelog. It should be the last commit on the `release` branch before the final merge happens.

    [   ]  MODIFY the comparison settings from `...HEAD` to `<base_vers>...<this_vers>`

-->
