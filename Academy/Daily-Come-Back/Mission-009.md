# Mission 009 — Dependency Injection and Testable Architecture

## Why this topic matters

Dependency injection lets you replace real services with mocks. It reduces coupling and makes code easier to test and change.

## Learning objectives

- Constructor injection
- Protocol dependencies
- Composition root
- Mocks and stubs

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
final class BalanceViewModel {
    private let service: BalanceProviding

    init(service: BalanceProviding) {
        self.service = service
    }
}
```

## Coding exercise

Inject a mock service into a view model and test without a real network call.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Create a central composition point for live dependencies.

## Interview practice

- What problem does dependency injection solve?
- Why is constructor injection usually preferred?

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
