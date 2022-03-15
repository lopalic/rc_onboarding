# Unless, until, while

The `unless` statement is structure similar to an `if` statement:
```
unless condition
  # something to be done
end
```
However, it is the inverse of the `if` statement, checking if the `condition` is `false` and only executing in that case.

For ease of understanding, the code block above can be written as:
```
if !condition
  # something to be done
end
```

The `!` operator inverts the result of a boolean, so `!true` becomes `false`, and `!false` becomes `true`.

`while` statements repeat a block of code as long as the condition is `true`, the example of its syntax is as follows:
```
while condition
  # something to do
end
```

`until` statements are the inverse of `while` statements, repeating for as long as the conditions is `false`:
```
until condition
  # something to do
end
```

## Important!
Take note of your loop conditions for `while` and `until` blocks, it's easy to make a mistake and end up in an infinite loop preventing your program/script from ever advancing to the next command!

[Click here to go back to the Ruby basics](../)

[Click here to go to the next chapter](../loops/)
