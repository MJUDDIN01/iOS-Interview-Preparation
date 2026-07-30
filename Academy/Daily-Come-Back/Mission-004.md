# Mission 004 — Closures and Behaviour as Data

## Why this topic matters

Closures let you pass behaviour around. They power callbacks, sorting, animations, completion handlers and much of SwiftUI.

## Learning objectives

- Closure syntax
- Parameters and return values
- Trailing closures
- Capturing values

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
let transactions = [120, 35, 500, 75]

let largeTransactions = transactions.filter { amount in
    amount >= 100
}

print(largeTransactions)
```

## Coding exercise

Use `map`, `filter` and `sorted` on an array of transaction amounts.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Add a reusable transaction filter that accepts a closure.

## Interview practice

- What is a closure?
- Why are closures useful in asynchronous APIs?

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
