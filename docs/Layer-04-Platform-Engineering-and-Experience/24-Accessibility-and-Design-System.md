# Accessibility and Design System

## Accessibility Target
Target WCAG 2.2 AA for supported web experiences.

## Requirements
- Keyboard navigation.
- Visible focus.
- Semantic HTML.
- Accessible labels.
- Screen-reader support.
- Sufficient contrast.
- Logical heading hierarchy.
- Accessible error messages.
- Reduced-motion support.
- No status conveyed only by color.
- Touch targets suitable for mobile.
- Map alternatives for essential information.

## Components Requiring Dedicated Testing
- Search input/autocomplete.
- Filter controls.
- Result cards.
- Map/list synchronization.
- Place profile.
- Comparison view.
- Modals/dialogs.
- Tabs.
- Forms.
- Claim workflow.
- Contribution workflow.

## Design System
Centralize:
- Typography.
- Spacing.
- Radius.
- Elevation.
- Semantic color tokens.
- Interactive states.
- Icons.
- Breakpoints.
- RTL behavior.
- Motion.
- Component variants.

## Component Rules
Components should:
- Expose accessible names.
- Support RTL.
- Support localization expansion.
- Avoid fixed text widths.
- Have documented states.
- Include loading, empty, error, disabled, and permission-denied states.

## Testing
Use automated accessibility checks plus manual keyboard and screen-reader testing for critical journeys. Automated tools cannot verify all usability or semantic problems.
