<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD033 -->
# Changelog

All notable changes to this project will be documented in this file.

!!!Hint Conventions
    This document's format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
    and [Semantic Versionning](https://semver.org/spec/v2.0.0.htmlspec/v2.0.0.html).

<!--
--------------------------------------------------------------------------------
___  TEMPLATE     ______________________________________________________________
--------------------------------------------------------------------------------

SECTIONS
´´´´´´´´´´
## [Unreleased](https://github.com/<user>/<repo>/compare/...HEAD)
## [<vers>](https://github.com/<user>/<repo>/releases/tag/<the-tag>) &nbsp;-&nbsp; <yyy-mm-dd>
## [<vers>](https://github.com/<user>/<repo>/compare/<to-that>...<this>) &nbsp;-&nbsp; <yyy-mm-dd>

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

-----------------------------------------------------------------------------

MILESTONES
´´´´´´´´´

**[d<X.Y>-<label>-<Z>](https://github.com/<user>/<repo>/compare/d<X.Y>-<label>-<N>...<base-tag>**

-->
<!--
--------------------------------------------------------------------------------
___ CHANGELOG   ________________________________________________________________
--------------------------------------------------------------------------------

NEW  VERSION  CHECKLIST  (!!! Release Branch !!!)
´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´
The first 3 steps below should be taken eright on the `develop` branch, right before  the `telease` branch is created. If done on the `release` branch, then the changes should be merged back to the `develop` branch asap (before  its changelog is updated with new entries, otherwise tconflicts will occur when the `release` branch is merged back to the `develop` branch).

    [   ]  REPLACE [Unreleased] by the last release's next version

    [   ]  ADD today's date in the format YYYY-MM-DD

    [   ]  REPLACE [Unreleased] by the last release's next version

The step below finalizes the release's changelog. It should be the last commit on the `release` branch before the final merge happens.

    [   ]  MODIFY the comparison settings from `...HEAD` to `<to-that>...<this>`
-->

## [Unreleased](https://github.com/<user>/<repo>/compare/...HEAD)

### Added

- ...

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

## [Seed](https://github.com/<user>/<repo>/releases/tag/v0.0.1) &nbsp;-&nbsp; <yyyy-mm-dd>

Seeded from [tmpl-repo-github](https://github.com/e2d2iCode/tmpl-repo-github), which provides:

### Added

- Standard Seeding Files:
  - [`README](readme.md) was updated to reflect the added material.
  - [`LICENSE](LICENSE.md) was added placeholders for date and name.
  - [`.gitignore`](.gitignore) was updated to reflect the added material.
- Folder hierarchy's documentation: `.fs-info` files
- Changelog tracking: [`/CHANGELOG.md`](CHANGELOG.md)
- Editor's configuration': [`.vscode/`](.vscode/.fs-info)
- Watchman configuration: [`.watchmanconfig`](.watchmanconfig)
- Git configuration: [`/.gitattributes`](.gitattributes), [`/.gitconfig`](.gitconfig)
- Template for local environment variables: [`/.env`](.env) - should not be committed.
- Template for required environment variables: [`/.env.required`](.env.required) - should be committed
- Policies: [`/CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md), [`/CONTRIBUTING.md`](CONTRIBUTING.md), [`/SECURITY.md`](SECURITY.md)
- Folder structure: [`/assets/`](assets/.fs-info), [`/docs/`](docs/.fs-info), [`/scripts/`](scripts/.fs-info), [`/src/`](src/.fs-info), [`/tests/`](tests/.fs-info), [`.github/`](.github/.fs-info)
- GitHub-specific features, including:
  - [Labeller](.github/labeler.yml) and [greetings](.github/greetings.yml) actions,
  - [Greetings](.github/greetings.yml) actions,
  - [Issue templates](.github/ISSUE_TEMPLATE/.fs-info),
  - [GitHub Workflows](.github/workflows/.fs-info),
  - [Greetings action](.github/gretteings.yml),
  - [Dependabot configuration](.github/dependabot.yml),
  - [Copilot instructions and prompts](.github/copilot/.fs-info)
