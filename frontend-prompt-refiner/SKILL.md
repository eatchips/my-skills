---
name: frontend-prompt-refiner
description: Refine rough software-development prompts from a senior frontend engineer perspective. Use when the user asks to polish, improve, rewrite, clarify, structure, or strengthen a prompt for frontend or full-stack UI work, including React, Vue, Angular, Next.js, web apps, component design, state management, styling, accessibility, performance, responsive behavior, testing, acceptance criteria, and implementation planning.
---

# Frontend Prompt Refiner

Refine the user's rough request into a clear, implementation-ready prompt that guides an AI coding agent like a senior frontend engineer.

## Workflow

1. Identify the intended product outcome, target users, frontend surface, and expected deliverable.
2. Detect missing context that materially affects implementation quality.
3. Ask at most 3 concise clarification questions only when ambiguity would cause rework; otherwise make explicit assumptions.
4. Rewrite the prompt with concrete requirements, technical constraints, UX expectations, acceptance criteria, and verification steps.
5. Preserve the user's original intent; do not invent product scope beyond useful frontend-quality details.

## Frontend Review Lens

Always consider whether the refined prompt should specify:

- Framework and runtime: React, Vue, Angular, Svelte, Next.js, Vite, SSR/CSR, TypeScript, package manager.
- Architecture: component boundaries, data flow, state ownership, hooks/composables/services, routing, error boundaries.
- UI behavior: loading, empty, error, success, disabled, optimistic, offline, and edge states.
- Styling: design system usage, tokens, theming, responsive layout, dark mode, animation constraints.
- Accessibility: semantic HTML, keyboard support, focus management, ARIA only when needed, color contrast.
- Performance: bundle impact, rendering cost, memoization needs, lazy loading, image optimization, Core Web Vitals.
- Data integration: API contracts, validation, caching, pagination, retries, race conditions, auth/session concerns.
- Testing: unit, component, integration, e2e, visual regression, accessibility checks, and test data.
- Maintainability: file organization, naming, reusable abstractions, migration risk, compatibility with existing code.

## Output Format

Return the refined prompt in this structure unless the user asks for another format:

```markdown
# Refined Prompt

You are a senior frontend engineer. [One-sentence mission.]

## Context
- [Known product/context details]
- Assumptions: [Only list assumptions if any]

## Goal
[Concrete outcome to build, fix, analyze, or plan.]

## Requirements
- [Functional requirement]
- [Frontend behavior requirement]
- [State/error/accessibility/performance requirement]

## Technical Constraints
- [Framework/runtime/library constraints]
- [Existing codebase constraints]
- [Do-not-change boundaries]

## UX & Accessibility
- [Responsive behavior]
- [Keyboard/focus/semantic requirements]
- [Visual and interaction expectations]

## Deliverables
- [Files, code changes, explanation, tests, or plan expected]

## Acceptance Criteria
- [Observable pass/fail criterion]
- [Observable pass/fail criterion]

## Verification
- [Specific commands, checks, or manual QA steps]
```

## Modes

Use the light mode for quick requests: produce only `Refined Prompt`, `Assumptions`, and `Acceptance Criteria`.

Use the deep mode for complex implementation requests: include all output sections and add a short `Risks & Questions` section.

## Quality Rules

- Make the prompt actionable for a coding agent, not just better-written prose.
- Replace vague phrases like "make it better" with observable behavior and quality criteria.
- Include frontend-specific non-functional requirements only when relevant.
- Avoid over-constraining implementation details when the user's repo should determine the best approach.
- Keep the final prompt concise enough to paste directly into an AI coding tool.
