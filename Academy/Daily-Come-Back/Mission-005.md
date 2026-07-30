# Mission 005 — Capture Lists and Escaping Closures

## Why this topic matters

Closures can outlive the function that created them. If they capture `self` strongly, they can keep objects alive forever.

## Learning objectives

- Escaping vs non-escaping
- Capture lists
- weak self
- Stored closures

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
final class TransferViewModel {
    var onSuccess: (() -> Void)?

    func configureCallback() {
        onSuccess = { [weak self] in
            guard let self else { return }
            self.showConfirmation()
        }
    }

    private func showConfirmation() {
        print("Transfer complete")
    }
}
```

## Coding exercise

Create a stored callback and use `[weak self]` safely.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Audit stored completion handlers and document where `[weak self]` is needed.

## Interview practice

- Why do escaping closures often need capture lists?
- What happens when `self` is captured strongly?

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
