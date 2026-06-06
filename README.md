# Build Web App Skill

A Codex skill for building, extending, debugging, and verifying production-quality web applications.

It guides Codex to understand the existing repository and technology stack before implementation, then validate the result with automated checks and browser testing instead of producing isolated code snippets.

## Capabilities

- Create websites, dashboards, landing pages, and web applications from scratch
- Build pages and components in existing React, Next.js, Vue, and Svelte projects
- Translate product briefs, designs, or screenshots into working interfaces
- Integrate APIs and handle loading, empty, error, and validation states
- Improve responsive layouts, keyboard navigation, and accessibility
- Debug browser-facing issues and verify critical user journeys
- Run formatting, type checks, tests, builds, and visual inspections

## Design Principles

- Reuse the project's existing framework, components, and design system
- Deliver complete, end-to-end functionality instead of disconnected scaffolding
- Account for loading, empty, error, and success states
- Use semantic HTML with keyboard-operable controls and visible focus
- Verify meaningful UI changes at desktop and mobile viewport sizes
- Avoid decorative cards, gradients, and motion that do not support the product

## Repository Structure

```text
build-webapp-skill/
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- ui-quality.md
    `-- verification.md
```

- `SKILL.md`: Core workflow and engineering constraints
- `agents/openai.yaml`: Display metadata and default prompt
- `references/ui-quality.md`: Visual design, responsive, and accessibility guidance
- `references/verification.md`: Automated and browser verification checklist

## Installation

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/shushiha/build-webapp-skill.git ~/.codex/skills/build-webapp
```

On Windows PowerShell:

```powershell
git clone https://github.com/shushiha/build-webapp-skill.git "$HOME\.codex\skills\build-webapp"
```

Restart Codex or begin a new session after installation.

## Usage Examples

```text
Use $build-webapp to build a responsive SaaS dashboard.
```

```text
Use $build-webapp to add an account settings page to this Next.js project.
```

```text
Use $build-webapp to inspect this page's mobile layout, keyboard navigation,
and error states, then fix the issues you find.
```

## Workflow

1. Inspect the repository structure, dependencies, routes, styles, and tests.
2. Convert the request into observable acceptance criteria.
3. Plan the smallest complete end-to-end implementation.
4. Implement the feature using established project patterns.
5. Run automated checks and verify the primary flow in a browser.
6. Fix issues discovered during verification and summarize the result.

## License

No open-source license has been declared yet. Public visibility does not automatically grant permission to copy, modify, or redistribute this project.
