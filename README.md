# Unexpected NaN Comparison in JavaScript

This repository demonstrates an uncommon bug in JavaScript related to comparing NaN (Not a Number) values.  The unexpected behavior arises from how JavaScript handles NaN in both loose (==) and strict (===) equality comparisons. 

## The Bug
The `foo` function is intended to check if two values are equal. However, when both `a` and `b` are NaN, it incorrectly returns `false` because NaN is not equal to itself.  This behavior is inconsistent with the expectation that two identical NaN values should be considered equal in a comparison. 

## The Solution
The solution involves using the `Number.isNaN()` function to explicitly check for NaN values.  This function reliably detects NaN, ensuring correct comparison logic.