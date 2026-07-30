# Mission 007 — Generics and Reusable Type-Safe Code

## Why this topic matters

Generics let you reuse logic without losing type safety. They reduce duplication while keeping compile-time guarantees.

## Learning objectives

- Generic functions
- Generic types
- Constraints
- Associated types

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
struct APIResponse<Value> {
    let value: Value
    let statusCode: Int
}

let balanceResponse = APIResponse(value: Decimal(900), statusCode: 200)
let nameResponse = APIResponse(value: "MJ", statusCode: 200)
```

## Coding exercise

Build a generic `ResultBox<Value>` with success and error states.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Model account and transaction API responses generically.

## Interview practice

- Why are generics better than `Any`?
- What is a generic constraint?

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
