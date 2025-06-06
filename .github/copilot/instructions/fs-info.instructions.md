# Copilot Instructions - `.fs-info` Files

The following instructions are designed to ensure that `.fs-info` files are created and formatted consistently, providing a clear overview of the folder's role and contents. These instructions apply in addition to the general markdown formatting rules specified in `.github/copilot/instructions/markdown.instructions.md`.

The provided description MUST be agnostic to the project and applicable to any project using the same directory structure. The `.fs-info` files are intended to provide a structured overview of the folder's role, typical content, and organization, and are NOT meant to contain project-specific details.

## The `.fs-info` File Template

In the next subsection below is the template to follow for `.fs-info` files. It provides a structured format that MUST be adhered to when creating these files.

- The template's structure, style and sectionning MUST be strictly followed to ensure consistency across the project.

- Replace << path-to-folder >> with the relative path to the folder from the project root, using forward slashes (`/`) as directory separators.

- Never mention the `.fs-info` file itself in the file, as it is implied by its presence in the folder.

### Template to follow

<!-- << path-to-folder >>.fs-info -->
# FS-INFO - << A Short Title, e.g. Styling Documentation Folder >>

!!!Note
    This file provides an overview of the folder's role and **typical** content. If available, a project-specific documentation is to be found in the folder's `README`

## Overview

<< Overview of the folder's role, structure, and contents. Be concise but informative. >>

## Folder's Role

(( Here, INSERT a detailed description of the folder's role in the project. ))

## Folder's Typical Content

(( Here, INSERT a short introduction before digging into the details in the following subsections. ))

### Folder's Typical Tree Structure

Below is the typical structure of the `<< path-to-folder >>` folder:

(( Here, INSERT the folder's typical tree structure as a plaintext as a plaintext doc-block. Follow the rules for ordering subfolders and files. ))

The following sections provide a comprehensive overview of the files and subfolders within the `<< path-to-folder >>` directory.

### Files Description

(( If there are no files, write: "The `<< path-to-folder >>` folder doesn't contain any file.". Otherwise, write: "The typical files to be found in the `<< path-to-folder >>` folder are as follows." and, then, provide a detailed description of each file's purpose, key responsibilities, and overall contribution; INSERT one subsection per file and label as "The `<<filename>>` file". ))

### Subfolders Description

(( If there are no subfolders, write: "The `<< path-to-folder >>` folder doesn't contain any subfolder.". Otherwise, write: "The typical subfolders to be found in `<< path-to-folder >>` folder are as follows." and, then, provide a detailed description of each subfolder's purpose, key responsibilities, and overall contribution; INSERT one subsection per subfolder and label it with "The `<<subfolder-name>>` folder". ))
