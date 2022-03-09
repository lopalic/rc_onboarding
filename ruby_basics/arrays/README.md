# Arrays

Arrays allow you to goup multiple values together in a list(or array if you preffer).
Each values in an array is reffered to as an 'element'.

The code below demonstrates how to create arrays:
```
my_first_array = [] # an empty array
my_second_array = [1, 2, 3] # and array with 3 elements
```

Array elements are numbered starting at zero and can be accessed by using the `[]` method and their number(index).
For example, if you wanted to access the first element of `my_second_array`, you would use `my_second_array[0]` or even `my_second_array.first` would work in Ruby.

To change an element in an array, you can assign the value to the desired element index:
`my_second_array[1] = 5 # this would change my_second_array[1]'s value from 2 to 5`

Also, unline other languages, Ruby does not care about having different types in an array(list) object.
Doing `puts [5, 'a', 3.1415, true]` would be completely valid syntax, as can be seen if you run `ruby example` from this directory.

[Click here to go back to the Ruby basics](../)

[Click here to go to the next chapter](../hashes_and_symbols/)
