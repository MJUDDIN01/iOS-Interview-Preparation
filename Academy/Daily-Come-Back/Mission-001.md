# Mission 001 — Engineering Mindset and How iOS Applications Work

## Why this topic matters

Strong engineers do not only memorise syntax. They understand how user actions travel through views, state, business logic, networking and storage. This helps you debug faster and make better design decisions.

## Learning objectives

- What an iOS app is made of
- Inputs, state, logic and outputs
- App flow at a high level

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
struct Account {
    let name: String
    var balance: Decimal

    mutating func deposit(_ amount: Decimal) {
        balance += amount
    }
}

var account = Account(name: "Current Account", balance: 100)
account.deposit(50)
print(account.balance)
```

## Coding exercise

Write a `SavingsGoal` type with a target, current amount and a method that adds money.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Describe how a tap on “Transfer” moves through validation, business logic and UI updates.

## Interview practice

- How would you explain the flow of data through an iOS app?
- What is the difference between syntax knowledge and engineering judgement?

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
