# Mission 011 — Asynchronous Programming with async/await

## Why this topic matters

Apps wait for networks, databases and system APIs without freezing the interface. `async/await` makes this easier to read and reason about.

## Learning objectives

- async functions
- await
- Task
- Cancellation
- Structured concurrency

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
func loadBalance() async {
    do {
        let balance = try await MockBalanceService().fetchBalance()
        print(balance)
    } catch {
        print(error)
    }
}
```

## Coding exercise

Create an async function that loads transactions and handles cancellation.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Convert one callback-based service into `async throws`.

## Interview practice

- What does `await` do?
- How does structured concurrency differ from callbacks?

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
