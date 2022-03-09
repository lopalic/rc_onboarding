# Function with parameters

Similarly to functions without parameters, functions with parameters can be defined like this for example:
```
def my_function_with_parameters(parameter1, parameter2, parameter3)
  puts parameter1
  puts parameter2
  puts parameter3
end
```
This would set the variables, local only to the function, within itself, called `parameter1`, `parameter2` and `parameter3`.
Such a function would be called, for example like this:
```
a = 1
b = 2
c = 3
my_function_with_parameters(a, b, c)
```
Notice how we're only passing the values of variable into the function, the variables within the function remain unchainged.

However, it is also possible to used **named** parameters when calling a function, like this:
```
def my_function_with_parameters(parameter1:, parameter2:, parameter3:)
  puts parameter1
  puts parameter2
  puts parameter3
end
```
This would make it impossible for a call like `my_function_with_parameters(a, b, c)` to work.
Instead, you would have to call it like this `my_function_with_parameters(parameter1: a, parameter2: b, parameter3: c)` which would work without any problems.

The advantage of using named parameters is that it's easier to keep track of what values you're passing to which function, instead of just blindly calling a function with some values, it makes it easier for people other than you to understand and read the code you wrote.

One other thing worth mentioning here is default values.

If you wanted to define a default value without named parameters, you could do something like this:
```
def my_function_with_default_values(parameter1: 5, parameter2 = 'something', parameter3)
  puts parameter1
  puts parameter2
  puts parameter3
end
```

This would require you to call this function with named parameters, but only if you wanted to change the value of `parameter1` or sending a value in without a name, to the second argument for `parameter2`, while requiring you to send whatever value for `parameter3` since it has no default value.
So the following would all be valid calls of the function:
```
my_function_with_default_values(parameter1: 'whatever', 'something else', 'whatever again)
my_function_with_default_values('something else', 'whatever again)
my_function_with_default_values(parameter1: 'whatever', 'whatever again)
```
[Click here to go back to the Ruby basics](../)

[Click here to go to the next chapter](../pry_debugger/)
