<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD033 -->

# Changelog

All notable changes to this project will be documented in this file.

!!!Hint Conventions This document's format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and
[Semantic Versionning](https://semver.org/spec/v2.0.0.htmlspec/v2.0.0.html).

<!-- SECTIONS' TEMPLATES ---

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

-->
<!-- MILESTONES' TEMPLATES ---

**[d<X.Y>-<label>-<Z>](<https://github.com/><<user>>/<<repo>>/compare/d<X.Y>-<label>-<N>...<base-tag>**

-->
<!-- NEW VERSION CHECKLIST (!!! Release Branch !!!) ---

The first 3 steps below should be taken eright on the `develop` branch, right before the `telease` branch is created. If done on the `release` branch, then the changes should be merged back to the `develop` branch asap (before its changelog is updated with new entries, otherwise tconflicts will occur when the `release` branch is merged back to the `develop` branch).

    [   ]  REPLACE [Unreleased] by the last release's next version

    [   ]  ADD today's date in the format YYYY-MM-DD, 2025-12-31

    [   ]  REPLACE [Unreleased] by the last release's next version

The step below finalizes the release's changelog. It should be the last commit on the `release` branch before the final merge happens.

    [   ]  MODIFY the comparison settings from `...HEAD` to `<base_vers>...<this_vers>`

-->

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

---

## [Seed](https://github.com/<<user>>/<<repo>>/releases/tag/v0.0.1) &nbsp;-&nbsp; <<yyyy-mm-dd>>

Seeded from [tmpl-repo-nodejs](https://github.com/e2d2iCode/tmpl-repo-nodejs),
which provides:

### Added

- NodeJS specific features:
  - A generic [`package.json`](package.json) file with e2**placeholders**2e
  - EsLint: dependency + [`.eslintrc.json`](.eslintrc.json) + VSC's ESLint
    Extension
  - Prettier: dependency + [`.prettierrc`](.prettierrc) +
    [`.prettierignorec`](.prettierignorec) + VSC's Prettier Extension
  - Postcss dependency for transforming CSS with JavaScript plugins
  - Jest framework for testing: dependency + [`jest.config.js](jest.config.js) +
    jest-environment-jsdom dependency
  - Husky support: dependency + [.husky/](.husky/.fs-info) folder
  - Git Hooks using Husky:
    - [`pre-push`](.husky/pre-push): runs all tests before pushing to remote
    - [`commit-msg`](.husky/commit-msg): Uses `commitlint` to enforce commit
      message conventions: dependency +
      [commitlint.config.js](commitlint.config.js)
    - [`pre-commit`](.husky/pre-commit): formats and lints the code before
      committing
    - [`post-merge`](.husky/pre-push): syncs dependencies after a merge
    - [`post-checkout`](.husky/pre-push): syncs dependencies after a checkout
- Standard Seeding Files:
  - [`README](readme.md) was updated to reflect the added material.
  - [`LICENSE](LICENSE.md) was added placeholders for date and name.
  - [`.gitignore`](.gitignore) was updated to reflect the added material.
- Folder hierarchy's documentation: `.fs-info` files
- Changelog tracking: [`/CHANGELOG.md`](CHANGELOG.md)
- Editor's configuration': [`.vscode/`](.vscode/.fs-info)
- Watchman configuration: [`.watchmanconfig`](.watchmanconfig)
- Git configuration: [`/.gitattributes`](.gitattributes),
  [`/.gitconfig`](.gitconfig)
- Template for local environment variables: [`/.env`](.env) - should not be
  committed.
- Template for required environment variables:
  [`/.env.required`](.env.required) - should be committed
- Policies: [`/CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md),
  [`/CONTRIBUTING.md`](CONTRIBUTING.md), [`/SECURITY.md`](SECURITY.md)
- Folder structure: [`/assets/`](assets/.fs-info), [`/docs/`](docs/.fs-info),
  [`/scripts/`](scripts/.fs-info), [`/src/`](src/.fs-info),
  [`/tests/`](tests/.fs-info), [`.github/`](.github/.fs-info) (docs/.fs-info),
  [`/scripts/`](scripts/.fs-info), [`/src/`](src/.fs-info),
  [`/tests/`](tests/.fs-info), [`.github/`](.github/.fs-info)
- GitHub-specific features, including:
  - [Greetings](.github/greetings.yml) actions,
  - [Issue templates](.github/ISSUE_TEMPLATE/.fs-info),
  - [GitHub Workflows](.github/workflows/.fs-info),
  - [Greetings action](.github/gretteings.yml),
  - [Dependabot configuration](.github/dependabot.yml),
  - [Copilot instructions and prompts](.github/copilot/.fs-info)
  - [Labeller](.github/labeler.yml) and [greetings](.github/greetings.yml)
    actions,
