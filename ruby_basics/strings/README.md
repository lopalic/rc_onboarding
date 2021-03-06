# Strings

A string is a collection of characters inside quotation marks.
Strings are interpreted as raw text.

You can use single or double quotes for strings, either is acceptable*.

```
my_first_string = 'I am a string!'
my_second_string = "I am as well!"""
```

There are many built-in method in Ruby for manipulating strings.

`.length` will give you the number of characters in a string.
`'Hi!.length # will return 3`

`.reverse` will flip a string around.
`'Hi!'.reverse # will return '!iH'`

`.upcase` will give you a string in all upper-case characters.
`'Hi!'.upcase # will return 'HI!'`

`.downcase` will give you a string in all lower-case characters.
`'Hi!'.upcase # will return 'hi!'`

Chaining method calls is also working in Ruby, they are evaluated from left to right.
`'Hi!'.downcase.reverse # will return '!ih'`

You can also check for sub-strings easily.
`'Hello world!'.include?('Hello') # will return true`

[Click here to go back to the Ruby basics chapter](../)

[Click here to go to the next chapter](../arrays/)
