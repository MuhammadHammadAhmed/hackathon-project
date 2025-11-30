# Feature Tasks: Docusaurus Book Setup

**Branch**: `001-docusaurus-book-setup` | **Date**: 2025-11-30 | **Spec**: [spec.md](./spec.md)
**Plan**: [plan.md](./plan.md)

This document outlines the implementation tasks for the "Docusaurus Book Setup" feature, generated from the feature specification and implementation plan.

## Phase 1: Project Setup

This phase focuses on initializing the Docusaurus project.

- [ ] T001 Initialize a new Docusaurus classic project in a temporary directory.
- [ ] T002 Move the contents of the initialized project to the repository root.
- [ ] T003 Install project dependencies by running `npm install`.

## Phase 2: Foundational Setup

This phase establishes the testing foundation for the project.

- [ ] T004 Install and configure Jest for component testing.
- [ ] T005 Install and configure Playwright for end-to-end testing.

## Phase 3: User Story 1 - Initialize Docusaurus Project

**Goal**: To have a foundational structure for the book and website.
**Independent Test**: Can be tested by running the Docusaurus development server and verifying the site title and initial content.

- [ ] T006 [US1] Update `docusaurus.config.js` to set the `title` to "Physical AI & Humanoid Robotic" and configure other project-level settings like the GitHub URL.
- [ ] T007 [US1] Create an initial introductory chapter file at `docs/intro.md`.
- [ ] T008 [US1] Update `sidebars.js` to include the introductory chapter in the book's sidebar.
- [ ] T009 [US1] Write a Playwright test to verify that the main page loads and the title is correct.

## Phase 4: User Story 2 - Create Custom Landing Page

**Goal**: To provide a visually appealing and informative introduction to the book.
**Independent Test**: The landing page can be viewed in a browser and compared against the design specification.

- [ ] T010 [US2] Replace the default content of `src/pages/index.js` with a new React component for the custom landing page.
- [ ] T011 [P] [US2] Implement the hero section (title, subtitle, main image) in the landing page component at `src/pages/index.js`.
- [ ] T012 [P] [US2] Implement the book description section in the landing page component at `src/pages/index.js`.
- [ ] T013 [P] [US2] Implement the footer section in the landing page component at `src/pages/index.js`.
- [ ] T014 [US2] Write a Jest component test for the hero section of the landing page.
- [ ] T015 [US2] Update the Playwright E2E test to verify that the custom landing page is displayed correctly.

## Phase 5: User Story 3 - Deploy to GitHub Pages

**Goal**: To make the book and landing page publicly accessible.
**Independent Test**: The deployment process can be triggered, and the resulting URL can be checked.

- [ ] T016 [US3] Update `docusaurus.config.js` with the necessary fields for GitHub Pages deployment (`organizationName`, `projectName`, `deploymentBranch`).
- [ ] T017 [US3] Create a new GitHub Actions workflow file at `.github/workflows/deploy.yml` that builds and deploys the Docusaurus site to the `gh-pages` branch on every push to `main`.
- [ ] T018 [US3] Manually trigger the deployment workflow and verify that the site is accessible at the GitHub Pages URL.

## Phase 6: Polish & Cross-Cutting Concerns

This phase focuses on quality checks and final improvements.

- [ ] T019 [P] Review all content and code for quality and consistency.
- [ ] T020 [P] Run a Lighthouse audit on the deployed site and ensure the performance score is 85 or higher.
- [ ] T021 [P] Manually check all links on the deployed site to ensure there are no broken links.

## Dependencies

- **User Story 1** is a prerequisite for all other user stories.
- **User Story 2** should be completed before the final deployment in **User Story 3** is fully validated.

## Parallel Execution

- Tasks within **User Story 2** (T011, T012, T013) can be developed in parallel.
- The configuration for **User Story 3** (T016) can be done in parallel with the development of **User Story 2**.

## Implementation Strategy

The implementation will follow an MVP-first approach.
1.  **MVP**: Complete User Story 1 to get a basic, functional book website online.
2.  **Iteration 2**: Complete User Story 2 to enhance the user experience with a custom landing page.
3.  **Iteration 3**: Complete User Story 3 to automate the deployment process, ensuring the site is always up-to-date.
This incremental approach ensures that a valuable product is delivered at each stage.
