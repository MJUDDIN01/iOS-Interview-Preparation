# Mission 002 — Value Types, Reference Types and Memory

## Why this topic matters

Choosing between structs and classes affects correctness, testability and shared state. Many subtle bugs come from unexpected mutation or shared references.

## Learning objectives

- Structs and classes
- Copy semantics
- Reference semantics
- Identity

## The five questions to ask

1. What problem existed before this feature?
2. What bug or limitation does it prevent?
3. Where would I use it in a real iOS app?
4. What are the trade-offs?
5. How would I explain it in an interview?

## Swift example

```swift
struct Profile {
    var name: String
}

var first = Profile(name: "MJ")
var second = first
second.name = "Jasim"

print(first.name)
print(second.name)
```

## Coding exercise

Create one struct and one class, copy each, mutate the copy and compare the behaviour.

## Testing task

Write one happy-path test and one failure or edge-case test.

## Architecture connection

Explain where this topic belongs in MVC, MVVM or Clean Architecture. Focus on responsibilities and dependency direction.

## Enterprise Banking App task

Model `Transaction` as a struct and explain why value semantics are useful.

## Interview practice

- When would you choose a struct over a class?
- What does value semantics mean in Swift?

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
