---
name: e2e-testing-patterns
description: Master end-to-end testing with Playwright and Cypress to build reliable test suites that catch bugs, improve confidence, and enable fast deployment. Use when implementing E2E tests, debugging flaky tests, or establishing testing standards.
---

# E2E Testing Patterns

Build reliable, fast, and maintainable end-to-end test suites.

## When to Use This Skill

- Implementing end-to-end test automation
- Debugging flaky or unreliable tests
- Testing critical user workflows
- Setting up CI/CD test pipelines

## Core Concepts

### What to Test with E2E

- Critical user journeys (login, checkout, signup)
- Complex interactions (drag-and-drop, multi-step forms)
- Cross-browser compatibility
- Real API integration
- Authentication flows

### What NOT to Test with E2E

- Unit-level logic (use unit tests)
- API contracts (use integration tests)
- Edge cases (too slow)
- Internal implementation details

## Best Practices

1. **Use Data Attributes**: `data-testid` or `data-cy` for stable selectors
2. **Avoid Brittle Selectors**: Don't rely on CSS classes or DOM structure
3. **Test User Behavior**: Click, type, see - not implementation details
4. **Keep Tests Independent**: Each test should run in isolation
5. **Clean Up Test Data**: Create and destroy test data in each test
6. **Meaningful Assertions**: Check actual user-visible behavior
7. **Optimize for Speed**: Mock when possible, parallel execution

```typescript
// ❌ Bad selectors
cy.get(".btn.btn-primary.submit-button").click();

// ✅ Good selectors
cy.getByRole("button", { name: "Submit" }).click();
cy.getByLabel("Email address").type("user@example.com");
cy.get('[data-testid="email-input"]').type("user@example.com");
```

## Common Pitfalls

- **Flaky Tests**: Use proper waits, not fixed timeouts
- **Slow Tests**: Mock external APIs, use parallel execution
- **Over-Testing**: Don't test every edge case with E2E
- **Coupled Tests**: Tests should not depend on each other
- **Poor Selectors**: Avoid CSS classes and nth-child

## Debugging Failing Tests

```typescript
// Playwright debugging
npx playwright test --headed   // headed mode
npx playwright test --debug    // debug mode

// Add test.step for better reporting
test('checkout flow', async ({ page }) => {
  await test.step('Add item to cart', async () => {
    await page.goto('/products');
    await page.getByRole('button', { name: 'Add to Cart' }).click();
  });
});

await page.pause();  // Pauses execution, opens inspector
```
