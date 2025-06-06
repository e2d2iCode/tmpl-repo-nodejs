# Copilot Instructions - `README.md` Files

The following instructions are designed to ensure that `README.md` files are created and formatted consistently, providing a clear overview of the "tool" at hand, whether a full project, a module, a component, a utility, or any other implementation.

These instructions apply in addition to the general markdown formatting rules specified in `.github/copilot/instructions/markdown.instructions.md`.


## General Instructions

In the next section below is the template to follow for `README.md` files. It provides a structured format that MUST be adhered to when creating these files.

- Copilot MUST start by determining the name and type of the tool at hand such that it can refer to the "tool at hand" adequately throughout the document. IF it is not able to do it based on the context, Copilot MUST put the file's editing in standby, ask the user for clarification and resume the editing automatically once the user has provided the necessary information.

- The template's structure, style and sectionning MUST be strictly followed to ensure consistency across the project.

## The `README.md` File Template

<!-- << path-to-file >> -->
# README - << Name of the tool at hand >>

(( Here, INSERT A concis description of the tool at hand, its purpose, and key features. ))

## Table of Contents

(( Here, INSERT a table of contents (toc) as a 3-levels lists, with the first level being the main sections, the second level being subsections, and the third level being subsubsections, if any. Each item in the table of contents MUST be a link to the corresponding section in the document. Do NOT reference the `Table of Contents` section itself. The toc MUST be generated automatically by Copilot and updated whenever the structure of the document changes. ))

## Overview

(( Here, INSERT a 2-3 paragraphs overview of the tool at hand, including its goals, target audience, and key functionalities. ))

## Installation

(( Here, INSERT step-by-step instructions on how to install and set up the tool at hand locally. If the tool at hand is not an npm package, specify that it must be copied manually and provide instructions for doing so. ))

## Usage

(( Here, INSERT instructions on how to use the tool at hand. Explain how to import the provided features using the `import` statement and the `index.<ext>` file. If applicable, dedicate a subsection on the tool's configuration and illustrate it using examples and code snippets. If longer than a few lines, subdivide into subheadings, subsubheadings. Provide any additional details necessary for understanding how to use the tool at hand. ))

## Features

(( Here, INSERT a list the key features of the tool at hand with a concise description. Then, provide a detailed description of each features in its own subsection. Further subdivide each subsection into lower level subsections if necessary.  Illustrate each feature's usage with example(s) and code snippets. ))

## Contributing

(( Here, INSERT detailed guidelines for contributing to the development of the tool at hand, including forking, branching, committing, pushing, and submitting pull requests. If applicable, reference the `README.dev.md` file for development-specific instructions. ))

## License

(( Here, INSERT the type of license under which the tool at hand is distributed and provide a link to the `LICENSE.md` file to be found in the tool's root directory. ))

## References

((Here, INSERT a list of references to any external resources, documentation, or related projects that may be useful for understanding or using the tool at hand, if any. If there are no references, write: "No references available."))
