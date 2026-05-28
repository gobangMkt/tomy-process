---
name: Test Case Creation
description: Create effective test cases and scenarios based on requirements to ensure full coverage and traceability
---

# Test Case Creation Skill

## Purpose
Translate requirements into executable steps to verify the system works as expected.

## When to Use
- During Requirements phase (to ensure testability)
- UAT Planning (writing scripts for users)
- Reviewing QA Test Plans (validation)

## Anatomy of a Good Test Case

1. **ID**: Unique (e.g., TC-001)
2. **Title**: Concise summary
3. **Preconditions**: Setup required (e.g., "User logged in")
4. **Test Steps**: Step-by-step actions using imperative verbs ("Click", "Enter", "Verify")
5. **Test Data**: Specific data used (e.g., "Email: test@example.com")
6. **Expected Result**: What should happen? (Specific)
7. **Postconditions**: State after test

## Types of Test Cases

### 1. Happy Path (Positive)
The standard flow working perfectly.

### 2. Negative Path (Error Handling)
Trying to break it / Invalid inputs.

### 3. Edge Cases (Boundary)
Testing limits.
- "User enters exactly 255 characters (max) → Accepted."
- "User enters 256 characters → Rejected."

### 4. Business Logic / Complex Flow
Multi-step scenarios.

## Test Case Template

| ID | TC-PROMO-01 |
|----|-------------|
| **Description** | Verify 'SUMMER20' gives 20% discount. |
| **Preconditions** | User has $100 item in cart. |
| **Steps** | 1. Navigate to Cart. 2. Enter 'SUMMER20'. 3. Click 'Apply'. |
| **Expected Result** | 1. Success message. 2. Discount -$20.00. 3. Total $80.00. |

## Best Practices
- **One Verification per Test**: Don't test 10 things in one case.
- **Be Specific**: Don't say "Check result". Say "Verify text says 'Success'".
- **Clean Up**: Tests should clean up data so the next test isn't blocked.
