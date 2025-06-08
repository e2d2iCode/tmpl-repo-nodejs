# DevDoc - Configuration Files

_This document provides a detailed overview of all configuration files used in
this project, both at the root level and within the `.configs/` folder. For each
file, you will find an explanation of the currently used parameters, possible
alternative values, and a link to the official documentation._

<!-- omit from toc -->

## Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Root-Level Config Files](#root-level-config-files)
  - [.editorconfig](#editorconfig)
  - [.watchmanconfig](#watchmanconfig)
  - [.prettierignore](#prettierignore)
- [Dedicated `.config/` Folder Contents](#dedicated-config-folder-contents)
  - [.eslintrc.json](#eslintrcjson)
  - [.markdownlint.json](#markdownlintjson)
  - [.prettierrc](#prettierrc)
  - [commitlint.config.js](#commitlintconfigjs)
  - [jest.config.js](#jestconfigjs)

## Root-Level Config Files

This section describes the main configuration files located at the root of the
project. These files define essential settings for code style, linting,
formatting, and development tooling, ensuring consistency and best practices
across the codebase.

### .editorconfig

The [`.editorconfig`](.editorconfig) file defines coding style and formatting
rules for supported editors and IDEs.

**Current parameters:**

- `root`: `true` Marks this file as the root `.editorconfig`.
- `end_of_line`: `lf` Other values: `cr`, `crlf`.
- `insert_final_newline`: `true` Other values: `false`.
- `charset`: `utf-8` Other values: `latin1`, `utf-16be`, `utf-16le`.
- `indent_style`: `space` Other value: `tab`.
- `indent_size`: `2` Number of spaces or tabs.
- `trim_trailing_whitespace`: `true` Other value: `false`.
- `[*.md] trim_trailing_whitespace`: `false` Disables trimming for Markdown
  files.

**Docs:** [EditorConfig Documentation](https://editorconfig.org/)

### .watchmanconfig

The [`.watchmanconfig`](.watchmanconfig) file configures Watchman for file
watching.

**Current parameters:**

- `ignore_dirs`: `[".git", "node_modules"]` Directories to ignore.

**Docs:** [Watchman Config](https://facebook.github.io/watchman/docs/config/)

### .prettierignore

The [`.prettierignore`](.prettierignore) file specifies files and directories to
ignore for Prettier formatting.

**Current patterns:**

- `node_modules/`, `dist/`, `build/`, `coverage/`, `.nyc_output/`, `.cache/`,
  `.next/`, `.tmp/`, `tmp/`, `.eslintcache`, `.vscode/`, `logs/`, `out/`,
  `.serverless/`

**Docs:** [Prettier Ignore Docs](https://prettier.io/docs/en/ignore.html)

## Dedicated `.config/` Folder Contents

This section outlines the configuration files found within the `.configs/`
directory, describing their purpose and key settings.

### .eslintrc.json

The [`.config/.eslintrc.json`](.config/.eslintrc.json) file configures ESLint
for code linting.

**Current parameters:**

- `root`: `true` Marks as root ESLint config.
- `env`:
  - `node`: `true` (Node.js global variables)
  - `es2021`: `true` (ES2021 globals)
  - `jest`: `true` (Jest testing globals)
- `extends`: `["eslint:recommended"]` Base rules. Other options: `"airbnb"`,
  `"plugin:react/recommended"`, etc.
- `plugins`: `["markdown"]` Enables linting in Markdown code blocks.
- `overrides`:
  - For `*.md` and `*.fs-info` files, uses the `markdown/markdown` processor.
- `rules`:
  - `"no-unused-vars": "warn"` Warns on unused variables. Other values: `"off"`,
    `"error"`.
  - `"no-console": "warn"` Warns on `console` usage. Other values: `"off"`,
    `"error"`.

**Docs:** [ESLint Configuration](https://eslint.org/docs/latest/use/configure/)

### .markdownlint.json

The [`.config/.markdownlint.json`](.config/.markdownlint.json) file configures
markdownlint for Markdown style and formatting.

**Current parameters:**

- `MD013`: `false` Disables line length rule. Other values: `true` (enable),
  `{ "line_length": 80 }` (custom length).

**Docs:**
[markdownlint Rules](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md)

### .prettierrc

The [`.config/.prettierrc`](.config/.prettierrc) file configures Prettier for
code formatting.

**Current parameters:**

- `semi`: `true` Use semicolons. Other value: `false`.
- `singleQuote`: `true` Use single quotes. Other value: `false`.
- `tabWidth`: `2` Number of spaces per tab.
- `trailingComma`: `es5` Trailing commas where valid in ES5. Other values:
  `none`, `all`.
- `printWidth`: `80` Line length.
- `proseWrap`: `always` Wrap markdown text. Other values: `never`, `preserve`.

**Docs:** [Prettier Options](https://prettier.io/docs/en/options.html)

### commitlint.config.js

The [`.config/commitlint.config.js`](.config/commitlint.config.js) file
configures commitlint for commit message linting.

**Current parameters:**

- `extends`: `['@commitlint/config-conventional']` Uses conventional commit
  rules.
- `ignores`: Ignores merge commits starting with `Merge branch`.

**Docs:** [commitlint Docs](https://commitlint.js.org/#/)

### jest.config.js

The [`.config/jest.config.js`](.config/jest.config.js) file configures Jest for
testing.

**Current parameters:**

- `rootDir`: `'..'` Sets Jest root directory to the project root.
- `testEnvironment`: `'node'` Test environment. Other value: `'jsdom'`.
- `roots`: `['<rootDir>/src', '<rootDir>/__tests__']` Test roots.
- `testMatch`:
  - `'**/__tests__/**/*.js?(x)'`
  - `'**/?(*.)+(spec|test).js?(x)'`
- `collectCoverage`: `true` Collects coverage.
- `coverageDirectory`: `'coverage'` Output directory for coverage.

**Docs:** [Jest Configuration](https://jestjs.io/docs/configuration)
