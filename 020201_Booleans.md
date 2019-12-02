---
layout: default
---

# Booleans Overview
[Home](./)

## Intro
There are many different data types used in computer programming. We have already used two of these types: 
* **String**: for text
* **Integer**: for whole numbers

Boolean is another type of data. A boolean data type has only two values: true or false.
In true binary fashion, these two values can be represented by the numbers 1 = true, and 0 = false.

Booleans are useful in programming for decision-making, often deciding when certain functions and parts of programs should start or stop running and are also used in database searches.

What things can you think of that have only two values or states?

Since we have already worked with conditionals and loops, we have already worked with this type of logic: 
* If a certain condition is true, do this, otherwise (if condition is false), do something else.
* While a certain condition is true, do this

## Boolean Operators: AND, OR, and NOT
To make working with Booleans useful for solving more complex decisions and searches, we can connect two or more Booleans into one decision statement. To do this, we use what are known as Boolean operators. The three most common and the ones we will use with the micro:bit are And, Or, and Not.

These operators can be used in conditionals and loops, like so:
* If condition A is true AND condition B is true
* If condition A is true OR condition B is true
* While event A has NOT happened
 
Let’s look at how each of these work.

### AND
(Condition A AND Condition B)

For this expression to evaluate as true, both conditions in the expression need to be true.
So, if both Condition A AND Condition B are true, the expression will evaluate as or return true.
 
### OR
(Condition A OR Condition B)

For this expression to evaluate as true, only one of the conditions in the expression needs to be true.
If Condition A is true, the expression will return true regardless of whether Condition B is true or false.

If Condition B is true, the expression will return true regardless of whether Condition A is true or false.

### NOT
NOT can be used when checking that a condition is false (or not true).
For example:
* (NOT Condition A and Condition B) evaluates as true only if Condition A is false and Condition B is true.
* (Condition A and NOT Condition B) evaluates as true only if Condition A is true and Condition B is false.
* (NOT Condition A and NOT Condition B) evaluates as true only if both Condition A and Condition B are true.

> NOT is also useful when using a loop. For example, you can use a NOT to check 
While button A is NOT pressed, continue to run this code…

> Note: ‘False’ can be thought of as equivalent to ‘NOT true’.
