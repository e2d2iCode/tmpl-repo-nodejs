# Copilot instructions - General Guidelines

## Placeholders and Special Symbols

The following are special symbols used to wrap placeholders and comments in Copilot instructions, code snippets, prompts, and templates. They MUST be used as specified below, and Copilot MUST interpret them accordingly.

- < ... > indicates something to be replaced with a specific value
- [ ... ] indicates that the content is optional and may be omitted
- ( ... ) contains a note or comment for Copilot (to be removed when used)
- <a> | <b> | <c> | ... indicates a list of items or options

When used in a context where a placeholder may conflict with other syntax or conventions, the wrapping symbols will be doubled, e.g. within a Markdown template or file, << ... >>, [[ ... ]], and (( ... )) will be used instead of < ... >, [ ... ], or ( ... ), respectively.

### Dedicated Placeholders
- `<< path-to-file >>` indicates the relative path to the current file from the project root, using forward slashes (`/`) as directory separators.
- `<< path-to-folder >>` indicates the relative path to the folder from the project root, using forward slashes (`/`) as directory separators.

## Custom Keywords and Commands

The following keywords have special meanings in the context of Copilot instructions. They MUST be used as specified below, and Copilot MUST interpret them accordingly.

### Actions

- **ADD**: Expects additional code or content to be added
- **UPDATE**: Indicates changes aiming to reflect the latest changes.
- **MODIFY**: Indicates changes that alter the existing code or functionalities.
- **EXPLAIN**: Expects an answer but no changes to the code to be made.

### Modal Operators

- **MAY**: Indicates an option that is permissible but not required.
- **MUST**: Indicates a requirement that is not negotiable and must be followed.
- **SHOULD**: Indicates a recommendation that should be followed unless there is a valid reason not to.

### Logical Operators

- **OR**: `a OR b` is true if at least one of `a` or `b` is true.
- **AND**: `a AND b` is true if and only if both `a` and `b` are true.
- **XOR**: `a XOR b` is true if and only if exactly one of `a` or `b` is true.
- **NOT**: `NOT a` is true if and only if `a` is false.
- **NAND**, **NOR**: shorts for "`NOT AND`" and "`NOT OR`", respectively.
- **IF-THEN**: `IF a THEN b` is true if and only if `a` is true and `b` is true.

### Store and Recover Information

The following are special instructions for Copilot to create a persistent state containing information that can be referenced in future interactions.

#### Store Information

The syntax for storing [whateve] information is as follows:

**LET** | **SAVE** | **VERSION** [<info>] as <label>

where:
- **LET** indicates that <label> MUST be an up-to-date reference to the value of `<whatever>`
- **SAVE** indicates that <label> MUST be a snapshot of the value of [<info>] at the time of the request
- **VERSION** indicates that <label> MUST be a versioned snapshot of the value of [<info>]; Copilot MUST automatically increment and append the version number to <label> as 2-digits integers, using `~` as a separator; it MUST confirm the versioned identifier in its answer, e.g. `SAVED [<info>] as <label>~01`, `SAVED [<info>] as <label>~02`, etc.

When clear from the context, [<info>] can be omitted, and the identifier can be used directly. As a general rule:
- When editing a file,  [<info>] is usually the file itself;
- When chatting, [<info>] is usually the last message I sent;

Copilot MUST ask for clarification if the context is not clear enough to determine what [<info>] refers to.

#### Recover Stored Information

The syntax for recovering information stored as <label> is as follows:

**GET** | **SHOW** | **USE** <label>

where:

- **GET** indicates that Copilot MUST retrieve the value of <label> and use it in its response

- **SHOW** indicates that Copilot MUST retrieve the value of <label> and display it in its response

- **USE** indicates that Copilot MUST retrieve the value of <label> and use it in its response, but NOT display it

## General Behavior

Unless explicitly requested to do otherwise, Copilot MUST follow the following general behavior guidelines:

- It MUST NOT rollback changes made by contributors

- It MUST NOT provide explanations about the code it generates

- It SHOULD provide code/scripts without comments

- It SHOULD end every code it generates with a newline character

- When asked for a list of things in the chat, it SHOULD be exhaustive and include all items that match the request. When not possible, it MUST specify that the list is partial, the reason why it was not exhaustive, and the selection criteria used.

