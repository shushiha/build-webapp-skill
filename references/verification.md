# Web App Verification

Use the strongest checks supported by the repository and available tools.

## Automated Checks

Run relevant commands in this order when available:

1. Formatter or formatting check
2. Type checker
3. Linter
4. Focused unit or integration tests
5. Production build
6. End-to-end tests

Do not broaden fixes into unrelated pre-existing failures. Report those separately.

## Browser Checks

Open the local app and verify:

- The requested route loads without console errors.
- The primary user journey works from start to finish.
- Loading, empty, error, and success states are reachable or reasonably simulated.
- Forms validate and preserve useful user input after recoverable errors.
- Links, buttons, menus, dialogs, and keyboard navigation behave correctly.
- Network failures do not leave the interface stuck or misleading.
- Layout works at approximately 375 px, 768 px, and a desktop width.
- No important content is clipped, overlapped, or hidden.
- Refreshing a deep route works when routing should support it.

Capture a screenshot when visual comparison or user review benefits from it.

## Fallback Order

If full browser verification is unavailable:

1. Run the production build and automated tests.
2. Inspect rendered markup and styling paths statically.
3. Verify component states with existing story or test tooling.
4. State exactly what could not be exercised and why.

Compilation alone does not validate layout or interaction quality.
