# UI Quality

Use this guide when creating or substantially changing a visual interface.

## Direction

Choose a visual direction that fits the product, audience, and existing brand. Define:

- One dominant typography approach
- A restrained color system with clear semantic roles
- A spacing and radius rhythm
- A recognizable treatment for surfaces, borders, and elevation
- A consistent interaction style

Avoid a generic collection of cards, gradients, and oversized headings unless the product calls for it.

## Hierarchy

- Give each screen one obvious primary purpose.
- Make the primary action visually distinct from secondary actions.
- Group related controls and separate unrelated regions with spacing before adding borders.
- Keep line lengths readable and information density appropriate to the task.
- Use headings in a logical order.

## Responsive Design

- Design for narrow and wide viewports, not one fixed canvas.
- Let content reflow instead of merely shrinking.
- Keep touch targets comfortably sized.
- Avoid horizontal scrolling except for intentionally scrollable data regions.
- Test long labels, long content, empty data, and validation messages.

## Interaction States

Provide visible states for:

- Hover and keyboard focus
- Pressed or selected controls
- Loading and progress
- Empty results
- Recoverable errors
- Disabled actions
- Success confirmation

Do not rely on color alone to communicate state.

## Accessibility

- Prefer native semantic elements.
- Associate labels, descriptions, and errors with form controls.
- Preserve a logical tab order and operability without a mouse.
- Ensure focus remains visible and moves predictably after dialogs or navigation.
- Use ARIA only where native HTML cannot express the behavior.
- Respect zoom, text scaling, color contrast, and reduced motion.

## Assets

- Reuse repository assets and icon systems first.
- Prefer real product imagery or intentional illustrations over meaningless placeholders.
- Reserve generated imagery for cases where it supports the requested concept and licensing expectations.
- Provide useful alternative text for informative images and empty alternative text for decorative images.
