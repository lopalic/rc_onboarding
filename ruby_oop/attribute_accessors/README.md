# Attribute accessors

In the previous chapter, you've already encountered an attribute accessor, however it wasn't the best example of it.

An attribute accessor, unifyes both an attribute reader and an attribute writer with just one statement.

They are depicted with the following keywords:
```
attr_reader # attribute reader
attr_writer # attribute writer
attr_accessor # attribute acessor
```

Remember how we defined a class before using `@some_variable` to store its instance value?

Now you no longer have to do that!

The following class definition:
```
class Example
  attr_writer :value_to_write
  attr_reader :value_to_read
  attr_accessor :something_entirely_different

  @value_to_read = 'something'
end
```

Allows you to do the following:
```
example = Example.new

example.value_to_read # would print out 'something'
example.value_to_write = 5 # would store the value of the number 5 into @value_to_write, even though it's not defined

example.something_entirely_different = 'look at me!' # would store the value 'look at me! into @something_entirely_different'
example.something_entirely_different # would print out 'look at me! into @something_entirely_different'

```

To keep things simple, `attr_writer` allows you to write values into an instance variable, but not read them.
`attr_reader` allows you to read value from an instance variable, but not write to it.
`att_accessor` allows you to both read and write to an instance variable giving you more freedom with your code.

This is the end of Ruby OOP, you can only go back to the repository root from here and continue with Git.
