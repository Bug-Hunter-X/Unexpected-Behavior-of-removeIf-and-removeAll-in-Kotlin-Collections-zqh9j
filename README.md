# Kotlin Collection Modification Gotcha: removeIf vs. removeAll

This repository demonstrates a subtle difference in behavior between the `removeIf` and `removeAll` functions when used with mutable lists and sets in Kotlin.  While seemingly similar, they have distinct impacts on the original collection.

`removeIf` directly modifies the existing list or set.

`removeAll` creates a *new* list or set containing only the elements that do *not* satisfy the predicate. The original collection remains unchanged.

This difference can easily lead to unexpected behavior if not carefully considered. The example code illustrates this.

Refer to the `bug.kt` and `bugSolution.kt` files for code demonstrating the behavior and its solution.