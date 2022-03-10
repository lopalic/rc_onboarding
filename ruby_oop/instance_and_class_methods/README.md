# Instance and class methods

Instance and class methods are methods that you can call from an instance, or object of a given class, and class methods are method you can call from the class itself.
They are mutually exclusive, so you can call instance methods **only** on instances of a class, but can't call class methods, and vice versa, you can call class methods **only** on the classes themselves, but not on their instances.
The keyword making the difference in Ruby is `self`.

For example, say we have the following class definition:
```
class MyClass
  def self.from_the_class
    puts 'this is called from the class itself'
  end

  def from_an_instance
    puts 'this needs an instance to be called'
  end
end
```

Then, the following code would produce this output:
```
MyClass.from_the_class # would print out 'this is called from the class itself'
MyClass.from_an_instance # would print out "undefined method `from_an_instance' for SayHello:Class"

my_object = MyClass.new
my_object.from_the_class # would print out "undefined method `from_the_class' for #<SayHello:some_hexadecimal_value_of_the_object"
my_object.from_an_instance # would print out 'this needs an instance to be called'
```

[Click here to go back to the Ruby OOP](../)

[Click here to go to the next chapter](../instance_and_class_variables/)
