# Mission 012 — Tasks, async let and Concurrent Work

## Why this topic matters

Independent work can run concurrently and finish faster, but unmanaged concurrency creates complexity. Structured tasks keep work cancellable and understandable.

## Learning objectives

- Task lifecycle
- async let
- Task groups
- Cancellation
- Priority

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
func loadDashboard() async throws -> (Decimal, [String]) {
    async let balance = MockBalanceService().fetchBalance()
    async let transactions = ["Salary", "Rent", "Groceries"]
    return try await (balance, transactions)
}
```

## Coding exercise

Load profile, accounts and transactions concurrently using `async let`.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Load dashboard sections concurrently while preserving cancellation.

## Interview practice

- When should work run concurrently?
- What benefits do task groups provide?

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
