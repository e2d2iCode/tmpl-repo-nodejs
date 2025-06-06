# Copilot Instructions - `README.dev.md` Files

The following instructions are designed to ensure that `README.md` files are created and formatted consistently, providing a clear overview of the implementation of "tool" at hand, whether a full project, a module, a component, a utility, or any other implementation.

These instructions apply in addition to the general markdown formatting rules specified in `.github/copilot/instructions/markdown.instructions.md`.

## General Instructions

In the next Section below is the template to follow for `README.dev.md` files. It provides a structured format that MUST be adhered to when creating these files.

- Copilot MUST start by determining the name and type of the tool at hand such that it can refer to the "tool at hand" adequately throughout the document. IF it is not able to do it based on the context, Copilot MUST put the file's editing in standby, ask the user for clarification and resume the editing automatically once the user has provided the necessary information.

- The template's structure, style and sectionning MUST be strictly followed to ensure consistency across the project.

- Eventual `.fs-info` files MUST be ignored

- Useful information MAY be found in the `README.md` file, but the current description MUST be adapted to the development context, focusing on implementation details, development practices, and technical aspects relevant to developers.


### The `README.dev.md` File Template

<!-- << path-to-file >> -->
# README - << Name of the tool at hand >>

(( Here, INSERT A brief description of the tool at hand, its purpose, and key features. ))

## Table of Contents

(( Here, INSERT a table of contents (toc) as a 3-levels lists, with the first level being the main sections, the second level being subsections, and the third level being subsubsections, if any. Each item in the table of contents MUST be a link to the corresponding section in the document. Do NOT reference the `Table of Contents` section itself. The toc MUST be generated automatically by Copilot and updated whenever the structure of the document changes. ))

## Overview

(( Here, INSERT an overview of the technical implementation of the tool at hand, including its goals, key functionalities and technologies used. If applicable, illustrate the overview with diagrams. ))

### Exported features

(( Here, INSERT a list of the key features exported by the tool at hand with a concise description and the file(s) where they can be found. ))

## Code's Organization

The tree-structure of the codebase is as follows:

(( Here, INSERT the folder's full tree structure as a plaintext doc-block, with a concise comment describing each level and file of the tree. Follow the rules for ordering subfolders and files. Show every folder and file to the exception of `.fs-info` files. ))

### Dependecies and Interdependencies

(( Here, INSERT a description of the dependencies and interdependencies between the files and folders, explaining how they interact with each other. If applicable, illustrate the interdependencies with diagrams. ))

### Files and Folders Description

This section provides a detailed description of the files and folders in the codebase, explaining their purpose, key responsibilities, and how they contribute to the overall functionality of the tool at hand.

#### Root Files

(( Here, INSERT a detailed description of the root files in the codebase, explaining their purpose, key responsibilities, and how they contribute to the overall functionality of the tool at hand. Ignore documentation fles. If there is more than one file to describe, use a subsection for each file and label it with "The `<<filename>>` file". ))

#### Subfolders

(( If there are no subfolders, write: "The codebase doesn't contain any subfolder.". Otherwise, write: "The codebase contains the following subfolders." and, then, provide a detailed description of each subfolder's purpose, key responsibilities, and overall contribution; INSERT one subsection per subfolder and label it with "The `<<subfolder-name>>` folder". Further subdivide each subsection into lower level subsections to describe the files within the subfolder ))

## Roadmap

(( Here, INSERT a roadmap of the development of the tool at hand, including planned features, improvements, and milestones. If applicable, illustrate the roadmap with diagrams. ))
