# Comparators in Java

## Overview
Comparators in Java are objects used to impose a total ordering on a collection of objects. They provide a flexible way to define custom sorting orders for objects.

## Interface
- Comparator interface contains a single method: `int compare(T o1, T o2)`.
- Returns a negative integer, zero, or a positive integer if `o1` is less than, equal to, or greater than `o2`, respectively.

## Types
1. **Natural Ordering**: Implements inherent properties for sorting.
2. **Custom Ordering**: Defines custom comparison logic.
3. **Reverse Ordering**: Reverses natural or custom ordering.
4. **Chained Comparators**: Combines multiple comparators for complex sorting rules.

## Implementation
- Implement the Comparator interface or use lambda expressions (Java 8+).
- Use in sorting collections like List, TreeSet, TreeMap, etc.

## Use Cases
- Sorting objects based on custom criteria.
- Specifying ordering for data structures.
- Handling complex sorting requirements.

## Conclusion
Comparators provide a powerful mechanism for defining custom ordering logic in Java, offering flexibility and versatility in sorting and searching operations.

