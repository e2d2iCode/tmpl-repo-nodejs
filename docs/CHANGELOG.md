<!-- docs/CHANGELOG.md -->
<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD033 -->

# Changelog

All notable changes to this project will be documented in this file.

!!!Hint Conventions This document's format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and
[Semantic Versionning](https://semver.org/spec/v2.0.0.htmlspec/v2.0.0.html).

## [v1.0.2](https://github.com/e2d2iCode/tmpl-repo-nodejs/releases/tag/v1.0.1...v1.0.2) &nbsp;-&nbsp; 2025-06-08

### Changed

- The `docs/CHANGELOG.md` file to reflect the project's history
- The `CHANGELOG.md` file for its `Seed` section describe the current template

### Fixed

- The `docs/CHANGELOG.md` file doesn't reflect the project's history
- The `CHANGELOG.md` template not specifying the correct `Seed` contents

## [v1.0.1](https://github.com/e2d2iCode/tmpl-repo-nodejs/releases/tag/v1.0.0...v1.0.1) &nbsp;-&nbsp; 2025-06-07

### Added

- A documented `.config/` folder for hosting the config files that can be:
  - `.prettierrc`
  - `.eslintrc.json`
  - `jest.config.js`
  - `markdownlint.json`
  - `.commitlint.config.json`
- A `.config/_DEVDOC.md` file documenting all configs, regardless of location
- The `Markdown All In One` and `mardownlint` VSC exta in the recommendations

### Changed

- THE `CHANGELOG.md` TO AN OLD VERSION
- THE `docs/CHANGELOG.md` TO AN OLD VERSION
- The `README.md` file to match the changes
- The `markdownlint.json` file to ignore no rule
- The wrapper used to italic text in Markdown from `*` to `_`
- The `jest.config.js` file to explicitely specify the `rootDir` to be `..`
- The `.commitlint.config.json` file to ignore msg starting with 'Merge branch'
- The `test` script in `package.json` to add the `--passWithNoTests` flag to it
- The `.vscode/settings` file to specify the location of the configuration files
- The format (quoted globs) and contents (better categories) of
  `.github/labeler`
- The format of most `.md` and `.fs-info` files to make them Git hooks
  compatible

### Removed

- The following files were removed from the root level and moved to `.config/`:
  - `.prettierrc`
  - `.eslintrc.json`
  - `jest.config.js`
  - `markdownlint.json`
  - `.commitlint.config.json`

### Fixed

- The `pre-push` hook failing when there are no tests
- The `commit-msg` hook failing when commiting a merge
- The `pre-commit` hook failing due to badly formatted md files
- The`.github/labeler` causing a`pre-commit` error due to non-quoted globs

### Security

- ...

## [v1.0.0](https://github.com/e2d2iCode/tmpl-repo-nodejs/releases/tag/v0.0.1...v1.0.0) &nbsp;-&nbsp; 2025-06-07

### Added

- Testing framework: `Jest` with `jsdom`
- Code quality features: `EsLint` and `Prettier`
- A generic `package.json` file with placeholders and standard scripts
- Git Hooks using Husky:
  - [`pre-push`](.husky/pre-push): runs all tests before pushing to remote
  - [`commit-msg`](.husky/commit-msg): Uses `commitlint` to enforce commit
    message conventions: dependency +
    [commitlint.config.js](commitlint.config.js)
  - [`pre-commit`](.husky/pre-commit): formats and lints the code before
    committing
  - [`post-merge`](.husky/pre-push): syncs dependencies after a merge
  - [`post-checkout`](.husky/pre-push): syncs dependencies after a checkout
- Git hooks with `husky`:
  - `pre-push` runs all tests before pushing to remote
  - `post-merge` synchronizes dependencies after a merge
  - `pre-commit` formats and lints the code before committing
  - `commit-msg` uses `commitlint` to enforce conventional commits
  - `post-checkout` synchronizes dependencies after a branch checkout

### Changed

- Update [`README`](README.md) with NodeJs-Specific features
- Update [`.watchmanconfig`](.watchmanconfig) to ignore `node_modules/` folder

### Deprecated

- ...

### Removed

- ...

### Fixed

- Set placeholders to the `CHANGELOG` template (root-level)

### Security

- ...

---

## [Seed](https://github.com/e2d2iCode/tmpl-repo-nodejs/releases/tag/v0.0.1) &nbsp;-&nbsp; 2025-06-07

Seeded from [tmpl-repo-github](https://github.com/e2d2iCode/tmpl-repo-github),
which provides:

### Added

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
  [`/tests/`](tests/.fs-info), [`.github/`](.github/.fs-info)
- GitHub-specific features, including:
  - [Labeller](.github/labeler.yml) and [greetings](.github/greetings.yml)
    actions,
  - [Greetings](.github/greetings.yml) actions,
  - [Issue templates](.github/ISSUE_TEMPLATE/.fs-info),
  - [GitHub Workflows](.github/workflows/.fs-info),
  - [Greetings action](.github/gretteings.yml),
  - [Dependabot configuration](.github/dependabot.yml),
  - [Copilot instructions and prompts](.github/copilot/.fs-info)

<!-- markdownlint-disable -->
<!-- TENPLATES

___________________________________________________________________________

SECTIONS' TEMPLATES
´´´´´´´´´´´´´´´´´´´

## [Unreleased](https://github.com/e2d2iCode/tmpl-repo-nodejs/compare/...HEAD)

## [<vers>](https://github.com/e2d2iCode/tmpl-repo-nodejs/releases/tag/<the-tag>) &nbsp;-&nbsp; <yyy-mm-dd>

## [<vers>](https://github.com/e2d2iCode/tmpl-repo-nodejs/compare/<to-that>...<this>) &nbsp;-&nbsp; <yyy-mm-dd>

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

**[d<X.Y>-<label>-<Z>](https://github.com/e2d2iCode/tmpl-repo-nodejs/compare/d<X.Y>-<label>-<N>...<base-tag>**

___________________________________________________________________________

NEW VERSION CHECKLIST (!!! Release Branch !!!)
´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´

The first 3 steps below should be taken eright on the `develop` branch, right before the `telease` branch is created. If done on the `release` branch, then the changes should be merged back to the `develop` branch asap (before its changelog is updated with new entries, otherwise tconflicts will occur when the `release` branch is merged back to the `develop` branch).

    [   ]  REPLACE [Unreleased] by the last release's next version

    [   ]  ADD today's date in the format YYYY-MM-DD, 2025-12-31

    [   ]  REPLACE [Unreleased] by the last release's next version

The step below finalizes the release's changelog. It should be the last commit on the `release` branch before the final merge happens.

    [   ]  MODIFY the comparison settings from `...HEAD` to `<base_vers>...<this_vers>`

-->
