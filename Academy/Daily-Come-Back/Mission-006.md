# Mission 006 — Protocols and Protocol-Oriented Design

## Why this topic matters

Protocols separate what a type does from how it does it. This makes code easier to replace, test and scale.

## Learning objectives

- Protocol requirements
- Conformance
- Abstraction
- Dependency boundaries

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
protocol BalanceProviding {
    func fetchBalance() async throws -> Decimal
}

struct MockBalanceService: BalanceProviding {
    func fetchBalance() async throws -> Decimal {
        1250
    }
}
```

## Coding exercise

Create a `TransactionProviding` protocol with live and mock implementations.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Introduce protocols for networking and storage.

## Interview practice

- Why use protocols for dependencies?
- What are the trade-offs of protocol-oriented design?

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
