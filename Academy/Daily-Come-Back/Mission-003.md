# Mission 003 — Automatic Reference Counting

## Why this topic matters

ARC manages memory for classes, but it cannot always detect ownership cycles. Understanding ARC helps prevent leaks, retained screens and poor performance.

## Learning objectives

- Strong references
- Weak references
- Unowned references
- Retain cycles
- deinit

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
final class Customer {
    let name: String
    weak var account: BankAccount?

    init(name: String) {
        self.name = name
    }

    deinit {
        print("Customer released")
    }
}

final class BankAccount {
    weak var owner: Customer?
}
```

## Coding exercise

Build two classes that reference each other, then fix the cycle using `weak`.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Review delegates, coordinators and stored closures for possible retain cycles.

## Interview practice

- What is a retain cycle?
- When should `weak` be used instead of `unowned`?

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
