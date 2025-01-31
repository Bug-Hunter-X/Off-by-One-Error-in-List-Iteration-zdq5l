# Off-by-One Error in Dart List Iteration

This repository demonstrates a common off-by-one error in Dart when iterating over a list using a `for` loop. The error arises from incorrectly accessing an index beyond the valid bounds of the list, leading to an exception.

## Bug Description
The provided Dart code attempts to sum the elements of an integer list. However, the `for` loop's condition `i <= numbers.length` is incorrect.  List indices are zero-based, so the valid indices range from 0 to `numbers.length - 1`. Accessing `numbers[numbers.length]` results in an `IndexOutOfRangeException`.

## Solution
The solution corrects the loop condition to `i < numbers.length`, ensuring that only valid indices are accessed.