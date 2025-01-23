# Lua pairs() Iterator Bug

This repository demonstrates a potential issue with Lua's `pairs()` iterator when dealing with nested tables that are modified during iteration.  The `bug.lua` file contains code that showcases this behavior.  The `bugSolution.lua` file offers a solution to address this problem.

## Bug Description

The `pairs()` iterator in Lua iterates over the key-value pairs of a table. However, if the table's structure is modified (e.g., elements added or removed) during iteration, the iterator might behave unexpectedly. It may skip elements or visit elements multiple times.  This is a common issue when recursively traversing tables.

## Solution

The best solution to prevent this error depends on the context.  Sometimes a simple copy is enough.  A more robust solution involves using a separate list to maintain iteration order independent of changes to the original table. This is demonstrated in `bugSolution.lua`.