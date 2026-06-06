---
name: build-webapp
description: Build, extend, debug, and polish production-quality web applications and frontend interfaces. Use when Codex needs to create a web app or website, implement pages or components, translate a product brief or screenshot into UI, add interactive behavior, improve responsive design or accessibility, connect frontend code to APIs, fix browser-facing bugs, or verify a local app in a browser. Applies to existing repositories and greenfield projects using HTML/CSS/JavaScript, React, Next.js, Vue, Svelte, and similar web stacks.
---

# Build Web App

Deliver working web experiences, not isolated snippets. Inspect the repository, preserve its conventions, implement the requested behavior, and verify the result at realistic viewport sizes.

## Workflow

1. Inspect the repository before choosing an approach.
   - Read package manifests, framework configuration, routes, shared components, styling conventions, tests, and run scripts.
   - Check the working tree and preserve unrelated user changes.
   - Reuse the existing framework, design system, dependencies, and local utilities.

2. Convert the request into observable outcomes.
   - Identify primary users, core actions, required states, data sources, and acceptance criteria.
   - Infer small missing details when the repository or request makes the intent clear.
   - Ask only when an unresolved choice would materially change the product or cause destructive work.

3. Plan the smallest complete implementation.
   - Identify the pages, components, state, API boundaries, and tests that must change.
   - Prefer a thin vertical slice that works end to end over disconnected scaffolding.
   - Avoid new dependencies unless they remove substantial complexity or match repository practice.

4. Implement using local patterns.
   - Keep components focused and state ownership explicit.
   - Model loading, empty, error, success, disabled, and validation states where applicable.
   - Use semantic HTML, keyboard-operable controls, visible focus, and meaningful labels.
   - Keep secrets and privileged operations out of browser code.
   - Do not rewrite unrelated modules or replace the project's visual language without a clear requirement.

5. Verify behavior and presentation.
   - Run the narrowest relevant formatter, type check, lint, unit tests, and build.
   - Start the application when feasible and inspect it in a browser.
   - Exercise the primary flow and inspect desktop and mobile layouts.
   - Check for console errors, broken requests, overflow, clipping, unreadable contrast, and missing interaction feedback.
   - Treat visual inspection as required for meaningful UI changes.

6. Finish cleanly.
   - Fix defects discovered during verification.
   - Summarize what changed and which checks ran.
   - State any unverified behavior or external dependency plainly.

## Product And UI Decisions

- Read [references/ui-quality.md](references/ui-quality.md) before creating a new visual direction, translating a screenshot, or making substantial layout changes.
- Match an established design system when one exists.
- For greenfield work, choose one coherent visual direction appropriate to the product instead of assembling generic dashboard patterns.
- Prioritize clear hierarchy, legible typography, deliberate spacing, useful empty states, and responsive behavior.
- Use motion sparingly to clarify state changes; respect reduced-motion preferences.
- Do not add decorative elements that compete with the primary task.

## Engineering Decisions

- Prefer server-rendered or static output when the chosen framework and product needs allow it.
- Keep server-only credentials and sensitive business logic behind server boundaries.
- Validate data at trust boundaries and render user-controlled content safely.
- Preserve URL-addressable state for navigation, filters, tabs, or selected records when it improves usability.
- Avoid premature abstraction. Extract shared code after repeated behavior is evident or when the repository already establishes the abstraction.
- Add tests in proportion to risk: focused tests for isolated logic, integration tests for shared workflows, and browser tests for critical user journeys.

## Browser Verification

Use the available browser-control capability after significant frontend changes when a local target is known or can be started. Read [references/verification.md](references/verification.md) for the completion checklist and practical fallback order.

Do not claim a UI is complete solely because it compiles.

## Common Requests

- "Build a responsive landing page for this product."
- "Add an authenticated settings page to this Next.js app."
- "Turn this screenshot into a reusable React interface."
- "Fix the mobile layout and keyboard accessibility."
- "Connect this form to the existing API and handle errors."
- "Run the app, test the main flow, and polish anything visibly broken."
