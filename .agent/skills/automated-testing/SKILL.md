---
name: testing-react-components
description: Automates the creation and execution of tests for React components (Vite or Next.js). Use when the user requests component testing, unit tests, Vitest, or Jest setup.
---

# Testing React Components

## When to use this skill
- When a new React or Next.js component is created and needs unit tests.
- When existing components lack test coverage.
- When the user mentions "Vitest", "Jest", "Testing Library", "Next.js testing", or "component tests".

## Workflow
- [ ] Identify the target component and its environment (Vite or Next.js).
- [ ] Check for environment-specific dependencies:
    - **Vite:** `vitest`, `@testing-library/react`.
    - **Next.js:** `jest`, `@testing-library/react`, `jest-environment-jsdom` (or `vitest` setup for Next.js).
- [ ] Create a `.test.tsx` file adjacent to the component.
- [ ] Write test cases covering:
    - [ ] Rendering without crashing.
    - [ ] Interaction (clicks, inputs).
    - [ ] Hooks/Navigation (e.g., `useRouter` mocks).
- [ ] Run the test using `npm test`, `npx vitest`, or `npm run test:watch`.
- [ ] Validate coverage and fix any failures.

## Instructions

### Environment Check
```bash
# Vite
npm list vitest @testing-library/react

# Next.js
npm list jest @testing-library/react next
```

### Test Template (React/Vite)
```typescript
import { render, screen, fireEvent } from '@testing-library/react';
import { describe, it, expect, vi } from 'vitest';
import { MyComponent } from './MyComponent';

describe('MyComponent', () => {
  it('renders correctly', () => {
    render(<MyComponent label="Test" />);
    expect(screen.getByText('Test')).toBeDefined();
  });
});
```

### Test Template (Next.js)
```typescript
import { render, screen } from '@testing-library/react';
import Page from './page';

// Mocking Next.js navigation if needed
jest.mock('next/navigation', () => ({
  useRouter: () => ({ push: jest.fn() }),
  usePathname: () => '/',
}));

describe('Next.js Page', () => {
  it('renders heading', () => {
    render(<Page />);
    expect(screen.getByRole('heading')).toBeInTheDocument();
  });
});
```

### Execution
```bash
# Vitest
npx vitest run path/to/MyComponent.test.tsx

# Next.js / Jest
npm test -- path/to/MyComponent.test.tsx
```

## Resources
- [See examples/MOCK_COMPONENT.md](examples/MOCK_COMPONENT.md) for a full implementation.
