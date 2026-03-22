# Case Study: Refactor Slicing for Safety and Throughput

## Problem
A single high-risk refactor would have too much blast radius.

## Approach
Split into deterministic tranches:
- PR A: extraction with behavior parity
- PR B: module decomposition
- PR C: final bootstrap cleanup

## Why it worked
- Reduced review complexity
- Preserved release velocity
- Maintained green CI at each slice
