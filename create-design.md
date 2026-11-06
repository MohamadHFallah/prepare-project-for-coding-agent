
You are acting as a Senior Frontend Architect,
UI Engineer, and Design Systems Specialist.

I have an existing, fully functional Next.js
e-commerce application built with:

- React
- Next.js
- TypeScript
- Tailwind CSS
- shadcn/ui
- Radix UI (if used in the project)

Your task is to analyze the existing application
and create a project-specific design.md file.

The goal is to establish consistent UI/UX
guidelines that AI coding agents must follow
when creating or modifying frontend components.

IMPORTANT RULES:

- Do not modify application source code.
- Do not redesign existing pages.
- Do not install dependencies.
- Do not introduce new UI libraries.
- Do not invent design tokens or conventions.
- Analyze the actual implementation.
- Document existing patterns rather than assuming
  default shadcn/ui styles.

# 1. Required Documentation

Read:

- AGENTS.md
- docs/architecture.md
- docs/project-structure.md
- Existing UI-related documentation
- package.json
- tailwind.config.* (if present)
- postcss.config.*
- components.json
- Global CSS files
- Existing theme configuration

# 2. Analyze Existing UI Architecture

Inspect the project structure and identify:

- Application layout structure
- Shared UI components
- Feature-specific components
- Admin dashboard components
- Public storefront components
- Form components
- Navigation components
- Dialogs and modals
- Tables and data grids
- Loading and skeleton components
- Empty states
- Error states

Identify which components come from shadcn/ui
and which are custom implementations.

Document actual file paths.

# 3. Design System Analysis

Analyze the existing visual design system.

## A. Colors

Inspect:

- Primary colors
- Secondary colors
- Background colors
- Foreground colors
- Border colors
- Muted colors
- Accent colors
- Destructive colors
- Success and warning colors
- Dark mode colors, if supported

Identify CSS variables and Tailwind tokens.

Do not invent new color values.

## B. Typography

Inspect:

- Font families
- Font weights
- Font sizes
- Heading hierarchy
- Body text
- Labels
- Helper text
- Button typography

Document the actual typography system.

## C. Spacing and Layout

Analyze:

- Container widths
- Page padding
- Section spacing
- Component gaps
- Grid layouts
- Responsive breakpoints
- Sidebar dimensions
- Header dimensions
- Content alignment

Document established spacing patterns.

## D. Borders, Shadows and Radius

Inspect:

- Border styles
- Border radius
- Shadow usage
- Card appearance
- Input appearance
- Button appearance

Identify the actual conventions.

# 4. shadcn/ui Guidelines

Inspect existing shadcn/ui components.

Document:

- Component installation structure
- Component customization patterns
- Variants and sizes
- Composition patterns
- Class Variance Authority usage, if present
- cn() utility implementation
- Radix UI integration, if present

Define rules for:

- Reusing existing components
- Extending component variants
- Creating custom components
- Avoiding duplicate UI components
- Maintaining consistent styling

Never recommend reinstalling or replacing
components that already exist.

# 5. Tailwind CSS Guidelines

Analyze the actual Tailwind version and configuration.

Document:

- Utility class conventions
- Theme configuration
- CSS variables
- Responsive design conventions
- Dark mode strategy
- Arbitrary value usage
- Class merging strategy
- Custom utility classes
- Global styles

Use the existing Tailwind version and syntax.

Do not assume Tailwind v3 or v4.
Verify the installed version first.

# 6. Responsive Design

Inspect how the application behaves across:

- Mobile
- Tablet
- Desktop
- Large desktop

Document:

- Breakpoint usage
- Responsive navigation
- Sidebar behavior
- Responsive tables
- Responsive forms
- Product grids
- Dialog behavior
- Mobile-specific layouts

Use existing responsive conventions.

# 7. RTL and Multilingual UI

This application supports multiple languages.

Inspect:

- RTL and LTR layouts
- Direction handling
- Logical CSS properties
- Icon positioning
- Text alignment
- Form field direction
- Navigation direction
- Responsive behavior in RTL

Document rules for building components
that work correctly in both RTL and LTR.

Avoid hardcoded left/right positioning
when logical CSS properties are appropriate.

# 8. UX Patterns

Analyze existing implementations of:

- Forms and validation
- Loading states
- Skeletons
- Toast notifications
- Confirmation dialogs
- Error messages
- Empty states
- Search and filtering
- Pagination
- Tables
- Dropdown menus
- Tooltips
- Destructive actions

Document the established UX conventions.

# 9. Accessibility

Inspect current accessibility practices.

Document rules for:

- Semantic HTML
- Keyboard navigation
- Focus management
- Accessible labels
- ARIA attributes
- Color contrast
- Dialog accessibility
- Form error announcements

Identify gaps separately.

# 10. E-commerce UI Patterns

Pay special attention to the existing storefront
and admin dashboard.

Inspect:

- Product cards
- Product detail pages
- Product image galleries
- Product listing grids
- Category navigation
- Shopping cart UI
- Quantity selectors
- Price display
- Admin product forms
- Admin data tables
- Category management forms

Document reusable patterns and conventions.

# 11. Create design.md

Create:

design.md

The document must include:

1. Design System Overview
2. Technology Stack
3. Project UI Architecture
4. Color System
5. Typography
6. Spacing and Layout
7. Borders, Shadows and Radius
8. shadcn/ui Usage Guidelines
9. Tailwind CSS Guidelines
10. Component Architecture
11. Responsive Design
12. RTL and LTR Guidelines
13. UX Interaction Patterns
14. Accessibility Guidelines
15. E-commerce UI Patterns
16. Do's and Don'ts
17. UI Implementation Workflow

# 12. UI Implementation Workflow

Define a reusable workflow for coding agents:

1. Inspect existing components.
2. Identify reusable UI patterns.
3. Read design.md.
4. Check RTL/LTR requirements.
5. Use existing design tokens.
6. Reuse shadcn/ui components.
7. Avoid unnecessary dependencies.
8. Implement responsive layouts.
9. Validate accessibility.
10. Verify visual consistency.
11. Run existing lint and type checks.

# 13. Final Requirements

The final design.md must:

- Describe the actual design system.
- Reference real file paths.
- Include examples from existing components.
- Document actual CSS variables and tokens.
- Avoid generic design advice.
- Avoid inventing colors or typography.
- Separate existing conventions from recommendations.
- Identify inconsistencies and technical debt.
- Be useful for future AI coding agents.

Do not modify application source code.
Only create design.md.

Finally, summarize:
- Existing design system
- Important reusable components
- Identified UI inconsistencies
- Missing design documentation
- Recommendations for future UI development
