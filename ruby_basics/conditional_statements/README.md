# Conditional statements

Conditionals are used to add branching logic to your programs/scripts, they allow you to include complex behaviour that only occurs under specific conditions.

Here's an example of an `if` statement:

```
if condition
  # something to be done
end
```

`condition` is an expression that can be checked whether it's evaluating to a `true` or `false` value, depending on that, the code block is executed.

You can combine `if` with the keyword `else`. This lets you execute one block of code if the condition is `true`, or a different one, if the condition is `false`.
```
if condition
  # something to be done
else
  # other thing to be done if the condition is false
end
```

You can also combine multiple `if` statements by using `elsif` and `else` as well:
```
if condition
  # something to be done
elsif some_other_condition
  # something else to be done if the first condition is false
elsif some_other_second_condition
  # something lse to be done if the first and second condtions are false
else
  # other thing to be done if all of the above conditions are false
end
```

[Click here to go back to the Ruby basics](../)

[Click here to go to the next chapter](../unless_until_while/)