- When providing different options in the chat, it SHOULD be very concise and provide only the necessary information to understand the options, unless otherwise specified. Its message MUST end with a compact table summarizing its 3 favorite options and the reasons for their ranking. No row SHOULD contain more than 2 lines of text.

- When editing files, it MUST keep track of its progress so that it can resume from where it left off in case of interruptions. It MUST NOT repeat the same changes multiple times, and it MUST NOT skip any changes that were already made.

## Filesystem's conventions

### Paths

A path starting with:

- `/` is relative to the filesystem's root;
- `./` is relative to the current file;
- `~/` is relative to the user's home directory;
- `../` is relative to the parent directory of the current file;
- All other paths are relative to the project root.

### Code Organization

#### Conceptual Directories

Conceptual directories are directories that group files and subdirectories based on their role or type of content, rather than their implementation details. They are used to organize the codebase in a way that reflects the project's architecture and design principles. E.g., `docs/`, `__tests__/`, `utils/`, `components/`, `models/`, etc.

The following conventions MUST be followed for conceptual directories:

- Conceptual directories MUST be named using a single word written in lowercase.

- Every conceptual directory SHOULD contain a `.fs-info` file at its root level, which MUST contain metadata about the directory's role and typical content. The description it contains SHOULD be agnostic to the project and applicable to any project using the same directory structure.

#### Module-like Directories

Module-like directories are directories that encapsulate a specific functionality or feature within the codebase. They typically contain all the necessary files, such as components, models, services, and tests, related to that functionality. E.g., `user/`, `product/`, `order/`, etc.

Module-like directories and the files they contain MUST be named using a case that reflects the nature of their content:

- Use PascalCase for directories and files exporting React components
- Use kebab-case for directories and files exporting RxJS-based functionalities
- Use snake_case for files exporting constant symbols (named in uppercase)
- Use camelCase for all other directories and files

Module-like directories must be organized according to the following conventions:

- The root level of a module-like directory MUST contain an `index.<ext>` file that exports all the public content of the directory.

- The root level of a module-like directory SHOULD contain a `README.md` file that documents the functionalities exported by the directory.

- The root level of a module-like directory MAY contain a `README.dev.md` file that provides technical details about the implementation of the directory's content.

- The root level of a module-like directory SHOULD NOT contain any other files or directories, except the ones mentioned above.

- The implementation of the functionalities exported by a module-like directory SHOULD be organized within conceptual directories, such as `components/`, `models/`, `services/`, `hooks/`, `utils/`, etc.

- Eventual tests MUST be placed in a `__tests__/` subfolder within the same folder as the code they test, and MUST follow the naming conventions specified above.

## Commit Message Guidelines

Copilot SHOULD handle the GIT workflow and suggest when to branch, commit, merge, and push changes based on the context of the changes being made. Commit messages MUST follow the conventional commit format, with the following additional requirements:

- Commit messages MUST be consistent throughout the project, following the same structure and style.
- Commit messages MUST be humans readable and understandable, avoiding technical jargon or abbreviations that may not be familiar to all contributors.
- Commit messages MUST be self-sufficient for generating changelogs, release notes, and documentation.
- Specifying a scope is mandatory. The scope SHOULD consist of a short, single, lowercase word; if more than one word is needed, kebab-case MUST be used. For changes affecting the entire project, the scope SHOULD be `global`.
- The message's subject MUST start with a gitmoji followed by a space
- The message's subject SHOULD not exceed 50 characters, including the gitmoji and spaces, where the gitmoji counts as 1 character.
- The body, if any, SHOULD be wrapped at 72 characters, including spaces.
- The body SHOULD provide a detailed description of the changes made, including the motivation behind them and any relevant context.tions.

## References

### The `prompts/` and `instructions/` folders

The `prompts/` and `instructions/` folders referenced in this project are located in `.github/copilot/` (use relative paths from the project root, **not** from the current file).

#### Specific instructions for Copilot

Instruction specific to given file types or contexts are stored in the `instructions/` folder. The provided files and the scope of their applicability are as follows:

##### Markdown Files

- `markdown.instructions.md`: instructions applying to all Markdown files, including `.md`, `.fs-info` files.

- `fs-info.instructions.md`: additional instructions applying to `.fs-info` files.

- `readme.instructions.md`: public, non-development `README.md` files documenting a tool, such as a project, module, component, utility, etc.

- `readme.dev.md`: development-specific `README.md` files documenting a tool, such as a project, module, component, utility, etc.
