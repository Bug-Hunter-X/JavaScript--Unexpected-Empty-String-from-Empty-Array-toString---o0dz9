# JavaScript: Unexpected Empty String from Empty Array toString()

This repository demonstrates a subtle bug in JavaScript related to the behavior of `toString()` on empty arrays.  The provided code intends to handle `null`, `undefined`, and various other data types by converting them to strings.  However, empty arrays are inadvertently converted to empty strings, which might lead to unexpected behavior in certain applications.  A solution is proposed to address this edge case.

## Bug Description

The `foo` function aims to convert different input types into string representations. While it correctly handles `null`, `undefined`, numbers, and objects, it returns an empty string for empty arrays. This differs from the behavior of other data types and can be counterintuitive.

## Solution

The proposed solution adds a check to specifically handle empty arrays and return a more meaningful string representation, such as "empty array".