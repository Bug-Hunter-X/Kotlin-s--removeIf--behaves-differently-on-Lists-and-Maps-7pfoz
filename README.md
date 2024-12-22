# Kotlin's `removeIf` gotchas

This repository demonstrates a subtle difference in how the `removeIf` function operates on `MutableList` and `MutableMap` in Kotlin.  The example highlights a common error when using `removeIf` with Maps: attempting to remove entries based on their value can lead to unexpected results. The solution shows how to correctly remove entries from a map using a more appropriate approach.

The bug occurs due to `removeIf` being called on the `entries` which are iterators, so the map itself isn't modified in the way that list is. 