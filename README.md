# TDD USING PHP: MIN BY COLUMN IN DATABASE TABLE

Imagine that we are working with a simple database. Each row
associates column names (strings) with integer values (for example: 5, 0, -3,
and so on). Here's a table with three rows:
 
 a   b   c   d
---------------
 1   0   0   0
 0   2   3   0
 0   0   0   4
 
We can choose to represent a database table in JSON as an array of objects. For
example, the previous table could be written as:
 
[ {"a": 1, "b": 0, "c": 0, "d": 0},
  {"a": 0, "b": 2, "c": 3, "d": 0},
  {"a": 0, "b": 0, "c": 0, "d": 4} ]
 
(There is no need to use JSON in your solutions -- the notation is just used to
introduce and explain the problems.)
 
Write a function minByColumn that takes a database table (as above), along with a
column, and returns the row that contains the minimum value for the given column.
If a row doesn't have any value for the column, your function should behave as
though the value for that column was zero.
 
In addition to writing this function, you should use tests to demonstrate that it's
correct, either via an existing testing system or one you create.
 
## Examples
 
table1 = [
  {"a": 1},
  {"a": 2},
  {"a": 3}
]
minByColumn(table1, "a") returns {"a": 1}
 
table2 = [
  {"a": 1, "b": 2},
  {"a": 3, "b": 0}
]
minByColumn(table2, "b") returns {"a": 3, "b": 0}
 
table3 = [
  {"a": 1, "b": -2},
  {"a": 3}
]
minByColumn(table3, "b") returns {"a": 1, "b": -2}
