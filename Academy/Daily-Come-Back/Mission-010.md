# Mission 010 — Unit Testing Fundamentals

## Why this topic matters

Tests protect behaviour while code changes. They help you refactor confidently and catch regressions before users do.

## Learning objectives

- Arrange, Act, Assert
- Test naming
- Deterministic tests
- Edge cases

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
import XCTest

final class TransferValidatorTests: XCTestCase {
    func test_validateTransfer_whenAmountExceedsBalance_throwsError() {
        XCTAssertThrowsError(
            try validateTransfer(amount: 200, balance: 100)
        )
    }
}
```

## Coding exercise

Test valid, zero, negative and insufficient-funds cases.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Add tests for transfer validation and balance formatting.

## Interview practice

- What makes a unit test valuable?
- What should not be mocked?

## Engineering journal

- What problem does this topic solve?
- Why would a production team care?
- What is one misuse or trade-off?
- How would I explain it to another developer?
- Where did I apply it in the banking app?

## Completion checklist

- [ ] I understand why this topic exists.
- [ ] I can explain it without notes.
- [ ] I typed and ran the example.
- [ ] I completed the exercise.
- [ ] I added or planned tests.
- [ ] I connected it to architecture.
- [ ] I updated the banking app.
- [ ] I answered the interview questions.
- [ ] I completed the journal.
