# Mission 008 — Error Handling and Failure Design

## Why this topic matters

Production apps fail. Networks time out, tokens expire and data can be invalid. Good error design makes failures understandable and recoverable.

## Learning objectives

- throw and throws
- do-catch
- Result
- Custom errors
- Recovery

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
enum TransferError: Error {
    case insufficientFunds
    case invalidAmount
}

func validateTransfer(amount: Decimal, balance: Decimal) throws {
    guard amount > 0 else { throw TransferError.invalidAmount }
    guard amount <= balance else { throw TransferError.insufficientFunds }
}
```

## Coding exercise

Create typed login errors and a user-friendly message for each.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Separate transfer validation, authentication and network failures.

## Interview practice

- When would you use `throws` instead of `Result`?
- How should domain errors differ from network errors?

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
