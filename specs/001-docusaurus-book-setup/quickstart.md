# Quickstart: Docusaurus Book Project

**Date**: 2025-11-30

This guide provides instructions for setting up and running the Docusaurus book project locally.

## Prerequisites

- **Node.js**: You must have a recent LTS version of Node.js installed (e.g., 20.x). You can check your version with `node -v`.
- **npm** or **yarn**: A package manager is required. This guide will use `npm`, which is included with Node.js.

## Setup & Installation

1.  **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2.  **Checkout the feature branch**:
    ```bash
    git checkout 001-docusaurus-book-setup
    ```

3.  **Install dependencies**:
    Navigate to the project root (if you are not already there) and run:
    ```bash
    npm install
    ```
    This will download Docusaurus and all other necessary packages defined in `package.json`.

## Running the Development Server

To start a local development server with hot-reloading, run the following command from the project root:

```bash
npm start
```

This will open a new browser window with the Docusaurus site, typically at `http://localhost:3000`. Any changes you make to the content (Markdown files) or code (React components) will be automatically reflected in the browser.

## Building the Site

To create a production-ready static build of the website, run:

```bash
npm run build
```

The output will be placed in the `build` directory. This is the set of files that will be deployed to GitHub Pages.

## Running Tests

The project is configured to use Jest for component testing and Playwright for end-to-end testing.

- **To run Jest tests**:
  ```bash
  npm test
  ```

- **To run Playwright E2E tests**:
  ```bash
  npx playwright test
  ```
