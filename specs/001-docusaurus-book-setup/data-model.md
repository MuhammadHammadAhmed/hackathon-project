# Data Model: Docusaurus Content

**Date**: 2025-11-30

This document describes the main content entities for the Docusaurus-based book project. As a static site, there is no traditional database-backed data model. Instead, the "data" is the content itself, structured through files and directories.

## Core Entities

### 1. Book Chapter

- **Description**: A single chapter or section of the book.
- **Representation**: A Markdown file (`.md` or `.mdx`) located in the `/docs` directory.
- **Key Attributes**:
    - `title`: The title of the chapter, typically derived from the first H1 heading in the Markdown file or from the front matter.
    - `content`: The body of the chapter, written in Markdown.
    - `slug`: The URL path for the chapter, derived from the file name.
    - `sidebar_position`: An optional number in the front matter to control the order in the sidebar.
- **Relationships**:
    - Chapters are organized into a hierarchical structure defined in `sidebars.js`. This creates the book's table of contents.

### 2. Landing Page

- **Description**: The main home page of the website.
- **Representation**: A React component file (e.g., `index.js`) located in the `src/pages` directory.
- **Key Attributes**:
    - This is a React component, so its "attributes" are its props and state. The content is hardcoded or derived from other sources within the component.
- **Relationships**:
    - It serves as the main entry point to the site and will contain links to the book chapters.

### 3. Static Asset

- **Description**: Images, videos, or other files that are part of the site's content.
- **Representation**: Any file (e.g., `.png`, `.jpg`, `.pdf`) located in the `/static` directory.
- **Relationships**:
    - Static assets can be referenced from any Book Chapter or the Landing Page.
