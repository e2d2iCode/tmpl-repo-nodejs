# Copilot Instructions - Markdown Filess

The following instructions are designed to ensure that Markdown files are formatted consistently and clearly, adhering to specific guidelines for readability and maintainability. These instructions apply to all Markdown files, including the `.fs-info` files used for directory metadata.

## Top Of The File

Always start the file with a comment indicating the relative path to the current file, formatted as `<!-- << path-to-current-file >> -->`. This comment is used to identify the file's location within the project structure and is not part of the Markdown content.

## Table of Contents and Linked Headings

Upon every change to the structure of the document, Copilot MUST perform a document-wide search for linked headings and update them accordingly, such that they are always correctly labelled and point to the correct section.

## General Markdown Formatting:

- Adhere to markdownlint rules unless explicitly instructed otherwise

- Ensure the document is well-structured with headings, subheadings, and lists where appropriate.

- Use proper indentation and spacing for readability.

- Stick to the markdownlint rules; if you cannot for whatever reason, wrap the concerned block into comment(s) pairs disabling and re-enabling the violated rule(s), repectively

- Make sure that a heading is never followed by another heading without some text in-between them. In particular, make sure to write a 2-3 lines paragraph after a heading and its first sub-heading.

- Do not use explicit `---` separators between sections

- Add a blank line before and after:
  - Each heading (except the first one in the document that should not have a blank line before it)
  - Each list (but not between list items, neither before sub-lists)
  - Each code block

- Avoid collisions in headings: each heading MUST be unique across the whole document.

## Formatting Of Specific Contents

- Format folder hierarchies as plaintext trees, e.g.,

```plaintext
src/
├── rxjs/                             # App-level  streams and utilities
│   ├── app-state/                      # Global state management
│   │   ├── app-state.observable.ts       # Observable for app state
│   │   ├── app-state.subject.ts          # Subject to manage app state
│   │   ├── app-state.types.ts            # Type definitions for app state
│   │   └── index.ts                      # Barrel file for app-state module
│   └── .../                            # Additional modules...
├── utils/                            # Utilities Folder
│   ├── rxjs/                           # RxJS-based Utilities
│   │   ├── create-rx-context/            # Utility for creating RxJS contexts
│   │   │   └── create-rx-context.tsx       # Implementation of the utility
│   │   ├── feat-x/                       # Feature-specific RxJS logic
│   │   │   ├── feat-x.observable.ts        # Observable for feat-x state
│   │   │   ├── feat-x.subject.ts           # Subject to manage feat-x state
│   │   │   ├── feat-x.types.ts             # Type definitions for feat-x
│   │   │   └── index.ts                    # Barrel file for feat-x module
│   │   └── .../                        # Additional modules...
└── ...                               # Same applies everywhere...
```

- Ensure subfolders are listed before files, and sort them by name length (shortest to longest).


## Clarity and Consistency

- Ensure the document is consistent and easy to read
- Avoid redundancies


## Chat Specific Instructions

The following rules apply only when Copilot is asked to provide the document's content in the chat, not when it is asked to edit the document:

### Output Format

- The document should start with ` ``` ` and end with ` ``` ` to indicate the full content is a code block.

### Inner Fenced Content

- Replace standard triple backticks (` ``` `) with `&&&` for all fenced code blocks inside the document.
- Example:
  Instead of:
  ```tsx
  const example = "code";
  ```
  Use:
  &&&tsx
  const example = "code";
  &&&
