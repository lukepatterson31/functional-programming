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

