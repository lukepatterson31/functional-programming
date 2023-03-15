# Functional Programming

## Typeclasses

### Monoids

| Things | Operation | Closed? | Associative? | Identity? | Classification |
|---------|------------|----------|---------------|-----------|----------------|
| Int32 | Addition | Yes | Yes | 0 | Monoid |
| Int32 | Multiplication | Yes | Yes | 1 | Monoid |
| Int32 | Subtraction | Yes | No | 0 | Other |
| Int32 | Max | Yes | Yes | Int32.MinValue | Monoid |
| Int32 | Equality | No |  |  | Other |
| Int32 | Less than | No |  |  | Other |
| Float | Multiplication | Yes | No (See note 1) | 1 | Other |
| Float | Division | Yes (See note 2) | No | 1 | Other |
| Positive Numbers | Addition | Yes | Yes | No identity | Semigroup |
| Positive Numbers | Multiplication | Yes | Yes | 1 | Monoid |
| Boolean | AND | Yes | Yes | true | Monoid |
| Boolean | OR | Yes | Yes | false | Monoid |
| String | Concatenation | Yes | Yes | Empty string "" | Monoid |
| String | Equality | No |  |  | Other | 
| String | "subtractChars" | Yes | No | Empty string "" | Other |
| List | Concatenation | Yes | Yes | Empty list [] | Monoid |
| List | Intersection | Yes | Yes | No identity | Semigroup |

[Note 1] Floats are not associative. Replace ‘float’ with ‘real number’ to get associativity.

[Note 2] Mathematical real numbers are not closed under division, because you cannot divide by zero and get another real number. However, with IEEE floating point numbers you can divide by zero and get a valid value. So floats are indeed closed under division! Here’s a demonstration:
```
let x = 1.0/0.0 // infinity
let y = x * 2.0 // two times infinity
let z = 2.0 / x // two divided by infinity
```
