# Examples

## Rough Prompt

Build a dashboard page for orders and make it look good.

## Refined Prompt

# Refined Prompt

You are a senior frontend engineer. Build a responsive orders dashboard that helps operations users quickly understand order volume, status, and exceptions.

## Context
- The app is a TypeScript frontend; infer existing framework and style conventions from the repo.
- Assumptions: use existing components, tokens, routing, and API utilities when available.

## Goal
Create an orders dashboard page with summary metrics, filterable order status views, and clear loading/error/empty states.

## Requirements
- Show summary cards for total orders, pending orders, fulfilled orders, failed orders, and revenue if data exists.
- Provide filters for status and date range without losing current view state on refresh if the app already has URL-state patterns.
- Render loading skeletons, empty states, and recoverable API error states.
- Keep data-fetching logic separate from presentational components when consistent with the repo.

## Technical Constraints
- Follow the existing frontend framework, routing, styling, and test conventions.
- Do not introduce a new design system, charting library, or state library unless the repo already uses it or the change is justified.

## UX & Accessibility
- Support desktop and mobile layouts.
- Use semantic headings, accessible form labels, keyboard-operable filters, and visible focus states.
- Ensure status colors are paired with text labels, not color alone.

## Deliverables
- Implement the dashboard page and any reusable components.
- Add or update relevant tests.
- Briefly summarize changed files and tradeoffs.

## Acceptance Criteria
- Users can view order metrics and filter the order list by status/date.
- Loading, empty, and API error states are visible and understandable.
- The page is responsive and keyboard accessible.
- Existing tests pass, and new behavior has appropriate coverage.

## Verification
- Run the repo's relevant frontend tests and type checks.
- Manually verify desktop and mobile layouts.
