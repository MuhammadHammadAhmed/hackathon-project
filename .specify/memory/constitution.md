<!--
Sync Impact Report:
- Version change: N/A (initial version 1.0.0)
- Modified principles: All principles were defined for the first time.
- Added sections: "Technical Stack & Tools", "Rapid Iteration & Collaboration"
- Removed sections: None
- Templates requiring updates:
    - .specify/templates/plan-template.md: ⚠ pending
    - .specify/templates/spec-template.md: ⚠ pending
    - .specify/templates/tasks-template.md: ⚠ pending
    - .specify/commands/*.toml: ⚠ pending
    - README.md: ⚠ pending
- Follow-up TODOs: None
-->
# Hackathon Unified Book Project Constitution

## Core Principles

### I. AI-Driven Development (Claude Code & Spec-Kit Plus)
All content creation, code generation, and development tasks will leverage AI tools, specifically Claude Code for code and text generation, and Spec-Kit Plus for spec-driven development.

### II. Spec-Driven Development
Features and content must be defined by clear, testable specifications before implementation begins. This ensures alignment with project goals and facilitates AI-driven generation.

### III. Testability & Verification
Every deliverable, including book content and chatbot functionality, must be testable and verifiable against its specifications. Automated tests will be prioritized.

### IV. Modularity & Reusability
Components (e.g., book sections, RAG modules) should be designed to be modular, self-contained, and reusable where possible to accelerate development and maintainability.

### V. Integrated RAG Chatbot
The RAG chatbot will be seamlessly integrated into the Docusaurus book, providing context-aware answers to user queries based *only* on the book's content, including user-selected text.

### VI. Open Source & Community Focus
All project artifacts (code, documentation, book content) will be open-sourced. Tools and processes will prioritize open standards and community-supported solutions where feasible.

## Technical Stack & Tools

**Book Platform:** Docusaurus, deployed to GitHub Pages.
**AI Code Generation:** Claude Code.
**Spec-Driven Framework:** Spec-Kit Plus.
**RAG Chatbot Frameworks:** OpenAI Agents/ChatKit SDKs (for agent orchestration), FastAPI (for API backend).
**Database:** Neon Serverless Postgres.
**Vector Database:** Qdrant Cloud Free Tier.

## Rapid Iteration & Collaboration

**Version Control:** All changes will be managed via Git, with clear commit messages and feature branches.
**Collaboration:** Utilize a shared development environment or clear hand-off points to facilitate parallel work on book content and chatbot development.
**Prioritization:** Focus on core deliverables first, followed by enhancements. Timeboxing will be crucial for hackathon success.

## Governance

This constitution defines the fundamental principles and technical choices for the hackathon project.
Amendments require team consensus and must be documented with rationale.
Compliance with these principles will be reviewed regularly during the hackathon.

**Version**: 1.0.0 | **Ratified**: 2025-11-29 | **Last Amended**: 2025-11-29
