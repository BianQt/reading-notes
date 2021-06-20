# Expressions and operators
JavaScript has many expressions and operators, such as assignment, comparison, arithmetic, bitwise, logical, string, ternary and more.

## Logical operators
Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table.

 
|  Operator  | Usage   |Description    |
| ----------- | ----------- |----------- |
| Logical AND      | expr1 && expr2     |Returns expr1 if it can be converted to false; otherwise, returns expr2. Thus, when used with Boolean values, && returns true if both operands are true; otherwise, returns false.     |
| Logical OR   II   | expr1 II expr2     |Returns expr1 if it can be converted to true; otherwise, returns expr2. Thus, when used with Boolean values, II returns true if either operand is true; if both are false, returns false.     |
| Logical NOT (!)   | !expr1   |Returns false if its single operand that can be converted to true; otherwise, returns true.    |



# Loops and iteration
Loops offer a quick and easy way to do something repeatedly.You can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another.



## For Statement
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

A for statement looks as follows:
> for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement

## While Statement
A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:
>while (condition)
  statement